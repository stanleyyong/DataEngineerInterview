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

PROBLEM ONE:  TRAINS
Problem:  The local commuter railroad services a number of towns in
Kiwiland.  Because of monetary concerns, all of the tracks are &#39;one-way.&#39;
That is, a route from Kaitaia to Invercargill does not imply the existence
of a route from Invercargill to Kaitaia.  In fact, even if both of these
routes do happen to exist, they are distinct and are not necessarily the
same distance!
The purpose of this problem is to help the railroad provide its customers
with information about the routes.  In particular, you will compute the
distance along a certain route, the number of different routes between two
towns, and the shortest route between two towns.
Input:  A directed graph where a node represents a town and an edge
represents a route between two towns.  The weighting of the edge represents
the distance between the two towns.  A given route will never appear more
than once, and for a given route, the starting and ending town will not be
the same town.
Output: For test input 1 through 5, if no such route exists, output &#39;NO
SUCH ROUTE&#39;.  Otherwise, follow the route as given; do not make any extra
stops!  For example, the first problem means to start at city A, then
travel directly to city B (a distance of 5), then directly to city C (a
distance of 4).
- The distance of the route A-B-C.
- The distance of the route A-D.
- The distance of the route A-D-C.
- The distance of the route A-E-B-C-D.
- The distance of the route A-E-D.
The number of trips starting at C and ending at C with a maximum of 3 stops.  In the sample data below, there are two such trips: C-D-C (2 stops). and C-E-B-C (3 stops).
The number of trips starting at A and ending at C with exactly 4 stops.
In the sample data below, there are three such trips: A to C (via B,C,D); A to C (via D,C,D); and A to C (via D,E,B).
The length of the shortest route (in terms of distance to travel) from A to C.
The length of the shortest route (in terms of distance to travel) from B to B.
The number of different routes from C to C with a distance of less than 30.
In the sample data, the trips are: CDC, CEBC, CEBCDC, CDCEBC, CDEBC,

### Problem 3 :

We take two balls, one at a time without replacement, at random from an urn starting with 10 black balls and 20 white
balls. 

The second ball removed is dropped and we replace it with one of the same color as the first ball. So if we had a pair of <ball 1: black, ball 2: white>, we would place 2 black balls back into the urn. If we had a pair of <ball 1: white, ball 2: black>, we would place 2 white balls back into the urn.

We repeat the experiment indefinitely. What is the probability that all the balls in the urn eventually turn black?
