# Stable Matching
Conceptually, this is based around [[stable matching theory]] from economics
## Motivating Example: Matching Medics
### The Problem
The specification of this example is as follows:
- We have `n` qualified doctors who want a job
- We have `n` hospitals that each have one post for a new doctor
- Doctors and hospitals both have preferences
- We want to find an assignment that respects the preferences

Given a set of preferences, the goal is to design a [[self-enforcing]] admissions process
- i.e. we want a find a way of matching up doctors and hospitals that respects both of their preferences while also considering what's best for the population at large

We want to avoid [[Unstable Pair|unstable pairs]] and try to ensure [[stable assignment]] whenever possible. 

In an ideal world we not only want to achieve [[perfect matching]], but [[stable matching]]. 

Thus, we have our problem that, given the preference lists of n doctors and hospitals, find a[[ stable matching]] if one exists
## Propose-And-Reject Algorithm
An intuitive method we can use that guarantees to find a stable matching is the [[Propose-And-Reject Algorithm]]
### Proofs of Correctness
#### Termination
##### Observation 1
Doctors apply to hospitals in decreasing order of preference 
##### Observation 2
Once a hospital is matched, it never becomes unmatched; they only get an improved match 
###### Claim
Algorithm terminates after at most n^2 iterations 
###### Proof
Each time through the while loop a doctor applies to a new hospital. There are only n^2 possible pairings. QED
#### Perfection
##### Claim
All doctors and hospitals get matched
##### Proof (by contradiction)
- Suppose, for sake of contradiction, that Erika is not matched upon termination of algorithm
- Then some hospital, say Vienna, is not matched upon termination (since there are n doctors and n hospitals)
- By Observation 2, Vienna was never applied to
- But, Erika should have applied everywhere, since they end up unmatched
- This is a contradiction, so this cannot happen
- Therefore the claim is true$

#### Stability
##### Claim
The algorithm does not produce any [[Unstable Pair|unstable pairs]]
##### Proof (by contradiction)
![[Pasted image 20231009112629.png]]
### Efficient Implementation
- Takes O(n^2) time to run
- Utilises arrays and queues
	- Maintain a list of free doctors in a queue
	- Maintain two arrays `doctor_at[h]` and `hospital_of[d]`
		- Set entry to 0 if unmatched
		- If`d` matched to `h` then `doctor_at[h]=d` and `hospital_of[d]=h`
- Doctors are named 1, ..., n and hospitals are labelled 1', ..., n'
	- To handle doctors applying:
		- For each doctor, keep a list of hospitals, ordered by preference
		- Keep an array `count[d]` to counts applications made by `d`
	- To handle the hospitals rejecting/applying
		- Does hospital `d` prefer doctor `d` to doctor `d'`
		- For each hospital, create **inverse** of preference list of doctors
		- Constant time access for each query after O(n) preprocessing