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
- Define the corrct board in application main.h file:
- Note that the #include "main.h" must be before all #include "TFT_eSPI.h" instructions
-	#define BOARD_PICO_TFT_4KEYS
-	//#define BOARD_TFT_4_QUADCORE_PICO

-Modify User_Setup_Select. at the root of the TFT_eSPI library:

-  . . .
-  ///////////////////////////////////////////////////////
-  //   User configuration selection lines are below    //
-  ///////////////////////////////////////////////////////
  
-  // Only ONE line below should be uncommented to define your setup.  Add extra lines and files as needed.
-	#if TFT_TARGET_BOARD == BOARD_PICO_TFT_4KEYS
-		#include "../T2602_My_TFT_Setups/Setup_PicoConsol_ILI9341.h"
-		//#pragma message("Including: Setup_PicoConsol_ILI9341.h")
-	#elif TFT_TARGET_BOARD == BOARD_TFT_4_QUADCORE_PICO
-		#include "../T2602_My_TFT_Setups/Setup_PicoQuadCore_ILI9488.h"
-		//#pragma message("Including: Setup_PicoConsol_ILI9488.h")
-	#else
-		#pragma message("ERROR!!! No board selected")
-		#include <User_Setup.h>           // Default setup is root library folder
-	#endif

-	
  . . .
