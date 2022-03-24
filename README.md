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

## heuristics
- experience bassed
- empirically found
- allows process the most promising branches first

to define heuristics: 
- **costs**: lower value is better
- **quality of the node path*: higher values is better

***depend on the domain/state space and not the algorithms/search strategy***

### classification of search strategies
- greedy search - minimizing the estimate cost to real search
- A*
- IDA* - iterative deepening A*
- SMA* search - simpilfied memory bounded A*
- iterative improvement algorithms
  - hill climbing
  - beam search
  - random restart hill climbing
  - stochastic hill climbing
  - simulated annealing

#### Best first search
- this search expands thew node appears to be the best according to the evaluation fuinction

#### greedy search 
https://www.geeksforgeeks.org/greedy-algorithms/

- reduces the time and pace complexity with a good heuristic function

### informed search strategies
more in: https://github.com/gabboraron/MI-EA 
#### A*
`f(n) = g(x) + h(x)`

#### memory bounded
condservs memory

#### iterative deepening A* - IDA*
-each iteration is depth first search - modified to use an f-cost
expands all nodes inside the contour for the current f-cost peeping over the contour to find out where the next contour is, where all nodes have `f(n)` less than or equal to f-cost
- only goes through two or three restarts since typically f only increases several times along the heuristic route

#### iterative improvement algorithms
- cheap - fast
- this search explores the state space trying to find the best value of estimated cost
- take to reach the goal very fast and with very low resources

#### SMA
more complicated tasks can be handled with this

#### beam search
- uses only the best W nodes at each level the other nodes are ignored
- uses lot of memory 
- breaadth first level by level
- all nodes from the list OPEN are expeaded
- expect only the the best weight

*beam* means how many nodes can we store

#### simulated annealing
- uses local maxima
- 
- picks a randomly seleted successor of the current node
- if the move improves the situation always executed
- probability decrases eponentially with the badness of the move calculated as difference of values between next and current state

#### hill climbing
- when we are creating path it should be good all the time
- if local choices are perfectly then the algo is it too

#### stochastic hill climbing
- randomy choses on of sucessors that imprves the quality of the state
- depends on the improvement
- **lowest heuristic**: *allwys going to lower value in the graph!*
- **highest heuristic**: *allwys going to hisgher value in the graph!*

### weakness of informed search strategies
> because heuristics use limited information they can lead a search algorithm to a suboptimal solution or fail to find any solution at all
> 
> - **best first**: is not an answer to all searching needs because at the worst case exponentional growt will occur.
> - **greedy star**: is optimal, finding the shortest path, but in worth case is neither complete
> - **`A*`**: 
> - **`IDA*`**: it can expand `N^2` nodes in `N` iteration
> - **`SMA*`** not complete and not optimal, huge memory usage
> - **Hill climbing**: will halt even thought the solution may be far from satisfactory
> 
> *different use cases needs different algorithms*

### two-player games
- two player (human or computer)
- conflict games
- players use heuristics

like in chess:
- both players know where the pieces are
- both know the possible moves

like in card games:
- players do not know the other's pieces

in each situation  each player has full information:
- chess
- tick-tack-toe
- checkers
- chess

are not: 
- poker
- bridge
- dice games

#### game tree
- game trees consists of nodes and arcs
- nodes represent a possible state of game
- edges represent a the way how we occure there
- root node is the starting position
- internal node
- leaf nodes are the possible termination places of the game
- each level in gme tree is a turn of a player

##### Mini-Max algorithm
- dividing into minimizer and maximizer levels of the game tree
- the idea is to maxximise your result in the game by minimizing opponents result
- the algorithm comes down to the leaf nodes and assigns the heuristic values that denote how good the state is for the maximizer
- the evaluations are transferred upwards
- heuristic evaluations:
  - the heuristic evaluations are given as numbers
  - they characterise how good the state is for the given player
  - 1 if the maximizer wins
  - -1 if minimizer wins
  - 0 if draw
