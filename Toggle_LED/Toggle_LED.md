# Toggle_LED Macro
This macro allows you to control a PWM-LED connected to your printer mainboard.

To use this marco to your printer follow below steps:
1. Install a PWM-LED to a PWM capable pin on your printer mainboard.
2. Open up ratos.local/ in your browser (Mainsail).
3. Navigate to the Machine tab.
4. Open up your Printer.cfg.
5. Navigate down to the User Overrides.
6. Add the code from the Toggle_LED.cfg.
7. Change "PD15" to match your PWM pin, refer to your mainboard pinout document for the correct name/number.
8. Save+Restart your printer.

After following above steps you should see a "Toggle_LED" be added to the Macros list on the Dashboard of Mainsail.
When pressed the macro will check the current state of the LED (On/Off) and switch it to the oposite.
Alternatively you can press the down arrow at the end of the macro to set the brightness of the LED.
Brightness is a float with a range from 0 to 1.
To st the LED to 50% brightness for example set it to 0.5.
