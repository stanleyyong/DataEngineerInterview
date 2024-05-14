We interpret the table below as a row-wise definition of payments where the sender is paying the stated amount to the receiver. 

For example, if we examine the first row which is labeled Tx1, A pays 25 to C. 

One could represent the system as a set of states with transitions between them. This state diagram is a sample:

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/b250fd69-61e0-4ac2-a1ee-0bc2c8315528)

In reality, we can have situations where state transitions are impossible under a given set of constraints. For example, if we impose a constraint that everyone must be solvent at all times, that can be stated as the statement: "All balances are non-negative". Now if A and C begin with only 20 instead of 30, Tx1 is no longer possible. 

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/9e8628e0-501f-41c5-86d6-4b8ea36acc98)



![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/d2bb1df0-8ff9-43fb-8ba1-5612b30d5c92)



![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/9950b731-b238-4b7a-b674-bdb390a97d8b)


![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/880745e7-515a-4df2-9e80-7a6fa187130e)

Consider the following netting problem:

![image](https://github.com/stanleyyong/DataEngineerInterview/assets/18695878/bd3de98c-e5dd-460f-99eb-272d87f7d3f9)
 
In this example, we have two examples of payment cycles. The first is Alice, Bob, Charles and the second is Bob, Charles, Demi. Of interest is that both of these payment cycles represent scenarios, sometimes referred to as gridlocks, in which no one participant is able to unilaterally make a payment, yet it is possible for either payment cycle to be resolved as a set.
x
