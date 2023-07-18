File name: algebra.cpp
 Assign ID: PROG7 
 Author: Daylen Hall
 Purpose:     Implement and call functions.
 Perform the following calculations:
 
integers:
1) d = a + b + 7;
2) 2) e = b*a + b/b
3) f = (3 *a - b*b*b ) / 7;

floats:            
1) z = x - y + 7.5;
2) w = y*x + y/y
3) u = (3*x - x*y*z ) / 1.25;



#include <iostream>   
#include <iomanip>
#include <fstream>
#include <string>
#include <cmath>
using namespace std;

#include "algebra_functions.h"
int main()
{
 
   int a,b,c,d,e,f,g,h;                 // int calculations.
   int itemp1, itemp2, itemp3, itemp4;  // partial answers.
   float w, x, y, z,r,s,t,u;            // float calculations.
   float ftemp1, ftemp2, ftemp3, ftemp4, ftemp5;  // partial answers.

  
     DisplayCopyright(2022, "hallD241", "Daylen Hall");

 
    intRead("Enter int value for a:", a);
    cout << "a = " << a << endl;
    
    intRead("Enter int value for b:", b);
    cout << "b = " << b << endl;

    intRead("Enter int value for c:", c);
    cout << "c = " << c << endl;
    

    intPrint("int variable a = ", a);
    intPrint("int variable b = ", b);
    intPrint("int variable c = ", c);

  

    d = Add(Add(a,b), 7);

    e = Add(Mult(b,a), Div(b,b));
    
    Sub(Mult(3, a), Mult(Mult(b, b), b), itemp1);

    f = Div(itemp1, 7);

    
    

   intPrint(" a + b + 7 = ", d);
   intPrint(" b*a + b/b = ", e);
   intPrint(" (3 * a - b * b * b) / 7 = ", f);
    

   x = floatRead("FLOAT value: ");

   y = floatRead("FLOAT value: ");
   

    
    floatPrint("decimal x = ", x, 2);
    floatPrint("decimal y = ", y, 2);
    
 
    
    z = Sub(Sub(x,y), 7.5);
    
    Mult(y, x, ftemp1);

    w = Add(ftemp1,Div(y,y)); 

    Mult(3, x, ftemp2);
    Mult(x, y, ftemp3);
    Mult(z, ftemp3, ftemp4);

    u = Div(Sub(ftemp2, ftemp4), 1.25);


    floatPrint("z = ", z, 3);
    floatPrint("w = ", w, 3);
    floatPrint("u = ", u, 3);

   
    DisplayCopyright(2022, "hallD241", "Daylen Hall");

   return 0;

}//main
