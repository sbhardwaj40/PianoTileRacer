# PianoTileRacer

#### Team Members: Sheel Bhardwaj, Alan Ko

Want to play Piano Tiles but don't have a smartphone? Our project is an mbed rendition of the popular mobile game Piano Tiles. Points are gained for every correct tile pressed on the touhcpad, and each correct note is outputted to the speaker. There are different game modes that increase in intensity and time duration, as well as a wide array of musical pieces to choose from. High scores for each intensity are stored to a micro SD card and can always be viewed. With that, good luck and aim for the highest score!

## Setup

### Key Components
- mbed NXP LPC1768
- MPR121 I2C Capacitive Touch Sensor
- uLCD-144-G2 128 by 128 Smart Color LCD
- microSD Transflash Breakout Board and microSD card
- Class D Audio Amplifier breakout board and speaker

### Pinnout Connections
Below are tables representing the pinnout connections between all the parts involved in the game. For some parts, the pinnouts can be altered, but it should be noted that the same pinnouts are used in the code, so they will need to be changed also. Examples of situations where pins may be altered are when a new user wants to add a functionality or a new piece of hardware to the setup.

## Usage
Piano Tile Racer is programmed entirely in C++ and makes use of various mbed libraries to utliize multithreading to operate multiple pieces of hardware and other internal functionalites at the same time. In order to run the game, the source code simply needs to be imported to the online mbed compiler, compiled, and pushed to the mbed itself. The mbed website can be found at (https://os.mbed.com/). A new user will have to:

1. Make an account
2. Navigate to the compiler tab
3. Upload the game code as a new project
4. Compile the main.cpp file
5. Move the executable file to the user's own mbed setup



