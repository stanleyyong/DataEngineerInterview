# DataEngineerInterview

Before you start, you have a total of 3 questions in this problem set. Each problem is equally weighted and you have a total of 1 hour to attempt all of them. You are encouraged to show your work and thought processes. Problem 2 involves writing code, and you have been provided with a computer and Visual studio code.

### Problem 1 :

Come up with a program to compute the longest common substrings between two DNA strands (where each letter is one of {C, A, G, T}). 

Solve the problem for these two substrings:

Strand 1: AGCATACAGGAGATTACAGGCGCATTGATTCGGGAATATA

Strand 2: AATGTCCCATTGGATGATTACAACCGTCAGGGCGTATAAA

What is the statistical significance of the match between the two strands? 
Can you give an approximate measure of Type 1 errors, i.e. false positive matches between DNA strands?

### Problem 2 :

Basic sales tax is applicable at a rate of 10% on all goods, except books, food, and medical products that are exempt. Import duty is an additional sales tax applicable on all imported goods at a rate of 5%, with no exemptions.

When I purchase items I receive a receipt which lists the name of all the items and their price (including tax), finishing with the total cost of the items, and the total amounts of sales taxes paid. The rounding rules for sales tax are that for a tax rate of n%, a shelf price of p contains (np/100 rounded up to the nearest 0.05) amount of sales tax.

Write an application that prints out the receipt details for these shopping baskets...

INPUT

#### Input 1:

1 book at 12.49

1 music CD at 14.99

1 chocolate bar at 0.85

#### Input 2:

1 imported box of chocolates at 10.00

1 imported bottle of perfume at 47.50

#### Input 3:

1 imported bottle of perfume at 27.99

1 bottle of perfume at 18.99

1 packet of headache pills at 9.75

1 box of imported chocolates at 11.25

OUTPUT

#### Output 1:

1 book: 12.49

1 music CD: 16.49

1 chocolate bar: 0.85

Sales Taxes: 1.50

Total: 29.83

#### Output 2:

1 imported box of chocolates: 10.50

1 imported bottle of perfume: 54.65

Sales Taxes: 7.65

Total: 65.15

#### Output 3:

1 imported bottle of perfume: 32.19

1 bottle of perfume: 20.89

1 packet of headache pills: 9.75

1 box of imported chocolates: 11.85

Sales Taxes: 6.70

Total: 74.68

### Problem 3 :

We take two balls, one at a time without replacement, at random from an urn starting with 10 black balls and 20 white
balls. 

The second ball removed is dropped and we replace it with one of the same color as the first ball. So if we had a pair of <ball 1: black, ball 2: white>, we would place 2 black balls back into the urn. If we had a pair of <ball 1: white, ball 2: black>, we would place 2 white balls back into the urn.

We repeat the experiment indefinitely. What is the probability that all the balls in the urn eventually turn black?
