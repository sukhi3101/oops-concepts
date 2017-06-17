# oops-concepts
My second presentation
                                         OOPS CONCEPTS

We have 4 basic things in java to understand or it can even be called as 4 pillars for understanding the whole core java concept they are-:
1)	Abstraction
2)	Polymorphism
3)	Inheritance
4)	Encapsulation
Abstraction-: Showing only essential details and hiding all the irrelevant details is called as abstraction.

EXAMPLE-: abstract class Bike{  
  abstract void run();  
}  
class Honda4 extends Bike{  
void run(){System.out.println("running safely..");}  
public static void main(String args[]){  
 Bike obj = new Honda4();  
 obj.run();  
}  
} 
OUTPUT-:
running safely..


Polymorphism-: Polymorphism means many forms. The most common use of polymorphism in oop occurs when a parent class reference is used to refer to a child class object.

EXAMPLE-: class Bike{  
  void run(){System.out.println("running");}  
}  
class Hayabusa extends Bike{  
  void run(){System.out.println("running safely with 60km");}  
  
  public static void main(String args[]){  
    Bike b = new Splender();//upcasting  
    b.run();  
  }  
} 

OUTPUT:running safely with 60km.


Inheritance-: Creating a class from an existing class or to be more specific creating a child class by inheriting the properties of a parent class is called as inheritance.

EXAMPLE-: class Animal{  
void eat(){System.out.println("eating...");}  
}  
class Dog extends Animal{  
void bark(){System.out.println("barking...");}  
}  
class BabyDog extends Dog{  
void weep(){System.out.println("weeping...");}  
}  
class TestInheritance2{  
public static void main(String args[]){  
BabyDog d=new BabyDog();  
d.weep();  
d.bark();  
d.eat();  
}}  
OUTPUT:
weeping...
barking...
eating...


Encapsulation-: Wrapping or binding of data and methods together into a container called class and by providing security to data is called as encapsulation.

EXAMPLE-:  //save as Student.java
package com.sukhi;  
public class Student{  
private String name;  
   
public String getName(){  
return name;  
}  
public void setName(String name){  
this.name=name  
}  
}  
//save as Test.java  
package com.sukhi;
class Test{  
public static void main(String[] args){  
Student s=new Student();  
s.setName("sukhvinder");  
System.out.println(s.getName());  
}  
}  

OUTPUT: sukhvinder

PROGRAMS-:
EMPLOYEE.JAVA-
package assignment1;

public class Employee {
	int empid;
	int empsal;
Employee()
{
	
}
	Employee(int empid,int empsal)
{
	this.empid=empid;
	this.empsal=empsal;
	
}
void print()
{
	System.out.println("Employee-id: "+empid+" Employee-sal: "+empsal);
}

public static void main(String[] args)
{
	Employee e=new Employee(18,60000);
	
e.print();
Employee e1=new Employee(14,50000);

e1.print();

}
}

OUTPUT-Employee-id: 18 Employee-sal: 60000
Employee-id: 14 Employee-sal: 50000

VEHICLE.JAVA-package assignment1;

public interface Vehicle {
     void setNoOfTires(int number);
	void setWeight(int pounds);
	void setMake(String make);
	void setModel(String model);
	
}

CAR.JAVA-package assignment1;

public class Car  implements Vehicle{
	public void setNoOfTires(int number){
		System.out.println("Vehicle Type: Car");
		System.out.println("No-tires: "+number);
	}
	public void setWeight(int pounds){
		System.out.println("Weight: "+pounds);
	}
	public void setMake(String make){
		System.out.println("Make: "+make);
			
	}
	public void setModel(String model){
		System.out.println("Model: "+model);
		
	}
	

}
BICYCLE.JAVA-package assignment1;

public class Bicycle  implements Vehicle{
	public void setNoOfTires(int number){
		System.out.println("Vehicle Type: Bicycle");
		System.out.println("Num-tires: "+number);
	}
	public void setWeight(int pounds){
		System.out.println("Weight: "+pounds);
	}
	public void setMake(String make){
		System.out.println("Make: "+make);
			
	}
	public void setModel(String model){
		System.out.println("Model: "+model);
		
	}


}

SEMITRUCK.JAVA-package assignment1;

public class SemiTruck implements Vehicle {
	public void setNoOfTires(int number){
		System.out.println("Vehicle Type: SemiTruck");
		System.out.println("Num-tires: "+number);
	}
	public void setWeight(int pounds){
		System.out.println("Weight: "+pounds);
	}
	public void setMake(String make){
		System.out.println("Make: "+make);
			
	}
	public void setModel(String model){
		System.out.println("Model: "+model);
		
	}

}

TESTVEHICLE.JAVA-package assignment1;

public class TestVehicle {

	public static void main(String[] args) {

		Vehicle v=new Car();
		v.setNoOfTires(4);
		v.setWeight(2000);
		v.setMake("Chrysler");
		v.setModel("300");
		Vehicle v1=new Bicycle();
		v1.setNoOfTires(2);
		v1.setWeight(200);
		v1.setMake("Hero");
		v1.setModel("210");
		Vehicle v2=new SemiTruck();
		v2.setNoOfTires(8);
		v2.setWeight(20000);
		v2.setMake("Volvo");
		v2.setModel("2017");
		
	}

}

OUTPUT-Vehicle Type: Bicycle
Num-tires: 2
Weight: 200
Make: Hero
Model: 210
Vehicle Type: SemiTruck
Num-tires: 8
Weight: 20000
Make: Volvo
Model: 2017
