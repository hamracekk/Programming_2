# Programming_2

Tasks:

Two Beast in a Labyrinth
King's path on a chessboard
Sokoban (storekeeper)
Alphabet
Water transfer
King's path on a chessboard (length)

Two Beast in a Labyrinth:

    Two beasts are in a labyrinth. The labyrinth is represented as a matrix of individual positions. At any moment, the beast is at one particular position and is         turned in one of four possible directions (up, down, left and right).

    In each round every beast makes one move. The possible moves are: TurnLeft, TurnRight, MakeStep (one step forward). At the beginning, the beast has a wall to its       right. As the beast moves it tries to follow this wall (see the example below).

    The input of the program contains a width and height followed by a map of the labyrinth. Individual characters depict individual positions in the labyrinth: 'X' is     a wall and '.' is an empty spot. The characters '^', '>', 'v' and '<' depict the beast turned upward, to the right, downward and to the left, respectively.

    Your program should read the input and then move the beasts 20 times. After each move it should print a map of the labyrinth in the same form in which it read it.     Write an empty line after each map.

    Beware: The first output is performed after the first move of the beasts.

    Example:

    Input (there will actually be no leading spaces; they are present here only for aesthetic reasons):

                    10
                    6
                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.Xv.X.X.X
                    X.X.>..X.X
                    XXXXXXXXXX
                    
    Ouput (the same remark on leading spaces):

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X.X.X
                    X.Xv.>.X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X.X.X
                    X.X>..>X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X.X.X
                    X.X.>.^X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X^X.X
                    X.X..>.X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X^..X
                    X.X..X.X.X
                    X.X...>X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X>..X
                    X.X..X.X.X
                    X.X...^X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X.>.X
                    X.X..X^X.X
                    X.X....X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X^.>X
                    X.X..X.X.X
                    X.X....X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X>.vX
                    X.X..X.X.X
                    X.X....X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X.>.X
                    X.X..X.XvX
                    X.X....X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X..>X
                    X.X..X.X.X
                    X.X....XvX
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X..vX
                    X.X..X.X.X
                    X.X....X>X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X.XvX
                    X.X....X^X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X.X>X
                    X.X....X<X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X...X
                    X.X..X.X^X
                    X.X....XvX
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X...X
                    X....X..^X
                    X.X..X.X.X
                    X.X....X>X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X..^X
                    X....X...X
                    X.X..X.X.X
                    X.X....X^X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X..<X
                    X....X...X
                    X.X..X.X^X
                    X.X....X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X.<.X
                    X....X..^X
                    X.X..X.X.X
                    X.X....X.X
                    XXXXXXXXXX

                    XXXXXXXXXX
                    X....X<.^X
                    X....X...X
                    X.X..X.X.X
                    X.X....X.X
                    XXXXXXXXXX

King's path on a chessboard:

    Write a program finding a shortest path with a chess king on a chessboard 8x8 where several squares cannot be accessed (by the king).

    Input is given in this ordering:

    Number of obstacles
    Coordinates of the obstacles (pairs of numbers 1.. 8)
    Coordinates of the starting square
    Coordinates of the end square.
    Number of the obstacles is on a separate line, obstacles are described each on a separate line (i.e., one pair of numbers on a line). On a line the numbers are         separated by the space-character.

    Output is either -1 (if the king cannot reach the end-square) or the list of coordinates of all the squares of the path, from starting to ending square. If there       exist more paths of the same length, print any of them.

    _Sample input:_
      1
      2 1
      1 1
      3 3

    _Appropriate output:_
      1 1
      2 2
      3 3
      
Sokoban (storekeeper):

    In a warehouse of size 10 x 10 squares, a storekeeper at position [sx,sy] needs to move a box at position [bx,by] to the destination [cx,cy]. The warehouse is         surrounded by walls, and there may be additional walls at several positions inside the warehouse.

    In each step, the storekeeper moves one position up, down, or to the left or right. If the box is in front of him (in the direction of movement) and there is an       empty space behind it, the storekeeper pushes the box into the empty space and moves into the position where the box was. If the square where he wants to move         contains a wall (including the edge of the warehouse), or if it contains the box and there is a wall behind it, then the storekeeper cannot move in that direction.

    Write a program that determines the minimum number of steps needed to move the box to its destination square. If it is not possible to move the box to that square,     write the value -1.

    Input format:

    The input is presented as a map containing the following symbols:

    . (period) indicates an empty square
    X indicates a wall
    S indicates the storekeeper
    B indicates the box
    C indicates the destination square
    Example:

    Input:
    ..........
    ..........
    ..........
    ..........
    ..........
    CSB.......
    ..........
    ..........
    ..........
    ..........
    
    Corresponding output:
    6
    
Alphabet:

    Some electronic devices allow text entry using a grid of letters. The grid contains a movable cursor, which begins in the upper-left hand corner. The arrow keys       move the cursor up, down, left and right. The Enter key chooses the letter under the cursor.

    For example, if the input grid looks like this:

    ABCDEFGH
    IJKLMNOP
    QRSTUVWX
    YZ
    we can enter the text "HELLO" with the following sequence of keys (which is only one of many possible sequences):

    right
    right
    right
    right
    right
    right
    right
    Enter
    left
    left
    left
    Enter
    down
    left
    Enter
    Enter
    right
    right
    right
    Enter
    
    Write a program which for a given grid (which may contain both lowercase and uppercase letters) and text (which may also contain non-alphabetic characters)             determines and writes out the minimum number of keystrokes required to enter the given text.

    Caution: Each letter may appear more than once in the grid!

    The input begins with numbers indicating the width and height of the grid (each on its own line).
    A single line follows containing the contents of the entire grid (in row major order, i.e. with one row after another).
    The rest of lines contain the text to be entered. ! You should ignore any characters in the text that are not present in the grid.

    Example:

    Input:
    3  
    3  
    ABCBFECDF  
    ABCDEFA
    
    Output:
    15
    
    Comment:
    In this example, the grid has the form:
    ABC
    BFE
    CDF
    
    It is possible to enter the text ABCDEFA in many possible ways; 15 keystrokes is the length of the shortest of these.
    
Water transfer:

    Let us have three cups of integer sizes a, b, c (a, b, c not greater than 10) containg at the beginning x, y, z of water, respectively.

    We can transfer the water from one cup to other until the cup to is full or the cup from is empty.

    It is not possible to throw the water out as well as take water from some external source.

    Input of the program are numbers a, b, c, x, y, z giving the sizes and starting volumes of cups.

    Program will print the list of all volumes (including zero, if possibble) obtainable by transfers (the whole volume must be containded in one cup) and for each of     those volumes it prints ":" (colon) and minimal number of transfers needed. Volumes would be printed in ascending order.

    Example:

    Input:
      4 1 1  1 1 1
      
    Output:
      0:1 1:0 2:1 3:2

King's path on a chessboard (length):

    Write a program finding a shortest path with a chess king on a chessboard 8x8 where several squares cannot be accessed (by the king).

    Input is given in this ordering:

    Number of obstacles
    Coordinates of the obstacles (pairs of numbers 1.. 8)
    Coordinates of the starting square
    Coordinates of the end square.
    Number of the obstacles is on a separate line, obstacles are described each on a separate line (i.e., one pair of numbers on a line). On a line the numbers are         separated by the space-character.

    Output is either -1 (if the king cannot reach the end-square) or number of steps that the king has to perform.

    _Sample input:_
      1
      2 1
      1 1
      2 2


    _Appropriate output:_
      1
