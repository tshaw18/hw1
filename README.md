#include <iostream>
#include <cmath>
#include <ctime>

using namespace std;

void ex02();
void ex03();
void ex04();
void ex05();

int doubleInt (int number);
int add(int sum);
int ex05_a();


int main() {
   
    ex02();
    ex03();
    ex04();
    ex05();
    
}

void ex02() {
    // initialize
    srand(time(NULL));
    int numberOfShares = 0;
    int boxW = 0;
    int bookW = 0;
    int shelfLife = 0;
    int temp = 0;

    // a)
    bool hasPassedTest = true;
    // b)
    int x = rand() % 100;
    int y = rand() % 100;
    
    // b)
    if (x > y)
        cout << "X (" << x << ") is greater than Y (" << y << ").\n" << endl;
    else if (x == y)
        cout << "X (" << x << ") is equal to Y (" << y << ").\n" << endl;
    else if (x < y)
        cout << "X (" << x << ") is greater than Y (" << y << ").\n" << endl;
    
    // c)
    cout << "Gimme a value: ";
    cin >> numberOfShares;
    if (numberOfShares < 100)
        cout << "That value is less than 100.\n\n";
    else
        cout << "That value is greater than or equal to 100.\n\n";
    
    // d)
    cout << "What is the box width? ";
    cin >> boxW;
    cout << "What is the book width? ";
    cin >> bookW;
    
    if (boxW % bookW == 0)
        cout << "The box width is evenly divisible by the book width!\n\n";
    else
        cout << "The box width is NOT evenly divisible by the book width.\n\n";
    
    // e)
    cout << "What is the shelf life of a box of chocolates? ";
    cin >> shelfLife;
    cout << "What is the temperature in Fahrenheit outside? ";
    cin >> temp;
    if (shelfLife > 90)
        shelfLife = shelfLife - 4;
    cout << "Shelf Life of a box of chocolates: " << shelfLife << endl;
}

void ex03() {
    // initialize
    char reply;
    // a)
    double area = 0;
    cout << "Enter an area for a square: ";
    cin >> area;
    cout << "The length of the diagonal for that square is: " << sqrt(area + area);
    
    // b)
    while (reply != 'y' && reply != 'n'){
    cout << "\nEnter yes (y) or no (n) : ";
    cin >> reply;
    }
    
    // c)
    char tab = '    ';
    
    // d)
    string mailingAddress;
    cout << "What is your mailing address? ";
    cin.ignore();
    getline(cin, mailingAddress);
    
    // e)
    string empty = " ";
    
}

void ex04(){
    
    int number = 0;
    int sum = 0;
    int j = 0;
    // a)
    do {
        cout << "\nEnter a number between 1 and 10: ";
        cin >> number;
        
    } while (number < 1 || number > 10);
    // b)
    for (int i = 1; i <= number; i++){
        sum+= (i * i * i);
    }
    // c)
    do {
        cout << " *";
        j++;
    } while (j < number);
    cout << endl;
    // d)
    for (int x = 0; x <= 40; x++) {
        if ((x % 2 == 0 || x == 0))
            cout << x << " ";
            
    }
    cout << endl;
    // e)
    cout << doubleInt(number) << endl;
    // f)
    cout << add(sum) << endl;
}

void ex05(){
// a)
    int sum = 0;
    double product = 0;
    int number[5];
    for (int i = 0; i < 5; i++){
        cin >> number[i];
    }
// b)
    for (int i = 0; i < 5; i++){
        sum+= number[i];
    }
    for (int i = 0; i < 5; i++){
        product+= number[i];
    }
    cout << "Sum: " << sum << "\nProduct: " << product << endl;
    
// c)
    //I'm not sure how to do these last two...
}

// ex05
//int ex05_a(int x, int y){
    //for (int i = 0; i < x ; i++){
      //  cout << ex05(number[5])<< endl;
   // }
//}

// ex04 e)
int doubleInt (int number){
    int doubleI = number * 2;
    return doubleI;
}
// ex04 f)
int add(int sum){
srand(time(NULL));
   int x = rand() % 100;
   int y = rand() % 100;
    sum = x + y;
    
    return sum;
}
