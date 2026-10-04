# Matthew Sychareun NFA Design Exercise 1
## Summary of my learning

## 1. Which problems gave me the most trouble?

**Problem 8: starts with 01 and ends with 10**

I think this one was probably one of the harder questions I did out of the five I chose. I think what made it hard was how these two patterns can overlap. An example of this is input `010` because the middle `1` is both the end of '01' and the start of `10`. 

Another problem I had trouble with was **Problem 11: the 2nd to last bit is 1.**

I think what made this tricky was how the NFA for this only has 3 states compared to the DFA which has 4 states. Since this has less states than the DFA version, I had to undestand that it guesses as when it reads a `1`, it does not know whether this is the second to last symbol.

**Did I avoid any problem because it was too hard?**

No, I did not avoid any problem because it was too hard. I decided to do the all the problems on my own as practice to get used to drawing both DFA and NFA to prepare myself for the midterm and finals and to also help me undestand NFAs and DFAs better.

**Did I ask questions to AI / the instructor?**

Yes, I used Claude to help me out. The way I used Claude is that I would first design my NFAs on JFLAP and ask it to give me test inputs of accepted and rejected inputs to check if what I designed satisfies these tests. If my designs did not meet these tests, I would ask Claude to check my work and give me advice on what I can do to fix it, but I made sure to have Claude no`t give me the answer or draw it themselves so that I can fix the mistake myself. 

## 2. Which next states did I not account for in the subset of next states?

When I initially drew **problem 8**, the middle state `q2` only had a self-loop on `1` and was missing the transition on `0`. So if it were to read an input like `01010`, after reading `01` the NFA is in the set `{q2, q3}`. Reading a `0` from that set should give `{q2, q4}`, but since my `q2` had no `0` transition, the `q2` branch died and the set became `{q4}` only. 

I missed this because I was only testing inputs like `0110`, `010`, and `01110`, where the middle contains only 1s, which made me forget to see if input had a 0 in the middle.

Something I can do to avoid this mistake in the future is to **write the transition table first** so that I can have a table for every state and every symbol, list the full set of next states, including the empty set on purpose. Another thing I can do is **give every loop the right label**, meaning if a part of the language means "any symbol", in this case the middle, the loop needs all symbols in the alphabet. 

**3. Other insights, comments and questions**

An insight that I had was knowing **when the NFA and DFA look the same**. From what I learned doing this and also asking Claude for clarification, when the NFA has no real choice points, then the DFA is the NFA plus the dead state for any missing transition. Another insight I got was the **complement works on DFAs, not NFAs**. To get something like "does not contain 10", you are able to buidl a complete DFA and flip the accepting states, however, flipping an NFA's accepting states does not complement the lanugae.

A question I have is for the midterms/exams, will there be test inputs we can use to check if our NFAs/DFAs are correct and if we will need to draw the transition tables and tree computations? Also if a NFA and DFA are drawn the same and there is a question that asks for both, do we need to draw both of them and label them or can we just draw one and say 'NFA and DFA are the same.'
