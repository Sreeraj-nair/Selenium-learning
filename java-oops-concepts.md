## What is an Object? (Encapsulation)
An object is a software bundle of related state and behavior. Eg your dog, your desk, your TV set, your bicycle. 

Real world objects share two characteristics. They all have state and behavior. Dogs have state (name, color, breed, hungry) and behavior 
(barking, fetching, wagging tail). 

Software Object will have Fields (state) and Methods (behavior). Eg Bicycle will have state like 

## What is a class? 
A class is a blueprint or prototype from which objects are created. 

## What is inheritance? 
Different kinds of objects often have a certain amount in common with each other. It is the ability of an object to aquire properties from other class. 

## What is an interface? 
Interface is a group of related methods with empty bodies. 

## What is a package? 
A package is a namespace that organizes a set of related classes and interfaces.

## What is the difference between static and instance variables? 
In certain cases, only one copy of a particular variable should be shared by all objects of a class- here a static variable is used.
A static variable represents class wide info. All objects of a class share the same data.

Instance variables accross different objects can have different values whereas class variables across different objects can have only 
one value. 

    class Test{
        public static int a = 5;
        public int b = 10;
    }
    // here t1 and t2 will have a separate copy of b
    // while they will have same copy of a.
    Test t1 = new Test(); 
    Test t2 = new Test();
    
You can access a static variable with it's class Name like this

    Test.a = 1//some value But you can not access instance variable like this
    System.out.println(t1.a);
    System.out.println(t2.a);
    
In both cases output will be 1 as a is share by all instances of the test class. while the instance variable will each have separate copy of b (instance variable) So

    t1.b = 15 // will not be reflected in t2.
    System.out.println(t1.b); // this will print 15
    System.out.println(t2.b); / this will still print 10; 
              

