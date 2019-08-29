---
layout: speech
comments: true
mathjax: true
---

### [SPEECH RECOGNITION WITH WEIGHTED FINITE-STATE TRANSDUCERS](../speech.html)

#### Finite Automaton (FA)
A finite automaton is an idealized compute machine used to recognize patterns in input. The input is a symbol set C. The finite automaton either accepts or rejects input.

* An FA has finite number states. 
* It has a special start state and a set of final states (accept/reject). 
* A set of state transitions labeled with symbols in C.

#### Finite State Transducer (FST)
A finite-state transducer is a finite automaton. 
* It's state transitions are labeled with both input and output symbols.
* A path in FST represents a mapping from input symbol sequence to output symbol sequence.

#### Weighted Finite State Transducer (WFST)
A WFST puts weights on state transitions in addition to input and output symbols.
* Weights may encode probabilities, durations or any quantity.
* We compute the overall weight of a mapping from input string to output string along the weights accumulated in the path.

Therefore WSFTs are best way to represent probablistic finite state models prevalent in Speech Recognition.


{% if page.comments %}
{% include disqus.html %}
{% endif %}
{% include mathjax.html %}
