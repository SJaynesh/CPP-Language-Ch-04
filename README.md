# Encapsulation :

<br><br>

## `Data Encapsulation`
(Encapsulation / Data Hiding)

<br>

> * `Encapsulation means wrapping code as much as you can in a class.`
> * Every logic must be written in class.
> * The meaning of Encapsulation is to make sure that **"sensitive" data is hidden from users**.
> * It helps in hiding the implementation details and provides data protection.
> * To achieve this, we **must declare class varibles/attributes** as **private**(cannot be accessed from outside the class).
> * If you want others **to read or modify the value** of a private member, you can provide **public getter and setter methods**.

<br/><br/>

## `Setter & Getter` 

<br>

 ` setter ` 
 
 <br>

  > * A method which is used to set(initialize) the data members.
  > * A function to take input of attributes.

<br/>

  ` getter `

<br>

 > * A method which is used to get(access) the data members.
 > * A function to give output of attributes.

<br/>

`NOTE : `
> Both setter & getter must be public for access and modify the data members.

<br><br>

## `this Keyword`

<br>

> * `When class attributes and function parameters both have same name, then we can make difference and identify the class attributes using this keyword`.
> * The this keyword is pointer that points to the current instance of a class.
> * It is a special keyword that is used within the member funtions of a class to refer to the object on which the function is called.
> * this keyword is written before the class attributes.

<br>

`USE : `

<br>

> * this->varName
> * this of variable name.

<br><br>

### `private attributes`

<br>

> * Access to provide attributes is controlled through public methods (getter and setters).
> * Private attributes are support only for class.

<br><br>

### `Nasted Member Function`

<br>

> * A nested member function is a function within a function.

<br><br>

## `Array of Objects`

<br>

> * An array of objects is a collection of object of the same class stored in contiguous memory locations.
> * Eash element of the array is an instance of the class.

<br><br>

