# cpp-lab3-sb-bsu
practical work 3 code



#include <iostream> 
using namespace std; 

int main()
{
int number, balance; 
/* declare int number (input) и balance (remainder) */ 
cout << "Enter number: "; 
cin >> number; //initializing number
balance = number % 2; 
/* remainder of number / 2 is assigned to balance */
if (balance == 0) cout << "The number is even. " << number + 1; 
/* if balance equals 0, the number is even, so we increment it by 1 */
else cout << "The number is odd. " << number - 1; //otherwise it's odd

return 0;
}


#include <iostream>
#include <iomanip> //needed for setprecision() output
using namespace std; 

int main()
{
double amount; //goods quantity
double price; //price per unit 
double cost; //total cost 
 
cout << "Enter price per unit: ";
cin >> price;    
cout << "Enter quantity: ";    
cin >> amount; 
cost = price * amount; 
cout << "Goods cost : " << fixed << setprecision(2) << cost << endl;
/* fixed and setprecision(2) are used to display the output with 2 digits after the point */
if (cost <= 100)     // check the condition
cout << "No discount!" << endl;
else    // calculating the discount
{
cost = cost*0.97; //the discount is calculated 
cout << "You have a discount. " << endl;
cout << "Price with discount is: " << fixed
<< setprecision(2) << cost << endl; 
}
return 0;
}



#include <iostream> 
#include <iomanip> 
using namespace std; 

int main()
{

double t_stav; //declaring pay rate variable
int exp; //declaring experience variable
double nadbavka; //declaring salary increment variable
cout << "Enter pay rate: "; 
cin >> t_stav;
cout << "Enter experience in years: "; 
cin >> exp;
if (exp < 5)
{
nadbavka=t_stav*0.05;
}
else if ((exp >=5) && (exp <10)) 
/* && (logical AND) means expression ((exp >=5) && (exp<10)) will be TRUE only if both parts are true */
{
nadbavka=t_stav*0.09;
}
else if ((exp >= 10) && (exp <= 15)) 
/* second condition: experience range from 10 to 15 */
{
nadbavka=t_stav*0.12;
} 
else //statements will get executed if exp > 15
{
nadbavka=t_stav*0.17;
}    
cout << "Your salary increment is " << fixed
<< setprecision(2) << nadbavka;
return 0;
}



#include <iostream> 
#include <iomanip> 
using namespace std; 
int main()

{
int number = 0;
cout << "Enter a number from 1 to 5 : "; 
cin >> number; //initialize number
switch(number) 
/* contains the expression we check. Can be an integer or character */
{ // starting switch block
/* when matched with case, the statements below are executed until the end of switch block or until break statement is met */
case 1:
cout << "one";
break;
case 2:
cout << "two"; 
break;
case 3:
cout << "three"; 
break;
case 4:
cout << "four"; 
break;
case 5:
cout << "five"; 
break;
/* default statements are executed when no other conditions are met */
default :
cout << "The number is not within 1 to 5 range";
}//finishing switch block
return 0;
}
