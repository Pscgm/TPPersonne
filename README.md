# TPPersonne
TP 4

Appels systeme donnat la date :

#include <time.h>

........

  // calcul de la date locale    
  //struct tm :
  /*
   int tm_sec;    // Seconds after the minute - [0,59]
   int tm_min;    // Minutes after the hour - [0,59]
   int tm_hour;   // Hours since midnight - [0,23]
   int tm_mday;   // Day of the month - [1,31]
   int tm_mon;    // Months since January - [0,11]
   int tm_year;   // Years since 1900
   int tm_wday;   // Days since Sunday - [0,6]
   int tm_yday;   // Days since January 1 - [0,365]
   int tm_isdst;  // Daylight-saving-time flag
*/
  
......
  struct tm *aujourdhui;
  time_t today;                
  time( &today );                     		// donne la date en secondes dans un entier long today
  aujourdhui  = localtime( &today );	// convertit les secondes en jour, mois, an dans la structure aujourd'hui
  jour =  jj ? jj : aujourdhui->tm_mday;
  mois =  mm ? mm : aujourdhui->tm_mon+1 ;
  an   =  aa ? aa : aujourdhui->tm_year+1900;
.......
  
  
