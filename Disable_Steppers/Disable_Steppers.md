# Disable_Steppers Macro
This macro allows you to disables the steppers when not using the printer.

To use this marco to your printer follow below steps:
1. Open up ratos.local/ in your browser (Mainsail).
2. Navigate to the Machine tab.
3. Open up your Printer.cfg.
4. Navigate down to the User Overrides.
5. Add the code from the Disable_Steppers.cfg.
6. Save+Restart your printer.

After following above steps you should see a "Disable_Steppers" be added to the Macros list on the Dashboard of Mainsail.
When pressed the macro will send a M80 gcode command to disable the stepper drivers.