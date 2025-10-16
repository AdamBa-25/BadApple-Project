# BadApple-Project

## What is the project about ? 

This project is about a rendering of the video [Bad Apple](https://www.youtube.com/watch?v=FtutLA63Cp8&list=RDFtutLA63Cp8&start_radio=1) on the command prompt.

I am a student in first year of Computer Science and this is a beginner project mostly made during my free time.

## How is it gonna work ?

### Idea N°1 (16/10/2025) :

The idea here is to make a 'fake' rendering on the cmd.

To put it simply, the script is gonna cut the video Bad Apple in frames and analyze each frames.
Each white pixel while be asigned a specific value and the black ones another. Those will then be added into a 2 dimension Array.
The objective is then to consecutively print each array with a clear of the console in between each frames to simulate a screen rendering.

I have absolutely no idea on how to do that, but my first sub-objective is to make a script that will take a 2 dimension array of 0 and 1 and accordingly display a string of this exact array. 

Firstly, I created a class entitled 'BadApple' and included two methods : the main method that is the point entry of the program and a method called 'clearConsole', which will just print out this specific character : "\033[H\033[2J" and also execute this : 'System.out.flush()'

Let's break the character down to understand it fully :

- '\033' is the escape caracter in ASCII that indicate that a control sequence is incoming, which means that the following characters will not be displayed but used as instructions by the terminal prompt.
- '[H' position the cursor in the top-left of the screen (Exact position : 0,0), 'H' stands for 'Home'
- '\033' is the same escape character, another instruction is coming right away.
- '[2J' will clear the entire screen. 'J' stands for 'Erase In Display', the '2' indicates that we want to erase the full screen and not just after the cursor or before.

So this full character is just gonna clear the console and move the cursor to the top left and will be used to create the frame system in our program.

The next command : System.out.flush() will force an immediate display. In other words, it guarantees that the code is executed right away. 

