# Encapsulation :

<br><br>

## What is Data Encapsulation ?

<br>

> * Encapsulation means wrapping code as much as you can in a class.
> * every logic must be written in class.
> * It helps in hiding the implementation details and provides data protection.

<br/><br/>

## setter & getter :

<br>

 `setter :` 
 
 <br>

  > * a function to take input of attributes.

<br/>

  `getter :`

<br>
  
> * a function to give output of attributes.

<br/>

## this Keyword :

<br>

> * when class attributes and function parameters both have same name, then we can make difference and identify the class attributes using this keyword.
> * this keyword is written before the class variable.

<br>

`USE : `

<br>

> * this->varName

<br>

### private attributes :

<br>

> * private atributes are support only for class.

<br>

### * Nasted member function :

<br>

> * A nested member function is a function within a function.

<br>

## Array of Objects :

<br>

> * Collection of Object of same class.

  > `Definition : `

  <br>
  
  > * className objName[size];

  > `Example : `

<br>
  
  > * student s1[50]; 


<br><br>

## What is Static Member : 

> * these are the members which represents the class directly.
> * these members are common for the all class objects.
> * these member also gives the same value for all class objects.
> * there are two types of static members:
> * `static data members`
> * `static member functions`
> * these are the simply class attributes and methods which can be
> * created using 'static' keyword.

<br/><br/>

### Static data members :

> * attributes created using static keyword.
> * this kind of variables acquires the memory space only once among all objects.
> * static data members must be assigned once in global area using scope resolution operator according to following syntex.
> * `::` scope resolution operator or Membership lable operator.
> * `DataType  ClassName :: varName = value;`
> * static data members gives the same value for all class objects.

<br/><br/>


### Static member functions :
> * class methods created using static keyword.
> * these kind of methods can only used with static atributes.
> * normal data members(attributes) aren't supported in static member functions.
> * these methods can be accessed directly only if there are public
> * static member function can be accessed like following syntex.
> * `ClassName :: methodName([arguments]);`

<br/><br/>

<p><img src = "https://github.com/SJaynesh/CPP-Languge-Ch-03/assets/115562979/449c51c6-ecce-4220-a29e-63b54725e52b.png" width=60% height=50%></p>

<br><br>

## Constructor :

> * `Constructor is a block of code which is automatically invoked when class is instanciated.`
> * Constructor is automatically called when an object(instance of class) is created. It is a special member function of the class.

<br>

### Rules to Create Constructor :
> * The name constructor must be same as class name.
> * Constructor cannot have any return datatype like void, int, char, etc...
> * It cannot return anything.

<br/><br/>

https://github.com/SJaynesh/CPP-Languge-Ch-04/assets/115562979/45f31973-7713-4d2c-9c58-6a1c581e41f5


<br/>

## Types of Constructor :
> `1. Default Constructor` <br><br>
> `2. Parameterized Constructor` <br><br>
> `3. Copy Constructor` <br><br>


<br/><br/>

### 1. Default Constructor :
> * `Default constructor is the constructor which doesn’t take any argument. It has no parameters. In this case, as soon as the object is created the constructor is called which initializes its data members. `

<br/>

<pre>
  #include<iostream>
  using namespace std;

  class City {
  	
  	//default Constructor
  	public :
  		
  	City() {
  		cout << "My City Surat ...";
  	}
  };
  
  int main()
  {
  	City c1;	
  }
     
</pre>


<br/><br/>

### 2. Parameterized Constructor :
> * `These are the constructors with parameters. Using this Constructor you can provide different values to data members of different objects, by passing the appropriate values as arguments. `

<br/>

<pre>
 
  #include<iostream>
  using namespace std;

  class City {
  	
  	private :
  		string cityName;
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
> * ` A copy constructor  is a member function which initializes an object using another object of the same class. `
> * to copy data of another object.
> * Both object must belong to the same class.
> * Two types of copy constructor.
> * `1. Implicit  `
> * `2. Explicit  `

<br/>

#### `1. Implicit  : `

<br/>

<pre>
 #include<iostream>
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
	City c2 = c1; // Implicit 
	

	c1.getData();
	c2.getData();
		
}
</pre>

<br/>

#### `2. Explicit  : `

<br/>

<pre>
 #include<iostream>
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
	City c2(c1); // Explicit 
	

	c1.getData();
	c2.getData();
		
}
</pre>

<br/><br/>

## Destructor :
> * `A Block of code which is automatically invoked when object is distroyed or code is completed.`

<br/>

### Rules to Create Constructor :
> * It's name must be same as class name but it begies with tild '~' operator.
> * Destructor cannot have any return datatype like void, int, char, etc...
> * It cannot return anything.

<br/>

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
			cout << "Code is End";
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



