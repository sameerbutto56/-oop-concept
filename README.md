# -oop-concept
some basic oop concept
#include<iostream>
using namespace std;

class Shape {
public:
	Shape(){}
	virtual void calculateArea() = 0;
	void printArea() {
		cout << "Print Area of Shape" << endl;
	}




};
class TwoDim:public Shape { 
public:
	TwoDim(){}
	virtual void calculateTwoDim() = 0;
	void calculateTwoDim() {
		cout << "Calculate Area of two dim" << endl;
	}


};
class ThreeDim :public Shape {
public:
	ThreeDim(){}
	virtual void calculateTwoDim() = 0;
	void calculateTwoDim() {
		cout << "Calculate Area of three dim" << endl;
	}

};
class Circle :public TwoDim {
public:
	Circle(){}
	void PrintArea() {
		cout << "Print Area of Circle" << endl;
	}
	void calculateTwoDimArea() {
		cout << "calculate Two dim area of Circle" << endl;


	}
		
};
class Triangle :public TwoDim {
public:
	Triangle(){}
	void PrintArea() {
		cout << "Print Area of Triangle" << endl;
	}
		void calculateTwoDimArea() {
			cout << "calculate Two dim area of triangle" << endl;

		
	}
		
};
class Rectangle :public TwoDim{ 
public:
	Rectangle(){}
	void PrintArea() {
		cout << "Print Area of Rectangle" << endl;
	}
	void calculateTwoDimArea() {
		cout << "calculate Two dim area of Rectangle" << endl;


	}
};
class Cube : public ThreeDim {
	void PrintArea() {
		cout << "Print Area of cube" << endl;
	}
	void calculateThreeDimArea() {
		cout << "calculate THree dim area of Cube" << endl;


	}
};
class Cone : public ThreeDim {
public:
	Cone(){}
	void PrintArea() {
		cout << "Print Area of Cone" << endl;
	}
	void calculateThreeDimArea() {
		cout << "calculate THree dim area of Cone" << endl;


	}
};

int main() {

	Shape* obj1 = new Shape();
	TwoDim* obj2 = new TwoDim();//
	ThreeDim* obj3 = new ThreeDim();
	TwoDim* obj4 = new Circle();
	TwoDim* obj5 = new Triangle();
	Circle* obj6 = new Circle();
	Rectangle* obj7 = new Rectangle();
	Cube* obj8 = new Cube();
	Cone* obj9 = new Cone();
	obj7->printArea();
	obj8->printArea();
	obj9->printArea();
	obj8->calculateThreeDimArea();
	obj6->calculateTwoDimArea();

	return 0;
}
