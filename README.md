# Artificial Intelligence - Intelligent agents paradigm

Egons.Lavendelis@rtu.lv - [Zunda Krastmala 10](https://goo.gl/maps/faKAXrtxrRuY6Q156) room 410

Course work
- laboratory works as hometasks - 40%
- video lectures
- online tests
- exam 60%
- Online tests sometimets to earn more points. (~5 tests)

`grade = 0.4*course_work+06*exam+bouns` only if `0.4*course_work+0.6*exam>=4`

lectures:
- 12:30-14:05
- 14:30-16:05

mandatory tasks: 
- 5 labs - min 2
  - large set of practical problems
  - tasks
    - do the task with the packaged software, create a report
- laboratory works:
  - intelligent agents
    - 4 points
    - `.net` 
  - search
    - 4 points
    - java
  - planning agents
    - java
  - inductive learning
    - java
  - complex decision making
    - .net
```
points scored   grade
at least 12     10
10 to 12        9
9 to 10         8
8 t 9           7
...             ...
```

**deadlines**
- fst deadline: april 3
- all other semester work: may 22
- extended deadline, without feedback: may 30

**text books:**
- Russel S and Norvig: Artifcial Intelligence
------

> **objective** strengthen theoretical knowledge about modern approaches of artificial intelligence acquired at the lectures of the course

## What is AI
- those unknown pocesses with which our brains solve problems ~ Minskiy
- the definition change through the years, which makes it difficult to explain 

**roots of AI:**
- philosophy
  - how the world works
  - what we think about something 
- mathematics
  - formal logic
  - algorithms  -  
- psychology
  - behaviorism
  - cognitive science 
- neuroscience 
- economics
  - decision theory, utility theory 
  - game theory
- computer science *(1940- about this part of computing)*
  - efficient computer 
- linguistics
  - natural language processing

*The mind is something behind the machine*

If you look at the mind as a machine then you can replicate it. If you look the emotional beeing behind the mind then you will see emotions, feelings, free will, etc, and we can't replicate them.

[![Shaky, the robot - YouTube video](https://i.ytimg.com/an_webp/qXdn6ynwpiI/mqdefault_6s.webp?du=3000&sqp=CIiJ748G&rs=AOn4CLAasbVZeqNwAbBxdXpdLYVaL_6I0w)](https://youtu.be/qXdn6ynwpiI)

1. Turing test
2. rational agent aproach
   - the agent is just something that acts
   - a rational agent acts like the best outcome

- view of intelligence
- collective behaviors
- agennt -oriented and emergent view of intelligence
  - autonoumus systems
  - agents situted in enviroment
 
## Agents and their structures - introduction to search
presentation: [slidetodoc.com](https://slidetodoc.com/rational-agents-chapter-2-outline-agent-function-and/)

> **Agent is just something that perceives and acts**. Functions: mapping percepts to actions.
>
> ![the structure of an agent metaphor](https://www.researchgate.net/profile/Pj-Tavner/publication/312707484/figure/fig1/AS:577987449810944@1514814354116/Agents-interact-with-environment-through-sensors-and-effectors-11.png)
> 
> **An agent is anything that can be viewed as *perceiving* its anviroment through sensors and *acting* upon that enviroment through effectors**
> 
> *based on this definitoin a termostat is an intelligent agent* 
> 
> **properties of intelligent agents:**
> ### reactivity
> - the capability to follow the enviroment all the time, including during the reasoning and acting
> - the agent must take an action when the action is meaningful
> ### proactivity
> ### autonoumus
> ***the agent coióntinues to learn uppon its experience***
> - one whose actions are not based completly on:
>   - built-in knowledge
>   - own experience
> - truly autonoumus agent can adapt to wide variety of enviroments
> ### social capability
> - can interact with other agents
> - agents can work together => multi agent system
> ### other aproaches of defining
> - viewed as consisting of mental components such as: beliefs, capabilities, choices, commitments
> - an entity is a software agent if and only if it communicates correctly in an agent communication language

### rational agent
- does the right thing
- the best available action
- rational: performande, percept sequence, knowledge about the enviroment, actions
- ideal rational
- omniscient <- knows everything

#### performance measure
- to determine if the agent does right things 
- outside the agent <- to be more objective valuation
- is defined by some authority
- how and wen to evaluate agents success

#### percept sequnece

#### knowledge about the enviroment

#### actions 


An agent is a **proram and an architecture**
- percepts
- actions
- goals
- enviroment

**PEAS/PAGE** description - *P*erformance *e*nviroment *a*ctuators and *s*ensors / *p*ercepts *a*ctions *g*oals *e*nvironment

| Agent | Performance | Enviroment | Actions | Sensors | 
|------|-----------|-----------| -------------|---------|
| Interactive English tutor | Maximie scored in the test | Student group | Witten tasks | written words|
| automated taxi driver | safe, fast, legal trip, maximal profit | Roads, other traffic, pedestrians, customers | Steering, accelerator, brakes, signal | cameras sonar, speedometer |
| Medical diagnosis system | Healthy patioents minimal costs | patients, hospital staff | questions, tests, treatments | symptoms, patent answers |

**enviroments**
- the range can be vast
- there are some dimensions that categorize enviroments
- characteristics: 
  - observability
    - fully observale: agents sensors give access to compplete state of the enviroment
    - effectively fully observe: detect everthing which is relevant to me now  
    - partially observable: noisy or inaccurate sensors or parts of the state are missing ins sensors sdata *ex: vacuum cleaner can not perceivve dirt in another room
    - unobservable: agent has no sensors at all
  - deterministics vs stochastic:
    - deterministic: next state the enviroment is completly determinated by current state and action executed by the agent
    - stochastic: uncertainity about outcomes is quantified in terms of probabilities  
  - episodic vs sequnetial 
    - episodic: the experience is divided in atomic episodes  
      - episode: an agent recieves a percept and performs a single action
      - epsodes do not depend on actions taken in prev episodes 
      - *calssification tasks* 
    - sequnetial: current decision can be larger   
  - single vs multi-agent
    - single: only on agent *ex: agent solving crosswqord puzzle*
    - multi-agent: there are other agents maximizin a performance measure that depends on the behavior of other one *ex: chess*
  - static vs dynamic
  - known vs unknown:
    - in known enviroment the designe knows the laws of physics *ex: the outcome probability of actios is known*
    - unknown: the agent has to learn how the enviroment works: *ex an unkown video game, wher don't know how to solve/use it* 

**the skeleton of agent:**
- choose best action
- action: update memory
- return: action
  
**table driven agent:**
- percept sequneces: look-up percepts, table
- return action
  
**rule based agent:**
- percept: interpretation
- rule match: interpreted percept, if pattern
- rule firing: then pattern
- action: return actrion

*applications in lgoical reasoning systems*

![siple reflex agent](https://upload.wikimedia.org/wikipedia/commons/3/3f/IntelligentAgent-SimpleReflex.png)

[Intelligent agent](http://static.hlt.bme.hu/semantics/external/pages/%C3%A1ltal%C3%A1nos_mesters%C3%A9ges_intelligencia/en.wikipedia.org/wiki/Intelligent_agent.html)

**model based agent**

![model based agent](https://static.javatpoint.com/tutorial/ai/images/model-based-reflex-agent.png)

**goal based agent**
- goal
- interface
- search and planning

![goal based agent](https://slideplayer.com/slide/3955449/13/images/29/Goal+Based+Agent+CISC4%2F681+Introduction+to+Artificial+Intelligence.jpg)

**utility agent**
- utility function assigs a real number starting how good the state is for the agent
- the higher the utility is the better the state is for the agent

## lab1 
> compare performance of differen computer agent types with human agents that have the same information as the computer agents
>
> The objective of the laboratory work is to study behaviour of different types of intelligent agents on the example of vacuum cleaning agent. The following types of agents are used in experiments: global optimization agent, local optimisation agent and random choice agent. Results achieved by human agent and computer agent must be compared based on experiments with the software “AgSim – 05”. The answers to the control tasks and conclusions must be given in the report.

## Search 
problem solving agent
1. goal formulation
2. problem formulation - process of decideing what actions and states to consider
3. search: systematic exploratio of the sequnece of alternative states that appear in a problem solving
4. current state
5. action
6. return

### problem types:
- single state problem
  - percepts: give enough info to tell exactly which state is it
  - agent knows exactly what each of its actions 
- multiple state poblem
  - percepts give not enough info to tell which state is it
  - agent knows all the effects of its actions
  - agent must reason about f states that it might get to

> **problem**: isa collection of information that the agent can use to decide what to do.
> specialization for single state probelm

> **state space** s the set of all states reeacheble from the initial state by any sequence of actions
> - initial state: is the state that the agent knows itself to be in
> - goal statet corresponds to the solution of the problem
> - operator describes an action in terms od which state will be reached by carrying out the action
> 
> representation: four tuple: `[N, A, IS, GS]`
>  - `N` - nodes - states
>  - `A` - edges
>  - `IS` - Initial state
>  - `GS` - goal states: agent can apply if explicit state or measurable property of the states encountered in the search, property of the path developed in the search.

representation with raphs:
- nodes: particluar problem splution states
- arcs: problem solving process
- initial states: from root of the graph and correspond to the given information ina problem instance

[Branching factor](https://en.wikipedia.org/wiki/Branching_factor): number of edges of a node. 

**how to mesure effectiveness:**
- does a search find a solution at all?
- is a solution good?
- what is the search cost associated with the time and memory required to fin a solution

`total cost = pth cost + search cost`

**search process:**
- builds up a search tree
- start drom search node - initial state
- dettermining the childre of state is called expanding the state

at each step the search algorythm chhooses one leaf node to excpand:
1. they have not been expanded
2. expanded but not the correct way

## Uninformed search
### Backtracking
> systematic move foreward and not coming back
> 
> - starts at initial and end at particular solution
> - there is no solution at any time
> 
> ![backtrack algo](https://www.w3.org/2011/Talks/01-14-steven-phenotype/backtracking.png)
> 
> but how will machine implement it?
> 
> ![backtrack idea](https://github.com/gabboraron/artificial_intelligence-intelligent_agents_paradigm/blob/main/backtrack_search.jpg)

### Classification of Search strategies
![goal vs data driven search](https://slideplayer.com/slide/13956099/86/images/62/Strategies+for+State+Space+Search.jpg)

there are cases where data driven is better then goal driver, and vice versa

### data driven
like above
### goal driven:
- search strarts from the goal, applies operators that could produce the goal, and chains backward to given facts of the problem
- searching backward means generating
- is better when there is more branching factor

### informed search
problem specific knowledge is used, so we have to know the problem

### uninformed search
**no** information is available about:
- the number of steps 
- the cost
- how good is the current state

in order which nodes are expended is:
- breath first search
- uniform cost search 
- depth-first search 
- depth limited search
- iterative deepening search
- bidirectional search

> #### breath first search 
> - this search expands the shallowest node in the search tree first
> 
> ![breath first search](https://i.ytimg.com/vi/oDqjPvD54Ss/maxresdefault.jpg) 
> 
> ![breath fst](https://github.com/gabboraron/artificial_intelligence-intelligent_agents_paradigm/blob/main/breadt%20fst.jpg)
> 
> [YouTube - Breadth First Search Algorithm | Shortest Path | Graph Theory](https://www.youtube.com/watch?v=oDqjPvD54Ss)

> #### uniform cost search
> - this search expands the lowesst cost node on the frontier first
> - the path cost must never decrease `g(successor(n)) >= g(n)`
> 
> ![uniform search strategy](https://cdn.educba.com/academy/wp-content/uploads/2020/02/Uninformed-Search-4.jpg)

> #### depth-first search
> works the same way as the backtracking

> #### depth limited search
> same as depth-first search, but have a maximum trashold what can achive in a direction
> 
> ![depth limited](https://github.com/gabboraron/artificial_intelligence-intelligent_agents_paradigm/blob/main/depth%20limited.jpg)

> #### iterative deepening search
> - has a limit
> - if fails then increase the limit
> - each time restart the search algo from the root

> #### bidirectional search
> iterative deepening search and depth-first from the other direction at the same time

> #### saving path
> ![](https://github.com/gabboraron/artificial_intelligence-intelligent_agents_paradigm/blob/main/saving%20path.jpg)

### Implementing search algorithms
two lists are used to implement algo:
- open: the nodes which we didn't found yet
- closed: which we already found it

to implement breadth-first and depth-first
- initially open contains the initial node
- states are excluded from the left side of the open list
- new states are included in **the right side** of open in case of breadth first search and in **the left side** in case of depth first search
- algo terminates when the goal state is either in the first **position of the list open** or is inserted into the list closed
- states that already are open or closed are not added to the list open

### evaluation of uniformed search strategies
- completeness - is a solution guaranteed?
- time complexity - time needed for solution
- space complexity - memory needed for solution
- optimality - is highest quality solution quaranteed when there are several different solutions?

| criterion | breadth first |uniform | depth first | dept limited | iterative deepening | bidirectional |
| ------- | ---- |----- |----|---- |----- |----|
| complete | + | + |- | + if l>= d | + | +  |
|time | b^d | b^d | b^m|b^l | b^d |b^(d/2) | 
|space | b^d | d^b | **bm** | **bl** | b^(d/2) | 
| optimal | + |+ |-| - | + |+ |

- *b* branching factor (every state can be expanded to yield *b* new states)
- *d* is the depth of solution
- *m* is the maximum depth of the search tree
- *l* is the depth limit

***NEXT TIME TEST***
1. open zoom
2. open camera
3. turn off microphone
4. open test
5. take it
6. send it in MSWord or Pdf

