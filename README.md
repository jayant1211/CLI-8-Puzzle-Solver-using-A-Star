# Puzzle Solver using Informed AI - A* Algorithm (CLI Version)

Check Web-Implementation Here: https://github.com/jayant1211/8-Puzzle-Solver-A-Star

This project contains an implementation of the A* algorithm applied to solve the classic 8-Puzzle problem. 

## Features
<ul>
<li><b>Heuristic-driven Optimization:</b> A* intelligently explores possible solutions by considering both the actual cost and a heuristic estimate.

<li><b>Versatility:</b> Solve the 8-Puzzle problem with either numbers or images, showcasing the adaptability of the AI algorithm.

<li><b>Visual Representation:</b> Visualize the steps taken to solve image-based puzzles, with an option to save the intermediate results.
</ul>


### Pre-requisites
<ul>
  <li> Python 3.x</li>
  <li> OpenCV </li>
</ul>

### Installation
<b>1. Clone the repository:</b>
```bash
git clone https://github.com/yourusername/AI-Puzzle-Solver.git
```

<b>2. Navigate to Project Directory:</b>
<br>cd AI-Puzzle-Solver

<b>3. Install dependencies</b>
```bash
pip install opencv-python
```

```bash
pip install numpy
```

### Usage
Run the 'main.py' file:
<be>
```bash
python main.py
```
Select Between Numbered Sliding Puzzle and Sliding Puzzle from an Image. 

If you chose a numbered sliding puzzle, you can input a randomized sequence of number for the 8-Puzzle. 
For eg.
|      |      |      |
|------|------|------|
| 1    | 2    | 3    |
| _    | 4    | 6    |
| 7    | 5    | 8    |

and after providing the input, you will be prompted to provide the goal state, which for this case ideally would be

|      |      |      |
|------|------|------|
| 1    | 2    | 3    |
| 4    | 5    | 6    |
| 7    | 8    | _    |

The A* algorithm combines the actual cost to reach a node (g) and a heuristic estimate of the remaining cost to the goal (h). 

The total cost (f) is given by:
<br> f(x) = g(x) + h(x)

In the context of the 8-Puzzle, the heuristic function 'h(x)' calculates the number of misplaced tiles between the current state and the goal state.

Here is a representation for the working of A* Algo on the numbered puzzle:

<img src="resources/A-star%20working.jpg" width="50%" height="50%"/>

If you select the image puzzle, you will be prompted to provide the path of the image. You can create a jumbled image puzzle by providing a sequence. And by mapping grid to numbers, image problem again becomes a number problem. Below is the eg of Image Puzzle.

## Results
Input & Jumbled Image

<div style="display: flex; flex-direction: row; gap: 30px;">
    <img src="resources/input.png" alt="Jumbled Image" title="Initial Image" width="30%" height="30%"/>
    <img src="resources/jumbled.png" alt="Jumbled Image" title="Jumbled Image" width="30%" height="30%"/>
</div>

**Solving:**

Stage1:

<img src="resources/step1.png" alt="Step 1" height="40%" width="40%"/>
<img src="resources/step1_.png" alt="Step 1 continued" width="30%" height="30%"/>

Stage2:

<img src="resources/step2.png" alt="Step 1" height="30%" width="30%"/>
<img src="resources/step2_.png" alt="Step 1 continued" width="30%" height="30%"/>

Stage3:

<img src="resources/step3.png" alt="Step 1" height="30%" width="30%"/>
<img src="resources/step3_.png" alt="Step 1 continued" width="30%" height="30%"/>

Final:

<img src="resources/step4.png" alt="Final" width="30%" height="30%"/>
