# Lander
 A Lunar Lander game for PDP-11 / Tektronix 4014

LANDER runs on a PDP-11/70 / PiDP-11/70 on the RSX-11/M PLUS operating system.

The OS build should include TCP/IP or possibly this will work with a serial connection (untested)

The terminal must be a Tektronix 401x compatible terminal, such as the one at https://github.com/rricharz/Tek4010

The LANDER program is written in FORTRAN-77 and is based on I/O libraries that are included with the MTREK game and are included here as well.

To build LANDER:

    FOR LANDER.FOR

    LINK LANDER,INPOUT,TAQIO,TERMINAL,[1,1]F77FCS/LIB

To run LANDER:

Start the Tektronix 4010 app from the linux command line:

    Tek4010 telnet 192.168.1.105	(or whatever the PDP-11 IP address is)

Log into the user account and launch the program

    RUN LANDER

The program will start in demo mode, press space to start playing the game

Controls (CAPS LOCK should be ON):

	W Increase thrust

	S Decrease thrust

	A Rotate Left

	D Rotate right


You will have up to 3 ships and 200 fuel units

To successfully land, the vertical velocity must be below 2 M/s and horizontal velocity below 1 M/s
