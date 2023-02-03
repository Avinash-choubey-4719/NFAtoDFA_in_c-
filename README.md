# NFAtoDFA_in_c-

An NFA can have zero, one or more than one move from a given state on a given input symbol. An NFA can also have NULL moves (moves without input symbol).
On the other hand, DFA has one and only one move from a given state on a given input symbol. 

Steps for converting NFA to DFA:
Step 1: Convert the given NFA to its equivalent transition table
To convert the NFA to its equivalent transition table, we need to list all the states, input symbols, and the transition rules. 
The transition rules are represented in the form of a matrix, where the rows represent the current state, the columns represent the input symbol, 
and the cells represent the next state. 

Step 2: Create the DFA’s start state
The DFA’s start state is the set of all possible starting states in the NFA. This set is called the “epsilon closure” of the NFA’s start state.
The epsilon closure is the set of all states that can be reached from the start state by following epsilon (λ) transitions.

Step 3: Create the DFA’s transition table
The DFA’s transition table is similar to the NFA’s transition table, but instead of individual states, the rows and columns represent sets of states. 
For each input symbol, the corresponding cell in the transition table contains the epsilon closure of the set of states obtained by following the 
transition rules in the NFA’s transition table.


Step 4: Create the DFA’s final states
The DFA’s final states are the sets of states that contain at least one final state from the NFA.

Step 5: Simplify the DFA
The DFA obtained in the previous steps may contain unnecessary states and transitions. To simplify the DFA, we can use the following techniques:

Remove unreachable states: States that cannot be reached from the start state can be removed from the DFA.
Remove dead states: States that cannot lead to a final state can be removed from the DFA.
Merge equivalent states: States that have the same transition rules for all input symbols can be merged into a single state.
Step 6: Repeat steps 3-5 until no further simplification is possible
After simplifying the DFA, we repeat steps 3-5 until no further simplification is possible. The final DFA obtained is the minimized DFA equivalent to the given NFA.
