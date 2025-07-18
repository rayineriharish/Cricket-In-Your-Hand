Cricket in Your Hand: An Embedded Virtual Game Using LPC2138

Project Overview
Cricket in Your Hand is a microcontroller-based cricket simulation game that offers interactive gameplay by allowing users to participate as batsmen against a virtual bowler with randomness and real-time feedback. The game simulates essential cricket match aspects: runs, overs, wickets, game modes (T20, ODI, Test), and delivers feedback through an LCD, LEDs, a buzzer, and a speaker.

Features
Multiple Game Modes: Choose between T20, ODI, and Test matches, each with unique overs, wickets, and time limits.

User Interaction: Input runs per ball using a matrix keypad.

Real-Time Feedback: LCD displays scores, current over/ball, and player status.

Visual and Audio Feedback: LEDs, buzzer, and speaker highlight events like wickets, sixes, half-centuries, and centuries.

Randomized Gameplay: Utilizes Timer0 for system random number generation, lending unpredictability to the simulation.

Milestone Recognition: Celebrates milestones (50, 100 runs) with distinct sound patterns.

Components Required
Microcontroller: LPC214x (based on ARM7)

Input: 4x3 Matrix Keypad

Display: 16x2 or 20x4 LCD

Indicators: LEDs (Green, Red), Buzzer, Speaker

Passive Parts: 220Ω & 10kΩ resistors, 100nF capacitors, breadboard, jumper wires

Supply & Clock: 5V power supply, 12MHz or 16MHz crystal oscillator

How It Works
Startup: The user selects a game mode (T20, ODI, Test) using the keypad.

Gameplay Loop: For each ball in every over:

The system generates a random score for the bowler.

The user inputs a score (runs) via the keypad.

If the user's score matches the system's, a wicket is taken.

Scoring a six triggers a green LED and sound.

LEDs, buzzer, and speaker respond to milestones and wickets.

The LCD provides live updates after every ball.

Game End: The match ends after overs or wickets are exhausted, or time runs out, displaying the final score and wickets.

Software Highlights
Peripherals: Extensive use of LPC214x GPIO, Timer0 (for randomness and time), PWM (sound), and UART (optional, for debugging or expansions).

Game Logic: Easily modifiable C code with well-documented functions for handling user input, scoring, timeouts, hardware feedback, and game state management.

Getting Started
Hardware Setup

Connect components (LCD, keypad, LEDs, buzzer, speaker) to the LPC214x per provided port mappings.

Ensure proper pull-up/pull-down resistors and stable power supply.

Use a crystal oscillator to match project timing requirements.

Software

Flash the main.c code onto LPC214x using a supported toolchain.

Review and tune pin definitions and timing constants if adapting to different setups.

Gameplay

Use keypad to select game mode and enter runs.

Watch scores and feedback on LCD and listen for buzzers/speaker for milestones.
