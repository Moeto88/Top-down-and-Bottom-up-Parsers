# Top-down-and-Bottom-up-Parsers

Implementing top-down and bottom-up parsers

## Top-down parser

For the purposes of this exercise assume that a terminal category [smthg] only ever appears in rules of the form x --> [smthg].  

### Desired behaviour:  

input is the man hit the dog  
WORDS: the man hit the dog  STACK: s   
WORDS: the man hit the dog  STACK: np vp   
WORDS: the man hit the dog  STACK: det n vp   
WORDS: man hit the dog  STACK: n vp   
WORDS: hit the dog  STACK: vp   
WORDS: hit the dog  STACK: tv np   
WORDS: the dog  STACK: np   
WORDS: the dog  STACK: det n   
WORDS: dog  STACK: n   
WORDS:  STACK:   
yep  
  
### Compilation

g++ -c TDPARSE_hw_start.cpp -o TDPARSE.o  
g++ -c td_tester.cpp  
g++ td_tester.o TDPARSE.o PDA.o rules.o -o td_hw_tester  
