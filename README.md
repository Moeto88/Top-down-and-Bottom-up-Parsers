# Top-down-and-Bottom-up-Parsers

Implementing top-down and bottom-up parsers  
  
For the purposes of this exercise assume that a terminal category [smthg] only ever appears in rules of the form x --> [smthg].  
    
### Compilation

g++ -c TDPARSE_hw_start.cpp -o TDPARSE.o  
g++ -c td_tester.cpp  
g++ td_tester.o TDPARSE.o PDA.o rules.o -o td_hw_tester  
　
