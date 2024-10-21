HyScript: a scripting language for ESP32 Arduino C++ to execute stuff without rebuilding the entire codebase. Interpreted by CenterOSKERNELv0
-

Can be used for multiple things: minor changes, OTA-updates, consumer changes.

It works like this: 
The script on the ESP32 reaches to a given RAW http website (github is handy for this) via wifi, 
then we define an array of stuff to do when the esp32 reads that line in the RAW file, that usually looks like this:
{"NEW_COMMAND", handleNewCommand}

The ESP32 then reads NEW_COMMAND in the RAW file and executes handleNewCommand() in the C++ code
