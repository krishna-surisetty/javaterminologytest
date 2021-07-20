## Description File
 
A class is a blueprint, while fields or instance variables and methods in it correspond to what an Object knows or has and what an Object does.

## Common Terminology

1. Arguments vs Parameter

For a method or function we usually get confused with arguments and parameters
In brief the argument is the actual value that is being sent to a method while parameter refers to the name we use when defining the corresponding method


Let's take an example of simple name setter

	public void setName(String nameValue) {
		name = nameValue;
	}
	objectOne.setName("apple");

Here, 'apple' corresponds to argument while 'nameValue' corresponds to parameter

2. Instance Variables vs Local Variables

Instance variables usually correspond to the fields declared in a class while Local variables correspond to fields declared in a method

Let's see the following example


	class Animal {
		private float weight;
		
		public float getAnimalTypeBasedOnWeightLessThan20Units(String weightInput) {
			float weightLimit = 20F;
			if(weightInput < weightLimit) {
				return "less weight animal";
				} else {
				return "more weight animal";
				}
			}
		}


Here 'weight' corresponds to instance variable while 'weightInput' corresponds to local variable

## Lets talk about inheritance

Consider an Animal class where there are certain characteristics and attributes for are all animals. Let they be :

- Name
- Weight
- eat()

A Dog always have the above attributes, but it is has something more which differentiates it from other animals like it can bark, can dig a hole (not just dog) and many more

We can say that this Dog "Has a" Name
We can say that this Dog "Has a" Weight
We can say that this Dog "Has a" eat() process

So Dog class can extend Animal class or inherits Animal class

## Lets now see what is Encapsulation

In the Animal class, we have an attribute 'Weight'. If an object tries to set the weight directly using this format of direct access

animalObject.weight = 20

It does work fine, isn't it?

But what if the object mistakenly set the weight less than 0 like a negative value. It doesn't make sense right.
 
 So, it is always better to make the instance variables (from now on i will refer to them as variables) to make them private (an access modifier) and create Getters (also called Accessors) and Setters(also called Mutators) to get the value and set the value
 
 Now you might ask, how this helps. Well we can customize the setter giving certain conditions to set the weight as a positive value else throw an error or send them a warning message









