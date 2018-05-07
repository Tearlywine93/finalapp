## My Final App
### Timothy Earlywine


# Calculator for c++ final project

// Tim's C++ Simple Calculator
// Header files
#include <cstdlib>
#include <cstdio>
#include <iostream>
using namespace std;
void Welcome_screen() {
   cout << "Weclome to Tim's C++ Simple Calculator.\n";
   
}
float input_check() {
  float num;
  while(1) {
    if (cin >> num) {
      break;
    }
    if(cin.fail()) {
      cout << "Numerical value needed !! Try again: ";
      cin.clear();
      cin.ignore( 1024, '\n' ); //spend a lot of time on this!
    }
  }
   return num;
}
float Plus    (float num1, float num2) { return num1+num2; }
float Minus   (float num1, float num2) { return num1-num2; }
float Multiply(float num1, float num2) { return num1*num2; }
float Divide  (float num1, float num2) { return num1/num2; }
int main() {
  char controller;
  float num1=0;
  float num2=0;
  char myoperator;
  float result=0;
  
  do { 
    Welcome_screen();
    cout << "Enter your first number: ";
    num1 = input_check();
    cout << "\nEnter the operator: ";
    cin >> myoperator;
    cout << "\nEnter second number: ";
    num2 = input_check();
    
    switch(myoperator) {
      case '+' : result = Plus     (num1, num2); break;
      case '-' : result = Minus    (num1, num2); break;
      case '*' : result = Multiply (num1, num2); break;
      case '/' : result = Divide   (num1, num2); break;
      default : cout << "Sorry, this is a BASIC calculator \n";
    }
    cout << '\n' << result << "\n";
    cout << "Type any key and ENTER to contunue or Q ENTER to quit ...:";
    cin >> controller;
    system("clear");
  } while(controller != 'Q');
  cout << "Thanks for using my basic calculator !! \n Goodbye \n";
  return 0;
}

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Tearlywine93/finalapp/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
