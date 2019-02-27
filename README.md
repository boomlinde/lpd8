# lpd8

`lpd8` is a program for managing configuration programs for the Akai LPD8 MIDI
controller. It can download and upload configurations from and to the LPD8,
which are represented on the computer as a JSON document.

    Usage: ./lpd8 <program> <device file>
    
    When stdin is a pipe, lpd8 loads a program from stdin
    Otherwise, it writes the current program to stdout.

The JSON representation corresponds obviously to the official Akai editor. The
device file is an OSS style MIDI device file

Example configuration:

    {
      "channel": 1, 
      "knobs": [
        { "cc": 60, "max": 127, "min": 0 }, 
        { "cc": 61, "max": 127, "min": 0 }, 
        { "cc": 62, "max": 127, "min": 0 }, 
        { "cc": 63, "max": 127, "min": 0 }, 
        { "cc": 64, "max": 127, "min": 0 }, 
        { "cc": 65, "max": 127, "min": 0 }, 
        { "cc": 66, "max": 127, "min": 0 }, 
        { "cc": 99, "max": 127, "min": 0 }
      ], 
      "pads": [
        { "cc": 1, "note": 40, "pc": 0, "toggle": false }, 
        { "cc": 2, "note": 41, "pc": 1, "toggle": false }, 
        { "cc": 3, "note": 42, "pc": 2, "toggle": false }, 
        { "cc": 4, "note": 43, "pc": 3, "toggle": false }, 
        { "cc": 5, "note": 36, "pc": 4, "toggle": true }, 
        { "cc": 6, "note": 37, "pc": 5, "toggle": true }, 
        { "cc": 8, "note": 38, "pc": 6, "toggle": true }, 
        { "cc": 9, "note": 39, "pc": 7, "toggle": true }
      ]
    }

## Requirements

Python (2 or 3)
