We interpret the table below as a row-wise definition of payments where the sender is paying the stated amount to the receiver. 

For example, if we examine the first row which is labeled Tx1, A pays 25 to C. 

One could represent the system as a set of states with transitions between them. This state diagram is a sample:

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/b250fd69-61e0-4ac2-a1ee-0bc2c8315528)

In reality, we can have situations where state transitions are impossible under a given set of constraints. For example, if we impose a constraint that everyone must be solvent at all times, that can be stated as the statement: "All balances are non-negative". Now if A and C begin with only 20 instead of 30, Tx1 is no longer possible. 

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

If we allow multiple transactions to execute at once so that their effects can be netted, can you find the maximum amount of transactions that can be settled?
(Hint: what if we deactivate some payments in the queue? Can we go through the set of actors in deficit at the end and remove the transactions that end up taking them to bankruptcy? Then repeat until everyone is solvent?)

Give an explicit solution!


