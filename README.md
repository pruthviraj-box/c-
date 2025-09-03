# c-
c++code


#include <iostream>
using namespace std;

class item {
    int number;
    float cost;

public:
    void getdata(int a, float b) {
        number = a;
        cost = b;
    }
void putdata(void) {
        cout << "number: " << number << "\n";
        cout << "cost: " << cost << "\n";
    }
};

int main() {
    item item1;
    item1.getdata(10, 99.99);
    item1.putdata();
    return 0;
}

inline function

#include <iostream>
using namespace std;

inline int fun(int a, int b, int c) {
    return (a > b) ? ((a > c) ? a : c) : ((b > c) ? b : c);
}

int main() {
    int value = fun(67, 87, 53);
    cout << value;
    return 0;
}






#include <iostream>
using namespace std;

class ankush;  
class ankit;

class ankush {
private:
    int money1 = 10;

    friend void rohit(ankush, ankit);
};

class ankit {
private:
    int money2 = 20;

    friend void rohit(ankush, ankit);
};
void rohit(ankush obj1, ankit obj2) {
    cout << "Sum: " << obj1.money1 + obj2.money2 << endl;
}

int main() {
    ankush obj1;
    ankit obj2;
    rohit(obj1, obj2);  
}


#include <iostream>
using namespace std;

class A {
public:
    void display() {
        cout << "Superclass display function" << endl;
    }
};

class B : public A {
public:
    void show() {
        cout << "Subclass B display function" << endl;
    }
};


class C : public A {
public:
    void display1() {
        cout << "Subclass C display function" << endl;
    }
};

class D : public A {
public:
    void display2() {
        cout << "Subclass D display function" << endl;
    }
};

int main() {
    A objA;
    B objB;
    C objC;
    D objD;


    objA.display();

    
    objB.display();  
    objB.show();    

    objC.display();  
    objC.display1(); 

    objD.display(); 
    objD.display2(); 

    return 0;
}
