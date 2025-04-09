# Estimate the valid endings of Tic-Tac-Toe❌⭕
This project uses **«Monte Carlo simulation»** to estimate the number of valid game endings in Tic-Tac-Toe by randomly sampling possible board states.Then we compare and validate the results with different methods.

------------------------------

## Required tools 🛠
In this Project we use **«Python 3, ipython notebook»** and many libraries like **«numpy, pandas, matplotlib, seaborn, itertools»** to speed up.
if you dont have this libraries please install them first!

------------------------------

## Work steps 👨‍💻
1. **Library Imports**: The project begins by importing necessary libraries such as NumPy, Pandas, Matplotlib, and Seaborn for data manipulation and visualization.
2. **Random Board Generation**: A function `make_random_board` is implemented to create random Tic Tac Toe boards.
3. **Winner Check**: A helper function `check_winner` is defined to determine if a player has won based on the current board state.
4. **Board Validation**: The `is_valid_board` function checks if a board configuration is valid according to the rules of Tic Tac Toe.
5. **Monte Carlo Simulation**: The `monte_carlo_simulation` function runs simulations to generate random boards and counts how many of them are valid.
6. **Generating All 5-Move Boards**: The `make_all_5_moves` function generates all possible board configurations with exactly 5 moves (3 X's and 2 O's).
7. **Data Visualization**: Functions for plotting (line plots, bar plots, and violin plots) are created to visualize the results of the simulations.
8. **Results Compilation**: The results from multiple Monte Carlo simulations are compiled into a DataFrame for analysis.

------------------------------

## How to run 🤔⁉
To run this project using Visual Studio Code, follow these steps:

1. **Install Visual Studio Code**: If you haven't installed Visual Studio Code yet, download and install it from the [official website](https://code.visualstudio.com/).
2. **Install the Python Extension**: Open Visual Studio Code and install the Python extension by Microsoft. You can find it in the Extensions view (Ctrl+Shift+X) by searching for "Python".
3. **Install the Jupyter Extension**: Similarly, install the Jupyter extension by Microsoft from the Extensions view. This will allow you to work with Jupyter Notebook files (.ipynb) directly in VS Code.
4. **Open the Jupyter Notebook**: Navigate to the directory where your project files are located. Open the `.ipynb` file (e.g., `Tic-Tac-Toe Simualtion.ipynb`) in Visual Studio Code.
5. **Run the Cells**: Once the notebook is open, you can run the code cells by clicking on the play button (▶️) next to each cell or by selecting a cell and pressing `Shift + Enter`. This will execute the code in that cell and display the output directly below it.
6. **View Results**: After running the simulation cells, you will see the output results printed in the notebook, including the number of valid boards, the ratio of valid boards, and other relevant statistics.
   
------------------------------

## Output results 📋
Upon running the simulation, the following results are displayed:
- **Number of valid boards**: The total count of valid Tic Tac Toe boards generated.
- **Ratio of valid boards**: The percentage of valid boards out of the total generated.
- **Number of valid boards with exactly 5 pieces**: The count of valid boards that contain exactly 5 moves.
- **Total boards with exactly 5 pieces**: The total number of boards generated with exactly 5 moves.

Example output:
Number of valid boards: 1422  
Ratio of valid boards: 28.44% 
Number of valid boards with exactly 5 pieces: 363  
Number of total boards with exactly 5 pieces: 1024 

------------------------------

## Conclusion 🧐
As you can see from the results and code outputs:<br>
out of 5,000 runs, **approximately 27.93% of the total (roughly 1396 cases) were accepted.**
Additionally, among these 5,000 runs, about 1023 cases correspond to states where 5 tokens are placed on the board.
meaning roughly 20.46% of all 5,000 game boards we had-of , which only around 319 are valid.

If we disregard the game rules and simply calculate all possible configurations for a 3×3 board where each cell can be in one of three states (X, O, ' '), we have 9 cells, each with 3 choices.<br>
Thus, the total number of possible states is 3<sup>9</sup> , or equivalently, 19683 distinct configurations.<br>
Now, if we multiply the percentage of valid boards obtained from the above code execution by this total, we conclude that:<br>
1. **There are approximately 5497 valid game states in total.**
2. Among them, roughly 1125 correspond to valid states with 5 tokens on the board.

If you execute the «make_all_5_moves» function, you will observe that the total possible moves for moving 5 tokens (where 3 of them belong to the «X» token and the other 2 moves correspond to the «O» token) equals 1260 .<br>
**With some calculation, we can see that this closely matches our earlier estimate (approximately 89.29% agreement)**.

