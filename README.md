# Arcade-Game
### Created using Alchitry AU FPGA and Lucid HDL programming

### The idea is to add two hexadecimals and then convert the result into a binary string as many times under 60 seconds.

### [Final design gameplay](https://youtube.com/shorts/iGxqrRCro3M?feature=share)

# The overall design
![alt text](https://github.com/SeanLimHH/Arcade-Game/blob/main/Overall%20Design.jpg?raw=true)

# The output board
![alt text](https://github.com/SeanLimHH/Arcade-Game/blob/main/Output%20Board%20(Screen).jpg?raw=true)

The two squares beside the SCORE is the decimal score of the player; how many expressions he or she computed correctly.

On the other side of the same line are another two squares. It will show two decimal numbers representing the countdown from 60s to 0s

Below it are 3 squares. The two hexadecimal and one operator in the middle is the 3 squares in the middle part of the board

# The input board
![alt text](https://github.com/SeanLimHH/Arcade-Game/blob/main/Input%20Board.jpg?raw=true)

There is one red button to reset the game when the 60 seconds is up.
There are 8 blue buttons. Based on the combination, they represent the corresponding binary string.

For example, if the player presses, from the left, buttons 4, and 8, it will symbolise the binary string of 00010001. This translates to a decimal value of 17.
The idea is to match this decimal value to the result of the expression computed on the output board.

To lock in the results, the player has to press the green button to "confirm" his binary input expression. Then the FPGA will match with the result of the computed value of the expression on the output board. (For 17, b00010001, a valid expression on the output board is B + 6. Which is 11 + 6 = 17. If the green button is pressed, a new expression is generated on the output board and the score increases by 1.)

The three squares beside the green button will display the decimal value of the current binary input expression. This will display regardless of whether the green button is pressed, so that the game is not too difficult for the general public