![arrayOfObject](https://github.com/user-attachments/assets/68f83fed-25b2-41ec-b805-b79b0d8cda51)

<br><br>

## `Scope Resulation Operator`

<br>

> * The scope resoultion operator (::) is used to access elements in a class or to access global variables.
> * It allows you to specify the context in which a particular identifier (variable, function, or class) is defined.

<br>

` Commonly it is used for: `

 > Access Global Variables
 > Access Static Members  

<br>

![global varibales](https://github.com/user-attachments/assets/d1cb0521-6138-4781-be53-3983b0063bb3)


<br><br>

## `static Keyword`

<br>

> * A static is a keyword or modifier that belongs to the type not instance. So **instance is not requied to access the static members**.
> * In C++, a static can be field, method, constructor, class, or properties.
> * A field which is declared as static is called static field. It is shared among all the objects.
> * These are the members which represents the class directly.
> * These members are common for the all class objects.
> * These member also gives the same value for all class objects.
> * There are two types of static members:

<br>

### `Use case of static Keyword`

<br>

> 1. Static Data Members
> 2. Static Members Functions 

<br/><br/>

### `Static Data Members`

<br>

> * Attributes created using **static** keyword.
> * This kind of variables acquires the memory space only once among all objects.
> * static data members must be assigned once in global area using **scope resolution operator** according to following syntex.
> * `::` scope resolution operator or Membership lable operator.
> * `DataType  ClassName :: varName = value;`
> * static data members gives the same value for all class objects.

<br/><br/>


### `Static Member Functions`

<br>

> * class methods created using **static** keyword.
> * These kind of methods can only used with static atributes.
> * Normal data members(attributes) aren't supported in static member functions.
> * These methods can be accessed directly only if there are public
> * static member function can be accessed like following syntex.
> * `ClassName :: methodName([arguments]);`


<br><br>

## Constructor :

<br>

> * `Constructor is a block of code which is automatically invoked when class is instanciated.`
> * A Constructor is a **special member function** is a class that **gets executed when a class is instantiated**(an object of the class is created).
> * Constructor is automatically called when an object(instance of class) is created. It is a special member function of the class.
> * It has the **same name as the class** and is **used to initialize the object's data members**.

<br><br>

### Rules to Create Constructor :

<br>

> * The name constructor must be same as class name.
> * Constructor cannot have any return datatype like void, int, char, etc...
> * Constructor cannot return anything.

<br><br>

## Types of Constructor :

<br>

> `1. Default Constructor` <br><br>
> `2. Parameterised Constructor` <br><br>
> `3. Copy Constructor` <br><br>

<br><br>

https://github.com/SJaynesh/CPP-Languge-Ch-04/assets/115562979/45f31973-7713-4d2c-9c58-6a1c581e41f5  


<br/><br/>

### 1. Default Constructor :

<br>

> * Default constructor is the constructor which doesn’t take any argument. It has no parameters. In this case, as soon as the object is created the constructor is called which initializes its data members. 

<br/>

![default constructor](https://github.com/user-attachments/assets/23f0ab70-22c9-402c-86f5-1c0c53e58a36)

<br/>

<br/>

<pre>
 
  #include<<iostream>iostream>
  using namespace std;

  class City {
  	
  	//Default Constructor
  	public :
  		
  		City() {
  			cout << "Welcome to City." << endl;
  		}
  };
  
  int main()
  {
  	City c1;
        City c2;							    
  }
     
</pre>




<br/><br/>

### 2. Parameterised Constructor :

<br>

> * These are the constructors with parameters. Using this Constructor you can provide different values to data members of different objects, by passing the appropriate values as arguments.

<br/>

![Parameterized Constructor](https://github.com/user-attachments/assets/e7075629-3cac-4981-a605-a85d6bb54c1a)

<br/><br/>

<pre>
 
  #include<<iostream>iostream>
  using namespace std;

  class City {
  	
  	private :
  		char cityName[];
  		int pincode;
  	
  	//Parameterized Constructor
  	public :
  		
  		City(string cityName, int pincode) {
  			
  			this->cityName = cityName;
  			this->pincode = pincode;
  			
  		}
  		
  		void getData()
  		{
  			cout << "CITY NAME : " << cityName << endl;
  			cout << "PINCODE : " << pincode << endl;
  		}
  };
  
  int main()
  {
  	City c1("Surat",395010);
  	
  	c1.getData();
  		
  }
     
</pre>


<br/><br/>

### 3. Copy Constructor :

<br>

> * A copy constructor  is a member function which initializes an object using another object of the same class. 
> * To copy data of another object.
> * Both object must belong to the same class.

> * Two types of copy constructor.
> * `1. Implicit Copy Constructor `
> * `2. Explicit Copy Constructor `

<br/>

![Copy Constructor](https://github.com/user-attachments/assets/46439120-ccd4-4938-a8fd-64cd7e2071d1)

<br/><br/>

#### `1. Implicit Copy Constructor : `

<br/>

<pre>
 #include<<iostream>iostream>
 using namespace std;

class City {
	
	private :
		string cityName;
		int pincode;
	
	//Copy Constructor
	public :
		
		City(string cityName,int pincode) {
			this->cityName = cityName;
			this->pincode = pincode;
		}
		
		void getData()
		{
			cout << endl << "City Name : " << cityName << endl;
			cout << "Pincode : " << pincode << endl;
		}
		
	
};

int main()
{
	City c1("Surat",395010);
	City c2 = c1; // Implicit Copy Constructor
	

	c1.getData();
	c2.getData();
		
}
</pre>

<br/>

#### `2. Explicit Copy Constructor : `

<br/>

<pre>

#include<<iostream>iostream>
using namespace std;

class City {
	
	private :
		string cityName;
		int pincode;
	
	//Copy Constructor
	public :
		
		City(string cityName,int pincode) {
			this->cityName = cityName;
			this->pincode = pincode;
		}
		
		City(City &c) {
			this->cityName = c.cityName;
			this->pincode = c.pincode;
		}
		
		void getData()
		{
			cout << endl << "City Name : " << cityName << endl;
			cout << "Pincode : " << pincode << endl;
		}
		
	
};

int main()
{
	City c1("Surat",395010);
	City c2(c1); // Explicit Copy Constructor
	

	c1.getData();
	c2.getData();
		
}
</pre>

<br/><br/>

## Destructor :

<br>

> * `A Block of code which is automatically invoked when a program is completed or an object is deleted.`
> *  A destructor is a special member fucntion in a class that gets executed when an object is destroyed or goes out of scope.

<br><br>

### Rules to Create Destructor :

<br>

> * It's name must be same as class name but it begies with tild '~' operator.
> * Destructor cannot have any return datatype like void, int, char, etc...
> * It cannot return anything.

<br/>

<br>

![Destructor](https://github.com/user-attachments/assets/85073e4c-2b44-414c-b690-8e2abd1c6719)

<br><br>

<pre>
#include<iostream>
using namespace std;

class City {
	
	private :
		string cityName;
		int pincode;
	
	
	public :
		// Constructor
		City(string cityName,int pincode) {
			this->cityName = cityName;
			this->pincode = pincode;
		}
		
		// Destructor
		~City() {
			cout << "Thankyou for Visit...";
		}
		
		void getData()
		{
			cout << endl << "City Name : " << cityName << endl;
			cout << "Pincode : " << pincode << endl;
		}
		
	
};

int main()
{
	City c1("Surat",395010);
	
	c1.getData();
		
}
</pre>


<br><br>

<br><br>


## Friend Function:

<br>

> * `It is the type of function by which we can access private attributes or methods of any class.`
> * It can be created using friend keyword.

<br>

### friend Keyword:

<br>

> * friend returnDataType functionName();

<br>

> * It's being used as a getter when doesn't contain it's own getter.
> * `Though friend function can also access the private attributes of class, it can be us as a getter of one or more class.`

<br>

