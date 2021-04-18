# Tic-Tac-Toe in C++

An AI plays tic-tac-toe using the **minimax** algorithm with **alpha-beta pruning**.

## Compile

g++ *.cpp -Wall -o TTT

## Run

The players use standard input and output to communicate
The Moves made are shown as unicode-art on std err if the parameter verbose is given

## Play against self in same terminal

mkfifo pipe
./TTT init verbose < pipe | ./TTT > pipe

## Play against self in two different terminals
### Terminal 1:

mkfifo pipe1 pipe2
./TTT init verbose < pipe1 > pipe2

### Terminal 2:
./TTT verbose > pipe1 < pipe2
