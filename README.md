# 2048-Game

2048 is a popular single-player sliding block puzzle game. The objective of the game is to slide numbered tiles on a 4x4 grid to combine them to create a tile with the number 2048. Players can only move tiles in one of four directions - up, down, left, or right - with each move causing a new tile to appear randomly on the grid. The game ends when there are no more moves available or the player reaches the 2048 tile. The game's simplicity and addictive nature have made it a popular mobile app and web game.

## Instructions to run the game

* Open the Github repository where the game code is hosted.

* Click on the green "Code" button and then select "Download ZIP" to download the code as a ZIP file.

* Extract the ZIP file to a folder on your computer.

* Open a command prompt or terminal window and navigate to the folder where you extracted the code.

* Type ```python 2048.py``` and press Enter to start the game.

* Follow the prompts to play the game.

## Functionality of the code

* ```Importing the necessary modules```: The code starts by importing the ```"tkinter" module```, ```"messagebox" from tkinter```, and ```"random"```.

* ```Defining the Board class```: The Board class is defined, which contains various methods for the game's logic. It also has two dictionaries that define the background and text colors for each number tile.

* ```init() method of Board class```: Initializes the game board, creates an empty 4x4 grid of Label widgets using a nested loop, and stores them in the self.board list. It also sets up some variables to keep track of the game's state, such as "compress", "merge", "moved", and "score". The game board is displayed using the grid() method.

* ```reverse() method of Board class```: This method is used to reverse each row of the grid.

* ```transpose() method of Board class```: This method is used to transpose the grid.

* ```compressGrid() method of Board class```: This method compresses the grid by moving all the non-zero elements to the left and setting the empty cells to zero. It also sets the "compress" flag to True if any cell is compressed.

* ```mergeGrid() method of Board class```: This method merges two adjacent cells if they have the same value. It doubles the value of the first cell and sets the value of the second cell to zero. It also updates the "score" and sets the "merge" flag to True if any cells are merged.

* ```random_cell() method of Board class```: This method selects a random empty cell on the grid and places a "2" in it.

* ```can_merge() method of Board class```: This method checks if any adjacent cells can be merged, returning True if they can.

* ```paintGrid() method of Board class```: This method updates the text and background color of each cell in the grid based on its value.

* ```Defining the Game class```: The Game class is defined, which contains the game loop and event handling logic.

* ```init() method of Game class```: Initializes the game and sets the "end" and "won" flags to False.

* ```start() method of Game class```: Starts the game loop by calling the ```"random_cell()"``` method twice and calling ```"paintGrid()"```. It also binds the ```link_keys()``` method to the "<Key>" event.

* ```link_keys() method of Game class```: Handles the game's key events, such as moving the tiles and checking if the game has ended. It calls the appropriate Board class methods to handle the game's logic and updates the game board by calling ```"paintGrid()"```.

