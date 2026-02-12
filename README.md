# T2602_My_TFT_Setups
Setup files for my TFT Implementations

GitHub:  https://github.com/infrapale/T2602_My_TFT_Setups.git



Setup Bodmer TFT_eSPI library
-  Install TFT_eSPI Library in Arduino IDE
-  Open console
-  Change directory to the active libraries folder containing the TFT_eSPI librarie
-  Clone https://github.com/infrapale/T2602_My_TFT_Setups.git
-  The libraries folder should lookk like this
-    libraries
-      T2602_My_TFT_Setups
-      TFT_eSPI


Modify User_Setup_Select. at the root of the TFT_eSPI library:

  . . .
  ///////////////////////////////////////////////////////
  //   User configuration selection lines are below    //
  ///////////////////////////////////////////////////////
  
  // Only ONE line below should be uncommented to define your setup.  Add extra lines and files as needed.
  
  #include "../T2602_My_TFT_Setups/Setup_PicoConsol_ILI9341.h"
  //#include <User_Setup.h>           // Default setup is root library folder
  //#include <User_Setups/Setup1_ILI9341.h>  // Setup file for ESP8266 configured for my ILI9341
  . . .
