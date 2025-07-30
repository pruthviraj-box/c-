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
