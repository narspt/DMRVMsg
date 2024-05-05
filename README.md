# DMRVMsg - DMR Voice Message Recorder
This software connects to a DMR "master" (using MMDVM protocol) and records all received private call or group call voice messages, playing back a confirmation message to the user. Streams are decode using an AMBEServer and will be saved in .WAV files.

# Build
Main program is a single C file, no makefile is required. To build, simply run gcc:
```
gcc -o dmrvmsg dmrvmsg.c
```

# Usage
```
./dmrvmsg [CALLSIGN] [DMRID] [DMRHostIP:PORT:TG:PW] [AMBEServerIP:PORT] [SavePath]
```
If you wish the program to record only private call messages, you can set TG to 0 to prevent connecting a TG or even set it to 4000 to ensure any dynamic TG's are dropped.
