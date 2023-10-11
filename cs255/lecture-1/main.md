# Rational Agents
## Defining Agents
We can define an [[Agent]] and understand that they work under practical constraints which often make perfect reasoning unattainable or impractical

Hence, a good agent is one which aligns closely with some *[[Goals or Preferences]]* and we can use a [[Performance Measure]] to judge this quantitatively

An action that maximises the expected value of the [[Performance Measure]] given the [[Past Experiences]] of the agent to date is what we would then define as a [[Rational Action]] *(i.e. doing the right thing)*

It is worth noting the **importance** of considering the [[Past Experiences]] of the [[Agent]] to date
- Doesn't take long to think of a situation that would explain why this is the case
### Conditions for an agent to act intelligently
In general, we can outline the following 3 conditions for us to be able to say that an agent acts intelligently:
1. It is versatile in a changing environment and learns from experience
2. It works within practical constraints
3. It makes choices aligning with its goals and preferences
### Inputs to an Agent
1. [[Abilities]]
2. [[Goals or Preferences|Goals/Preferences]]
3. [[External Stimuli]] 
4. [[Past Experiences]]
5. Prior Knowledge
#### Diagram
![[Pasted image 20231007154930.png]]
#### Example: Autonomous Car
##### Abilities
- Steer
- Accelerate
- Brake
etc.
##### Goals
- Get to destination
- Safety
- Timeliness
etc.
##### External Stimuli
- Peripheral Vision
- Cameras
- GPS
etc.
##### Past Experiences
- Commonly traversed routes
- Braking distance relative to speed
etc.
##### Prior Knowledge
- What signs mean
- What to stop for
etc.
## Dimensions of Complexity
This modules focuses on the engineering goal of designing useful, intelligent agents.

We can approach this design problem as being defined by 10 dimensions of complexity:
### 10 Dimensions
1. Modularity
2. Planning Horizon
3. Representation
4. Computational Limits
5. Learning
6. Sensing Uncertainty
7. Effect Uncertainty
8. Preference
9. Number of Agents
10. Interaction
#### Inter-level interaction
These dimensions all interact in complex and intricate ways,; some interact more-so than others

## Representations
### Motivation
To solve some informally defined task, we must first find a formal representation so we can use computational help, the output of which we then integrate into a real-world solution.
### What do we want in a representation?
We want a *good* representation to be:
- Detailed
- Accurate
- Able to be acquired from people, data and [[Past Experiences]]
- [[Amenable to a Computational Solution]]
## Solutions
### Assumptions
Typically, given an informal definition of a problem, much is left unspecified but the unspecified parts cannot be filled in arbitrarily

Much work in AI is motivated by [[Common-Sense Reasoning]]
### Quality of Solutions
We can broadly categorise how [[Performance Measure|good]] a solution is using [[Classes of Solutions|classes]]
## Reasoning
### Definition
We can think of reasoning as the computation which determines how the agent should act.

There are broadly 3 [[Categories of Reasoning]]