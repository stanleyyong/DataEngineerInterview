## The payment problem

Note to candidate: This is an open-book task, you can use any resources as long as you acknowledge them to the interviewer. Try your best to complete this and explain your reasoning!

Movmint is in the business of helping Central Banks build central bank digital currency systems. One of the main uses for such systems is to help people to make and receive payments electronically instead of using cash! In our system, we keep a record of the amounts of central bank digital currency each person is holding, and a record of the transactions that are done between them. The transactions change the amounts of money people end up with.

We interpret the table below as a row-wise definition of payment requests where the sender is paying the stated amount to the receiver. 

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/4c7b526b-34c6-46dd-8e73-5ea299bae25c)

For example, if we examine the first row which is labeled Tx1, A pays 25 to C. 

One could represent the system as a set of states with transitions between them. This state diagram is a sample:

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/b250fd69-61e0-4ac2-a1ee-0bc2c8315528)

In reality, we can have situations where state transitions are impossible under a given set of constraints. For example, if we impose a constraint that everyone must be solvent at all times, that can be stated as the statement: "All balances are non-negative". Now if A and C begin with only 20 instead of 30, Tx1 is no longer possible. In such cases we have the choice to reject the transaction immediately, or if we have the option of taking some time, we might queue the transaction until the sender has sufficient funds to pay out without going negative.

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/9e8628e0-501f-41c5-86d6-4b8ea36acc98)

If one receives the following set of transactions to execute, we must know the balances that each actor has at the start to correctly choose the state of the world after each transaction is attempted.

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/9950b731-b238-4b7a-b674-bdb390a97d8b)

For the following questions, assume that everyone starts with a balance of 20.

### Question 1
If we do not have a non-negative constraint, which actors will end up in bankruptcy and by how much?

### Question 2
If we impose a non-negative constraint, and each transaction has to be executed individually, which transactions can be executed?

### Question 3
Netting is the concept of allowing multiple transactions to happen at once such that their effects can cancel out. Netting works as long as: incoming money + current balance > outgoing money

Consider the following netting problem:

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/bd3de98c-e5dd-460f-99eb-272d87f7d3f9)
 
In this example, we have two examples of payment cycles. The first is Alice, Bob, Charles and the second is Bob, Charles, Demi. Of interest is that both of these payment cycles represent scenarios, sometimes referred to as gridlocks, in which no one participant is able to unilaterally make a payment, yet it is possible for either payment cycle to be resolved as a set.

One way to net off simultaneously is to do this:
![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/d37e75a7-4603-44fa-af96-1e461ab0a201)

We revisit the problem set of 12 transactions:
![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/e3e5743e-4314-4508-97b2-7d27e1eb8925)

If we allow multiple transactions to execute at once so that their effects can be netted, can you find the maximum amount of transactions that can be settled?

(Hint: what if we deactivate some payments in the queue? Can we go through the set of actors in deficit at the end and remove the transactions that end up taking them to bankruptcy? Then repeat until everyone is solvent?)

For example, you might do this:

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/f4af9b36-a56a-4550-827e-3da07f48b794)

This would mean that the transaction Tx9 is skipped, or the amount is set to 0 (both equivalent in effect on the state).

Give an explicit solution! Tell me:

1. How many transactions are deactivated
2. What amount is paid out of the total that was supposed to be paid

### Question 4
Back to the problem with Alice, Bob, Charles and Demi:
![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/bd3de98c-e5dd-460f-99eb-272d87f7d3f9)

I'd listed one way to net off the transactions. Can you draw a state diagram for the other netting set? What if we tried to net both sets at the same time? Is that going to be successful in avoiding bankruptcy for everyone?

### Question 5
Can you fix this situation? What is required for the fix to work?

### Question 6
What if the actors are not able to coordinate and must act in a decentralized way? Can you still solve this conundrum? What are the issues involved?
