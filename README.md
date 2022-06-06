Cheese Program 

/// week 2 programing assignment.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include <iostream>
#include <iomanip>

//using namespace
using namespace std;

int main()
{

    //declare the constants
    const float cheese_containers = 2.76, cost_containers = 4.12, profit_containers = 1.45;
    const int headerlen = 75;

    //inatilizing the variables
    int cheese;
    int containers;
    float cost;
    float profit;

    //the welcome message for the program and intro
    string sTitle = "Welcome to my Local Grocery Cheese Program";
    int iTitleLen = static_cast<int>(sTitle.length()); //Quell compiler warning. 

    //calculating and creating a variable
    int iFillLen = headerlen - iTitleLen;
    int iFillLenHalf = iFillLen / 2;
    string strFill(iFillLenHalf, '*');

    cout << setfill('*');
    cout << setw(headerlen) << "*" << endl;
    //static_cast to quell compiler warning 
    cout << setw(static_cast<std::streamsize>(iTitleLen) + iFillLenHalf) << right << sTitle << strFill << endl;
    cout << setw(headerlen) << "*" << endl << endl;
    //reseting the setfill
    cout << setfill(' ');

    //taking the users input 
    cout << "Please enter the total number of kilograms of cheese produced: ";
    cin >> cheese;
    containers = cheese / cheese_containers + 1;
    cout << "The number of containers to hold the cheese is: "" \t " " \t" << ('\t') << containers << endl;

    //calculation for the profit and cost
    profit = containers * profit_containers;
    cost = containers * cost_containers;

    //the results after the calculations are done for the profit and cost 
    cout << "The cost of producing " << containers << " container(s) of cheese is:" << " $      \t " << ('\t') << cost << endl;
    cout << "The profit form producing " << containers << " container(s) of cheese is:" << " $    \t " << ('\t') << profit << endl;

    return 0;
}
