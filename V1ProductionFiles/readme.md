This folder contains the production gerber for the limited run of the first version of the Battreus44.
Only 6 were made in total.
Position of the switches isn't MX spaced nor Choc Spaced.
Only choc-spaced keycaps will work.

This is for future reference in case the owner of one of the 6 that were made want to make a 3D printed case.
The gerber file is what was sent for production.
The PCB file was re-created from the Gerber File
The Edge Cuts DXF file was created using a plot of the PCB file - only the edge cut was exported.

Unlike the V2, the V1 uses more columns and has gaps in the key matrix.
This code snippet should help out for the rows and columns:


``` python
keys = keypad.KeyMatrix(
    row_pins=( board.P0_28, board.P1_11, board.P0_10, board.P1_06,),
    column_pins=(board.P0_15, board.P0_17, board.P0_20, board.P0_13,  board.P0_24,
                 board.P0_09, board.P0_03, board.P1_13,  board.P0_02, board.P0_29, board.P0_26,  board.P0_30),
    columns_to_anodes=True,
)
```

GPIOs are that of the [BlueMicro840](http://nrf52.jpconstantineau.com/docs/bluemicro840_v1)
