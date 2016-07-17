# campbell-scientific-CSAT3-data-acquisition-labview
Communicates with the CSAT3.  Stores and processes 3D wind speeds.

Known issues.

The CSAT3 requires a true RS-232 connection in order to properly work.  It only turns on its serial drivers when the RTS
line is asserted and kept high.  If using with USB (which is fairly unavoidable these days), I recommend getting a quality
USB-to-RS232 adapter.

The CSAT3 should be set up to send the synchronization code.  The instructions for setting it up to do so are as follows:

To send synchronization code and save this setting to non-volatile memory, follow the steps described below.  
Commands are given in quotes.  The quotes  are not to be entered.  Commands are ended by pressing the Return key.

1.   Remove power from CSAT3's white electronics box.
2.   Place the electronics box with four military-type connectors facing
     toward you.
3.   Remove the lid.
4.   Locate a jumper above the upper-left corner of the black, square,
     surface-mount chip with the white label on it.
5.   The current jumper position should be center-right.
6.   Move the jumper to left-center position.
7.   Apply power to CSAT3.
8.   Using the Campbell Scientific CSAT3 terminal program, press the Return
     key until you get the > prompt.
9.   Type the "rs 1" command to enable synchronization code output.  First
     enter "rs 1" (without the quotes) and then hit Return.
10.  Enter the "&" command for unprompted data output mode.
11.  Type "??" to get status.
12.  Look for rs=1 and &=1 or &=0 from the returned status message.
13.  Verify that rs=1 and &=1.
14.  Upon verification, type "sr2718" to save this setting to non-volatile
     memory.
15.  If you get "LD1ok, LD2ok" back, all is well.  If not, return to step 9.
16.  Power off CSAT3.
17.  Move the jumper back to center-right position.
18.  Power CSAT3 back on.
19.  Type "??" and verify that rs=1 and  &=1.
20.  Reattach case lid.
