#                          
							 USER GUIDE
							*************
\page CONTENT

\subpage INTRODUCTION
\subpage PUBLIC FUNCTIONS
\subpage HOW TO START
\subpage SIMPLE PRINT
\subpage ANIMATION
\subpage ANIMATION EFFECTS LIST
\subpage DOUBLE ANIMATION EFFECT

=====================================
\page INTRODUCTION
      ------------
	  CK_MAX is a basic library for 8 digits seven segments module, driven by MAX7219. Written by Chandan kumar mondal. First version released in 28 April 2020.
	  This software combined with two method. One for simple print and another is creating some small effects. 
	  
======================================	  
\page PUBLIC FUNCTIONS
      ----------------
	  1. BCD_Mode()
	  2. Set_Brightness()
	  3. Using_digit()
	  4. SetShutdown()
	  5. DefaultSettings()
	  6. SetPosition()
	  7. ShowMe()
	  8. AnimateMe()
	  9. SetBufferCount()
	 10. AutoRefresh()
	 11. RefreshMe()
	 
======================================
\page HOW TO START
      ------------
	  After Creating object, we can start the display using three ways.
	  Way 1,
	  - Set BCD_Mode (ACTIVE or DEACTIVE)
	  - Set Set_Brightness  (1 TO 14)
	  - Set Using_digit      (0 TO 7)
	  - Set SetShutdown (OFF)
	  
	  Way 2, take a shortcut
	  - Using DefaultSettings
	  
	  Way 3, take a shortcut and then change other stuff
	  - Using DefaultSettings
	  - Change other Stuff
	  
======================================
\page SIMPLE PRINT
      ------------
	  For Set the position use "SetPosition" function.
	  Example...
	  SetPosition(2) (0 is left most digit)
	  
	  For print any data (int, float, double , long , char, string, user defined), we can use "ShowMe" function.
	  Examples...
	  ShowMe(1234) - Print Integer data
	  ShowMe(3.14) - Print Float data
	  ShowMe('C')  - Print Character
	  ShowMe("HE") - Print String
	  ShwoMe(0,0b00011001) - User Defined, where 0 points the position
	 
=====================================
\page ANIMATION
      ----------
	  It also print the data, but in movement and different styles. There are some Animation Effects in this library.
	  There are two types of animation. One is single Effect. Data printed by animation effect and remove for just a blink. And another is Double effect.
	  In this case, Data appearing by one effect and remove by other effect.
	  Single Effect
	  AnimateMe(data, effect's name, effect duration, pause)
	  Example:
	  AnimateMe("HELLO", SCROLL_LEFT, 100, 1000)
	  
=====================================
\page ANIMATION EFFECTS LIST
	  -----------------------
	  
           +----+---------------------------------------------------+
           | ID | EFFECT'S NAME        | CREATION DATE   | VERSION  |
           +----+---------------------------------------------------+
           | 1  | SCROLL_LEFT          | 17 MAY, 2020    |   3.0    |
		   | 2  | SCROLL_RIGHT         | 17 MAY, 2020    |   3.0    |
           | 3  | MAKE_BUFFER          | 18 MAY, 2020    |   3.0    |
    	   | 4  | SCROLL_UP            | 18 MAY, 2020    |   3.0    |
    	   | 5  | SCROLL_DOWN          | 18 MAY, 2020    |   3.0    |
    	   | 6  | RAND_UP              | 18 MAY, 2020    |   3.0    |
    	   | 7  | RAND_DOWN            | 18 MAY, 2020    |   3.0    |
    	   | 8  | SLICE_OWN            | 19 MAY, 2020    |   3.0    |
    	   | 9  | SLICE_ALL            | 19 MAY, 2020    |   3.0    |
    	   | 10 | SCAN_TOP             | 25 MAY, 2020    |   3.1    |
    	   | 11 | SCAN_BOTTOM          | 25 MAY, 2020    |   3.1    |
	       | 12 | WAVE                 | 27 MAY, 2020    |   3.2    |
           | 13 | MAKE                 | 29 MAY, 2020    |   3.2    |
           | 14 | BREAK                | 29 MAY, 2020    |   3.2    |
           | 15 | SCROLL_UP_SINGLE     | 8 JUNE, 2020    |   4.0    |
           | 16 | SCROLL_DOWN_SINGLE   | 8 JUNE, 2020    |   4.0    |
           | 17 | SCROLL_UP_RANDOM     | 8 JUNE, 2020    |   4.0    |
           | 18 | SCROLL_DOWN_RANDOM   | 8 JUNE, 2020    |   4.0    |
		   | 19 | GROW_UP              | 20 JUNE, 2020   |   4.1    |
		   | 20 | GROW_DOWN            | 20 JUNE, 2020   |   4.1    |
		   | 21 | RANDOMIZED           | 01 AUGUST, 2020 |   4.1    |
    	   +----+---------------------------------------------------+
		   
======================================
\page DOUBLE ANIMATION EFFECT
      -----------------------
	  
	  Not only Entry Effect but also Exit Effect.
	  AnimateMe(data, Entry Effect's name, Exit Effect's name, Entry Effect duration, Exit Effect duration, pause)
	  Example:
	  AnimateMe("8 JUNE", SLICE_ALL, MAKE, 100, 200, 2000)

