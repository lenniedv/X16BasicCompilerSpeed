# Check MO Speed Compiler is actually fast

BASIC v2 that run on the Commander X16 device is interpreter.

I wanted to see how fast the on device interpreter is versus if you compile it with a tool like
MoSpeed (BASIC v2).

The script speed_test.bas do basic math to then output the result to the screen after completion.

# Result

21 vs 9 seconds.

* 21 seconds when running with interpreter.
* 9 seconds with MOSpeed compiler.

# Using latest Commander X16 Release 33 emulator:

https://github.com/commanderx16/x16-emulator/releases/tag/r33

# Compiled using latest MO Speed compiler

https://github.com/EgonOlsen71/basicv2

./mospeed.sh speed_test.bas /target=SPEED.PRG /platform=x16 -generatesrc=true /addressheader=true

# Run

./x16emu -run -prg SPEED.PRG

# Reference:

https://www.c64-wiki.com/wiki/MOSpeed
