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
 /**
 main.cc: In function 'int main(int, char**)':
main.cc:17:9: error: use of deleted function 'A& A::operator=(const A&)'
    a2 = a1;
         ^~
main.cc:2:8: note: 'A& A::operator=(const A&)' is implicitly deleted because the default definition would be ill-formed:
 struct A
        ^
main.cc:2:8: error: non-static reference member 'int& A::r', can't use default assignment operator
**/
