Allegro YACE
============
Allegro YACE is a front end for YACE (Yet Another Chip8 Emulator) written in C++ using Allegro 5.

Usage
-----
###Running
To run Allegro YACE, type the following command in a terminal\\command line (inside of the Allegro YACE directory):
`yace [<game>] [<configuration-file>]`

`[<game>]` - The Chip8 game to run. **(Optional)**  
`[<configuration-file>]` - The configuration file to use. **(Optional)**

The easiest way to run Allegro YACE is simply by typing `yace` or double-clicking the executable.

###Keys
`ESCAPE - Exit Allegro YACE`  
`F1 - Load game`  
`F2 - Toggle timer on/off`  
`F3 - Step emulation (Only if the timer is stopped)`

###Configurations
In the configuration file it's possible to change key-bindings (and soon BG-/FG-color). It's possible to have several configuration files, however, only one can be used at a time.

The default configuration has the following key layout:
<p><img src="http://i41.tinypic.com/2dlj0d1.png" alt="Key layout" /></p>

Compiling
---------
###Requirements
* [YACE Back end](https://github.com/Johoel/YACE)
* Allegro 5.0.4 (or greater)

**The file hierarchy should look something like this with the YACE back end in place.**  
<ul>
<li>Allegro YACE/</li> 
<ul><li>include/</li></ul>
<ul><li>src/</li></ul>  
<ul>
<li>YACE/</li>
<ul>
<li>include/</li>  
<li>src/</li>
</ul>
</ul>
</ul>

###Compiling
There's a *makefile* provided with Allegro YACE. It's very basic and doesn't allow for adding new source files without having to add them manually into the makefile. Follow these steps to compile Allegro YACE:

1. Open a terminal\\command line
2. Change directory to the Allegro YACE directory.
3.  * To compile Allegro YACE **without** debugging enabled, simply write                 
    `make ALLEGRO_PATH=<path-to-allegro>`

    The output file will be named *yace*.

    * To compile Allegro YACE **with** debugging enabled, simply write
    `make debug ALLEGRO_PATH=<path-to-allegro>`
    
    The output file will be named *yace-debug*.

Example 1 - Compiling **without** debugging:

`make ALLEGRO_PATH="C:\allegro-5.0.4"`

**(Note: Don't put a front-/backslash at the end of the path.)**

To-Do list
----------
+ Improve event handling (like keyboard input)
+ Add sound support
+ Add possibility to set user-defined colors in configuration file (default is White BG & Black FG).
