# PianoTileRacer

#### Team Members: Sheel Bhardwaj, Alan Ko

Want to play Piano Tiles but don't have a smartphone? Our project is an mbed rendition of the popular mobile game Piano Tiles. Points are gained for every correct tile pressed on the touhcpad, and each correct note is outputted to the speaker. There are different game modes that increase in intensity and time duration, as well as a wide array of musical pieces to choose from. High scores for each intensity are stored to a micro SD card and can always be viewed. With that, good luck and aim for the highest score!

## Setup

### Key Components
- mbed NXP LPC1768
- MPR121 I2C Capacitive Touch Sensor
- uLCD-144-G2 128 by 128 Smart Color LCD
- microSD Transflash Breakout Board and microSD card
- TPA2005D1 Class D Audio Amplifier breakout board and speaker

### Pinnout Connections
Below are tables representing the pinnout connections between all the parts involved in the game. For some parts, the pinnouts can be altered, but it should be noted that the same pinnouts are used in the code, so they will need to be changed also. Examples of situations where pins may be altered are when a new user wants to add a functionality or a new piece of hardware to the setup.

mbed to MPR121 I2C Capacitive Touch Sensor

![mbed_touchpad_pinnoutTable](https://user-images.githubusercontent.com/57376146/117066187-6e749b00-acf6-11eb-8f09-6559eb02f05b.png)

mbed to Class D Audio Amp and Speaker

![mbed_classDamp_speaker_pinnoutTable](https://user-images.githubusercontent.com/57376146/117066308-9532d180-acf6-11eb-8163-fb497741c6b9.png)

mbed to uLCD Display

![mbed_ulcd_pinnoutTable](https://user-images.githubusercontent.com/57376146/117066345-9ebc3980-acf6-11eb-9bea-c95c548b216a.png)

Setup Overview

![mbedSetup_overview](https://user-images.githubusercontent.com/57376146/117066604-efcc2d80-acf6-11eb-9544-116750e759bc.jpg)


## Usage
Piano Tile Racer is programmed entirely in C++ and makes use of various mbed libraries to utliize multithreading to operate multiple pieces of hardware and other internal functionalites at the same time. The libraries used in this project are not the most updated for some parts because only specific libaries work in conjunction for all the parts. Some newer libaries do not have support for all the hardware being utitlized in terms of threading protection, etc. In order to run the game with a working setup as outlined in the earlier section, a user needs to:

1. Make an account if not done so already on the online mbed page https://os.mbed.com/
2. Once the user has an account, follow this link (https://os.mbed.com/users/alanjko9/code/Piano_Tile_Racer/) to a public repository on the mbed page with the Piano Tile Racer source code
3. Import the project to the user's own online mbed code compiler
4. Compile the main.cpp file
5. Move the created executable file to the user's own mbed setup
6. Once file is loaded into the mbed, press the mbed hard reset button
7. Finally, press 11 on the touchpad to launch the game
8. Enjoy!

## Features

### Main Menu Screen
![mainmenu](https://user-images.githubusercontent.com/57376146/117071272-e2b23d00-acfc-11eb-8de3-926d9607d2bf.jpg)

Once the game is launched, the main menu will pop up with options to start the game (0 key on touchpad), change the song (1 key on touchpad), change the game time limit duration (2 key on touchpad), or view high scores (3 key on touchpad). The main menu will also display the selected game duration and whether sound is on or off.

### Song Selection Screen
![songSelectionMenu](https://user-images.githubusercontent.com/57376146/117071313-f362b300-acfc-11eb-8455-b5ee6da30fa4.jpg)

The Song Selection Screen uses the touchpad to allow the user to either return to main menu, turn off music, or select a song.

### Game Duration Selection Screen
![gameDurationMenu](https://user-images.githubusercontent.com/57376146/117071516-36bd2180-acfd-11eb-9720-87b74b495f95.jpg)

The Game Duration Screen uses the touchpad to allow the user to return to the main menu or change the game duration between 15 seconds to 120 seconds.

### View Highscore Screen
![highscores](https://user-images.githubusercontent.com/57376146/117071665-610edf00-acfd-11eb-8113-6d96018e4d67.jpg)

The View Highscore Screen shows the top five scores for each game duration. The user presses 1 on the touchpad to toggle through the different game durations and 0 on the touchpad to return to the main menu screen.

### Gameplay
![gameplay](https://user-images.githubusercontent.com/57376146/117071915-b8ad4a80-acfd-11eb-8cbc-566d4b194188.jpg)\

Four rows of black piano tiles are randomly generated and displayed on the LCD screen. The player advances in the game by pressing the correct corresponding touchpad key (0 - 3) to the piano tile shown on the bottom row. A countdown timer and the player's current score are shown on the right side of the screen. The game ends when the timer reaches 0 or a player presses an incorrect key. 

## Project Features and Gameplay Demo
https://www.youtube.com/watch?v=elqrJ6IbV74&authuser=0
