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