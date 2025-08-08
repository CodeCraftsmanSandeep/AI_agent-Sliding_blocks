# AI Agent: Sliding Blocks Solver

Welcome to the **Sliding Blocks Solver**! 🧩
This project brings together **classic puzzle fun** and **artificial intelligence**. Watch as an AI agent uses the **A\*** search algorithm to crack the 3×3 sliding blocks puzzle, step by step, finding the optimal path to victory.

Whether you’re here to explore **AI search algorithms**, learn about **heuristics**, or just see a puzzle get solved intelligently, you’re in the right place!

## Overview  

This project genereates sliding blocks, and then builds AI agent solver. The AI agent solves the **Sliding Blocks Puzzle** using the **A\*** search algorithm. The puzzle consists of a 3×3 grid with numbered blocks (0–8), where **0 represents the empty space**. The goal is to rearrange the blocks from a given initial configuration into the standard goal configuration by swapping the empty space with adjacent blocks.  



### Goal Configuration:  

```
1 2 3  
4 5 6  
7 8 0  
```

### Example Initial Configuration:  

```
1 2 3  
7 8 5  
0 6 4  
```

## Implementation  

The agent uses **A\*** search with different heuristics to find the optimal path to the goal state.  

### Heuristics Used:  

1. **Manhattan Distance Heuristic (h₁)**:  
   - The sum of Manhattan distances of all misplaced blocks from their goal positions.  
   - Formula:  
     \[
     d_{Manhattan} = |x_1 - x_2| + |y_1 - y_2|
     \]
   - **Performance: Best**  

2. **Misplaced Blocks Heuristic (h₂)**:  
   - The count of blocks that are not in their correct positions.  
   - **Performance: Moderate**  

3. **Zero-Block Manhattan Distance Heuristic (h₃)**:  
   - Only considers the Manhattan distance of the **empty block (0)** instead of all blocks.  
   - **Performance: Worst**  

## How It Works  

1. **A\*** Search Algorithm is applied to explore the state space.  
2. The heuristic function evaluates the cost of moving to each possible new state.  
3. The algorithm selects the move with the lowest estimated cost to the goal.  
4. The process repeats until the goal configuration is reached.  
5. The program prints:  
   - The total number of steps taken.  
   - The blocks' configuration at each step.  
   - The number of states explored for performance comparison.  

## Performance Comparison  

| Heuristic | Order of Explored Nodes | Performance Ranking |  
|-----------|-------------------------|----------------------|  
| Manhattan Distance (h₁) | Least | **Best** |  
| Misplaced Blocks (h₂) | Moderate | Medium |  
| Zero-Block Manhattan Distance (h₃) | Most | **Worst** |  

## Contributions  

Feel free to contribute by optimizing the search algorithm or adding new heuristics. Fork the repository and submit a pull request!  
