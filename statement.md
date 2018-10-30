```C++ runnable
#include <iostream>
struct A
 {
   A(int& var) : r(var) {}

   int &r;
 };

 int main(int argc, char** argv)
 {
   int x = 23;

   A a1(x);

   A a2 = a1;

   a2 = a1;

   return 0;
 }
