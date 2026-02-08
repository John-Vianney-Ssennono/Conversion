  /*
   ****************************************************************************
   *** Program: conversions.c                                               ***
   *** Author: John Vianney Ssennono                                        ***
   *** Description: The program will ask the user for any random values  of ***
   *** energy in kilocalories and fuel burn rate in gallons per hour. The   ***
   *** program will convert these input variables to their metric units of  ***
   *** ergs and liters per second respectively. 
   ****************************************************************************
   */
#include <stdio.h>

int main ()
{/*main*/
   
   /*
    ***************************
    *** Declaration Section ***
    ***************************
    *
    **************************************************************************
    * The variables to be converted are declared in this section accordingly *
    * more so the constants which are going to be used while running the     * 
    * program.                                                               *  
    **************************************************************************
    */
    
   /* 
    *****************************
    * Named Variable subsection *
    *****************************
    */
   

    const float joules_per_calorie      = 4.184;
    const float ergs_per_joule          = 1e+7;
    const float quarts_per_liter        = 1.05669;
    const int calories_per_kilocalorie  = 1000;
    const int quarts_per_gallon         = 4;
    const int seconds_per_hour          = 3600;
   /*
    *******************************
    * Unnamed variable subsection *
    *******************************
    */   


    float energy_in_kilocalories;
    float energy_in_ergs;
    float fuel_burn_rate_in_gallons_per_hour;
    float fuel_burn_rate_in_liters_per_second;


    /*
    *********************
    * Greeting section  *
    *********************
    *
    *************************************************************************
    * This program is going to be used to convert the units of any desired  *
    * energy and fuel burn rate input by the user from, kilocalories to ergs*
    * and  gallons per hour to liters per second respectively.              * 
    * This because Kilocalories and gallons per hour are english units      *
    * so they are going to be converted to metric units.                    *
    *************************************************************************
    */

    
    printf("Are you surviving? I am here to help you convert any energy you");
    printf(" want from kilocalories to ergs and any fuel burn rate from ");
    printf("gallons per hour to liters per second.\n");
    printf("So, let's make this quick. Answer the following questions for");
    printf(" me.\n");
    printf("What is the energy in kilocalories?\n");
    printf("What is the fuel burn rate in gallons per hour?\n");

    
   /*
    **********************
    * Input subsection   *
    **********************
    *
    *************************************************************************
    * The user types in the valuesof the energy in kilocalories and the fuel*
    * burn rate in gallons per hour.                                        *
    ************************************************************************* 
    */

    scanf("%f", &energy_in_kilocalories);
    scanf("%f", &fuel_burn_rate_in_gallons_per_hour);
   
   /* 
    ****************************
    * Calculation sub-section  *
    ****************************
    *
    ************************************************************************* 
    * The conversion statement is carried out using multiplication and      *
    * division method until the desired unit is achieved.                   *
    *************************************************************************
    */

    energy_in_ergs = (energy_in_kilocalories * calories_per_kilocalorie * 
        joules_per_calorie * ergs_per_joule);
    
    fuel_burn_rate_in_liters_per_second =
        (fuel_burn_rate_in_gallons_per_hour * quarts_per_gallon)
        /(quarts_per_liter * seconds_per_hour);  
    
   /*
    **********************
    * Output sub-section *
    **********************
    *
    *************************************************************************
    * The answers to the conversion are then going to be output to the      *
    * terminal screen by the statements below in order of energy, then the  *
    * fuel burn rate.                                                       *
    *************************************************************************
    */

    printf("Energy in kilocalories is %f.\n", energy_in_kilocalories);
    printf("Fuel burn rate in gallons per hour is %f.\n");
    printf("Energy in ergs is %f.\n", energy_in_ergs);
    printf("Fuel burn rate in liters per second is %f.\n",
        fuel_burn_rate_in_liters_per_second);

 



}/*main*/