> **steps of mimiax algorithm**
> 
> [javatpoint.com description](https://www.javatpoint.com/mini-max-algorithm-in-ai)
> 
> 1. build full gam tree
> 2. divide the gam tree into the levels (MIN-MAX)
> 3. assign heuristi evaluations to the leaf nodes
> 4. transfer the evaluations upwards till the root node
> 5. 

## MINIMAX
- in building the game tree choosing the parameters is the key

## Complex games
> - it is hard to create the game tree
> - looking forward by n moves
> 
> `F(s) = a*B + b*R+c*M+d*C+e*P+f*A` where
> - `B` total value of pieces
> - `R` protection of the king
> - `M` mobility of the pieces
> - `C` contorl over the center
> - `P` pawn structure
> - ` A` possibel attack
> - `a;b;c;d;e;f` - weights

## using knowladge
> what is knowladge?
> - an individual understanding of given subject
> - **for us only the *domain specific* knowledge is intersting!**
> - ***domain* is a well-focused area!**
> - in general a representation is a set of conventions about how to describe a class of things
> - a description makes use of the conventions of a represenation to describe some particular thing
> the function of any representation scheme is to capture essential features of a problem domain => make this available for the machine
> - the represenation language must allow the programmer to use the knowladgebase 

### wumpus world 
https://www.javatpoint.com/the-wumpus-world-in-artificial-intelligence

- cave explored by agent consist from rooms connected with passageways

![the cave](https://static.javatpoint.com/tutorial/ai/images/the-wumpus-world-in-artificial-intelligence.png)

### knewledge representation
**declarative knowledge**
- concepts
- facts
- objects

**procedureal knowledge**: describes how a problem is solved
- rules
- strategies
- agendas
- procedures

**heuristic knowledge (shallow knowledge)**: describe a rule of thumb that guides the reasoning process; it is empirical and represents the knowledge compiled by an expert throught the experience of solving past problems
- rules of thumb

**meta knowledge**: describes knowledge about knowledge. This type of knowlede is used to pick other knowledge that is best suited for solving a problem. experts use this type of knowledge to enhance the efficiency of problem solving by directing their reasoning in the most promising area.
- knowledge about the other types of knowledge and how to use them

**structural knowledge**: describes knowledge structures. this type of knowledge describes an expert's overall mental model of the problem. The expert's mental model of concepts sub-concepts and objects is typical of rhis type of knowledge
- rule sets 
- concepts relationships
- concept to object relationships

> knowledge representation language:
> 
> - syntax of the language describes the possible config
> - semantics determines the facts in the world which the sentences refer
> 
> *if yntacs and semantics are defines precisely the language is called logic* 
> 
> Sentences => semantics => facts 
> - *representation must be encoded some way that can be physically stored within an intelligent system*
> - *it is imposible to put the worlld inside a computer so all reasoning mechanisms must operate on representations of facts, rather than on facts themselves*
> 
> representation:
> - kexical
> - structural
> - procedural
> - semantic

### the role of logic in artificial intelligenc
***logical formalism suggests a powerful way of deriving new knowledge from olf mathematifal deduction; this conclusion can be made that a new statement is true by proving that it follows from the statements that are already known.***
- sound
- complete


AI programming requires means of capturing and reasoning about qualitative aspects of a problem

logic provides ai progrmmers with a well-definied language => create automation for us

logical axioms, and "problmes as theorems" representations help us attack a problem

=> AI programming languages: [PROLOG](https://en.wikipedia.org/wiki/Prolog)

- not all problems can be solved with logic
- some knowledge resits embodiment in axioms
- logic is weak as a representation for certain kinds of knowledge
- the notation of pure logic does not allow to express such notations as heuristic distances
- difficult to develop a system like that

Kinnds of logic:
- general lang:
  - propositional calculus
  - predicate calculus 
- based on general lang:
  - temporal 
  - probability
  - fuzzy 

### propositional logic
- symbols: P, Q, R, S, T
- truth symbols: True, False
- connectivities: ^; ˇ; =>, ≅, !

where
- every propositinoal symbo and truth symbol is a sentence
- negation of a sentance is a sentance
- conjunction or AND of two sentences is a sentence


how to test truth validity:
- truth table method:
  - `+` any propositional calculus expression can be tested
  - `-` time consuming in case of large number of propositions
- complete proof procedures
  - `+` can procedure any expression that logically folllows from a set of experiences
  - inference mechanism <-methods by the conclusion is reached 


`a |= b `meaning:`b` can be derived from `a` by inference: `a/b`

- an interfence rule is sound if the conclusion is true, in all cases where the premises are true
- to prove the soundness the truth table must be constructed with one line for each possible model of the proposition symbols in the premises, in all model where the premise is true, the conclusion must be also true

![proposition calculus truth table](https://leanprover.github.io/logic_and_proof/_static/semantics_of_propositional_logic.4.png)

## intelligent agents
### predictive calculus
```
B=It rained on Firday
will it rain on Monday?
```
- irreducible syntactic elements
- symbols may represent constants *tom* represents Tom. **the *true* and *false* are reserved as truth symbols**
- a fact or proposition is divided into two parts: predicate and argument. The arguments athe object or objecxt of the proposition 

```
Tom owns the car => owns(tom,car)
- owns - predicate
- tom, car - arguments and symbols
```
- variables: represent general classes of objects or poperties
- functions: mapping one or more leemnt of a set (*domain*) to a unique elemnt of another set (*range*)
  - elements of the domain and range are objects in the world of discourse
  - every function symbol has an associated *arity* (number od elements in domain which are used in the function)
- functions can be used within predicates
- atomic sentences


