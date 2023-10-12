# Encapsulation :

## * What is Data Encapsulation ?

> * Encapsulation means wrapping code as much as you can in a class.
> * every logic must be written in class.
> * It helps in hiding the implementation details and provides data protection.

<br/><br/><br/>

## * setter & getter :
<br/>

 `setter :` 
  > * a function to take input of attributes.

<br/>

  `getter :`
  > * a function to give output of attributes.

<br/><br/>
## * this Keyword :
> * when class attributes and function parameters both have same name, then we can make difference and identify the class attributes using this keyword.
> * this keyword is written before the class variable.

`USE : `
> * this->varName

`->` Fat arrow 

<br/><br/>

### private attributes :
> * private atributes are support only for class.

### * Nasted member function :
> * A nested member function is a function within a function.

<br/><br/>

## Array of Objects :
> * Collection of Object of same class.

  > `Definition : `
  > * className objName[size];

  > `Example : `
  > * student s1[50]; 


<br/><br/>

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




