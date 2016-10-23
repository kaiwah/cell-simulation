**Cell Automata** Simulator/Game
==================================

A coding assignment to create a cellular automata program. 

Entire logic is coded in a JS class object and listens to the "Right Arrow" button to move on to the next generation.

#Cellular Conditions:#

  * Cells have one of two states: alive or dead
  * Cells are laid out in a rectangular grid where edges wrap around
  * Each cell has exactly 8 neighbors. (i.e. Every cell directly next to the origin cell is a "neighbor")
  * For the next generation:
  	* A dead cell that has exactly 3 living neighbors will become alive again
  	* A living cell that has exactly 2 or 3 living neighbors will stay alive, otherwise it will die

#Application Features:#

  * The board has 3 board modes:
		* Blinker
		* Glider
		* Flower
	* Whenever neighbors are searched, it will blink blue
	* Simulation was coded in a Object-Oriented design pattern to allow for segmentation/modularity
	* Two different calculation methods for finding neighbors are included both O(1) time complexity

#Known Issues:#

  * When the maximum rows and columns exceed a certain amount, the application will lag due to the amount of DOM rendering

#Possible Improvements:#

In order to combat against the rendering lag issues, instead of using DOM elements to represent each "cell", we can create nodes to represent each cell and assign it a virtual position. 

The virtual position is then rendered via absolute positioning. Thus we do not need to render each "cell" block, only the alive cells.