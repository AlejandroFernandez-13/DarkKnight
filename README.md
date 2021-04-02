#include <iostream>
#include <fstream>
#include<string>
#include<iomanip>
using namespace std;

int main()
{

std::string filename;
std::string line_;

    cout << "Enter File Name: ";
    cin >> filename;

cout << endl;

ifstream file_(filename);

    if(file_.is_open()){
    while (getline(file_, line_)){
        std::cout << line_ << endl;
}
   file_. close();

}
    else{
        std:: cout << "File was not found" << endl;
        std:: cout << "Make sure to have .txt when entering the file name" << endl;
    }

return 0;
}
