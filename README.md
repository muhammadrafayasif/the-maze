# The Maze
**Programming Fundamentals (PF) Semester Project (CT-24141) - NEDUET - CSIT**

The Maze is a basic game where you start off at the entrance of the maze, your goal is to reach the end of the maze where there is an opening available.

![Title Screen](https://lh3.googleusercontent.com/pw/AP1GczMaFq15M4EpsdPWMiXm71oE9pa4TcDpOMTLp4rO8fXoLcfY9wBpvzwTvmwxDCq9t0zHCENTpqVAjBZe3aF0OA81_4gzzLVPak7KbkaF6KnWQiDHWXZdyL8NzqmPJoad5VKYh3cYbAoPz4EAAEY2qsG5=w657-h295-s-no?authuser=0)
![Image of The Maze](https://lh3.googleusercontent.com/pw/AP1GczPQHyrk0L8cSF5Y-1k-XnN2eQc9VYvW_uH1WP7I2zVyVG89HCNWE2KTXuLeE4dqRJ70j4SS_BCRjqx666Eg3EL7U7nys_2fSp9TrZR6R0hdlACwd5PNPJOCOJ8iQSM3wN-5XSLfaVUccSj9ySNduSEL=w304-h378-s-no?authuser=0)
# Controls
* WASD
* Arrow Keys

Use can use both the WASD and the Arrow Keys to move the character, the character cannot move through walls.

The entire game is playable with just these keys, with the exception of the main screen, which allows any key to be pressed to begin.

# Functionality
The maze utilizes the use of a **Two-dimensional array**, the two dimensional array is used to draw the maze onto the screen, furthermore, it also tracks the movement of the player, so that it is unable to phase through walls.

The program also uses ASCII codes like
|ASCII| Function |
|--|--|
| \033[?25l | Hides the cursor highlighting |
| \033[col;rowH | Points cursor to specific row and column
| \033[?25h | Reactivates cursor highlighting

> These ASCII codes may not work on every system, as the application is specifically targeted towards Windows systems and is meant to run on the terminal.

Since these ASCII values directly alter the players position by erasing the players character and drawing it to the next position based on user input, the maze is only drawn once. This prevents the jittery effect that occurs when constantly refreshing the screen, so the movement appears smooth.

# Drawbacks
* Since the program directly tracks the X and Y coordinates of the terminal, it is dependent upon it, therefore resizing the window of the terminal may cause unexpected issues on the player position being drawn.

# Dependencies
* Standard Input/Output **(stdio.h)**
* Console Input/Output **(conio.h)**
* Standard Boolean **(stdbool.h)**
* Standard Library **(stdlib.h)**
