<<<<<<< HEAD
<h1 align="center">Lists</h1>

<h1>Arraylists</h1>

>Java ArrayList class uses a dynamic array for storing the elements. It inherits AbstractList class and implements List interface

>ArrayList in Java can be seen as similar to vector in C++. 

> ArrayList only supports object entries, not the primitive data types(like int, float, char, etc).

>Java ArrayList class maintains insertion order

>Java ArrayList allows random access because array works at the index basis.

>In Java ArrayList class, manipulation is slow because a lot of shifting needs to be occurred if any element is removed from the array list.



### Operations


|<center>Function</center>  |<center>What it does?</center>  |  <center> Complexity </center>
| :------------- | :------------- | :------------- |
| void clear()   | It is used to remove all of the elements from this list.|O(1)
| void add(int index, Object element) | It is used to insert the specified element at the specified position index in a list.|O(1) if added at the end,O(n) if added in the interior
| int indexOf(Object o)  | It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element |O(n)
| int lastIndexOf(Object o)  |It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.|O(n)
| Object[] toArray()   |It is used to return an array containing all of the elements in this list in the correct order.|O(n)
| Object clone()  | It is used to return a shallow copy of an ArrayList.|-
| void trimToSize() |It is used to trim the capacity of this ArrayList instance to be the list's current size.|-


### Implementation of ArrayList

```java
//declaration
//creating new generic arraylist
ArrayList<String> al=new ArrayList<String>();
```
```java
//simple example
    import java.util.*;  
    class TestCollection1{  
     public static void main(String args[]){  
      ArrayList<String> list=new ArrayList<String>();//Creating arraylist  
      list.add("Shivam"); 
      list.add("Tushar");  
      list.add("Chirag");  
      list.add("Neel");  
      //Traversing list through Iterator  
      Iterator itr=list.iterator();  
      while(itr.hasNext()){  
       System.out.println(itr.next());  
      }  
      System.out.println();
     
  
     //addall()
       
      ArrayList<String> al2=new ArrayList<String>();  
	list.add("Devansh");    
	al2.addAll(list);  
	Iterator itr2 = al2.iterator();  
	  
	while(itr2.hasNext()){  
	 System.out.println(itr2.next());  
	}  
	System.out.println();
	
     //indexOf()
     
     int pos1 =list.indexOf("Shivam");
     System.out.println(pos1);
     }

    }  

```
Output:
```
Shivam
Tushar
Chirag
Neel

Shivam
Tushar
Chirag
Neel
Devansh

0

```

<br>

<h1>Vector</h1>
 
 >Vector implements a dynamic array that means it can grow or shrink as required. Like an array, it contains components that can be accessed using an index.

 >They are very similar to ArrayList but Vector is synchronised and have some legacy method which collection framework does not contain. 

 >It extends AbstractList and implements List interfaces.


### Operations

|<center>Function</center>  |<center>What it does?</center>  |  <center> Complexity </center>
| :------------- | :------------- | :------------- |
|void clear()   | It is used to remove all of the elements from this list.|O(1)
|void add(int index, Object element)  | It is used to insert the specified element at the specified position index in a list.|O(1) if added at the end,O(n) if added in the interior
|int indexOf(Object o)  | It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element |O(n)
|int lastIndexOf(Object o) |It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.|O(n)
|Object[] toArray()  |It is used to return an array containing all of the elements in this list in the correct order.|O(n)
|Object clone()  | It is used to return a shallow copy of an ArrayList.|O(n)
|void trimToSize() |It is used to trim the capacity of this ArrayList instance to be the list's current size.|-
|boolean contains(Object o)  |This method returns true if this vector contains the specified element |O(n)
|boolean remove(Object o) |This method removes the first occurrence of the specified element in this Vector If the Vector does not contain the element, it is unchanged.|O(n)
|boolean equals(Object o)| This method compares the specified Object with this Vector for equality.|O(n)


### Implementation of Vectors

```java
//declaration


import java.util.*;
class Vector_demo    
{
    public static void main(String[] arg)
    {
        
        // create default vector
        Vector v = new Vector();

        v.add("Shivam");
        v.add("Chirag");
        v.add("Devansh");
        v.add("Nishchith");
        
        System.out.println("Vector is " + v);
        
        //addall()
        Vector arr = new Vector();
         
        // copying all element of array list int0 vector
        arr.addAll(v);
        System.out.println("vector arr:" + arr);
       
       // check whether vector contains "Nishchith"
       if(v.contains("Nishchith"))
       System.out.println("Nishchith exists");
       
       //equals

        Vector v1 = new Vector();         
        v1.add("Shivam");
        v1.add("Chirag");
        v1.add("Devansh");
        v1.add("Nishchith");
        System.out.println(v.equals(v1);
    }
}
```


Output
```
Vector is [Shivam, Chirag, Devansh, Nishchith]
vector arr:[Shivam, Chirag, Devansh, Nishchith]
Nishchith exists
true
```



<h1 align="center">Difference between ArrayList and Vector</h1>

|<center>ArrayList</center>|<center>Vector</center>
| :------------- | :------------- |
|1)ArrayList is not synchronized.|1)Vector is synchronized.
|2) ArrayList increments 50% of current array size if number of element exceeds from its capacity.|2)Vector increments 100% means doubles the array size if total number of element exceeds than its capacity
|3) ArrayList uses Iterator interface to traverse the elements.|3)Vector uses Enumeration interface to traverse the elements. But it can use Iterator also.
|4)Is is fast|4)It is comparatively slower.

<br>

<h1>LinkedList</h1>

>Java LinkedList class uses doubly linked list to store the elements. It provides a linked-list data structure

>Java LinkedList class can contain duplicate elements.

>Java LinkedList class maintains insertion order.

>Java LinkedList class can be used as list, stack or queue.

###  Operations

|<center>Function</center>  |<center>What it does?</center>  |  <center> Complexity </center>
| :------------- | :------------- | :------------- |
|void clear()   | It is used to remove all of the elements from this list.|O(1)
|void add(int index, Object element) | It is used to insert the specified element at the specified position index in a list.|O(1) if added at the end,O(n) if added in the interior
|int indexOf(Object o) | It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element |O(n)
|int lastIndexOf(Object o)  |It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.in|O(n)
|Object[] toArray()  |It is used to return an array containing all of the elements in this list in the correct order.|O(n)
|Object clone()  | It is used to return a shallow copy of an ArrayList.|O(n)
|void trimToSize() |It is used to trim the capacity of this ArrayList instance to be the list's current size.|O(n)
|void addFirst(Object o)|It is used to insert the given element at the beginning of a list.|O(1)
|void addLast(Object o) |It is used to insert the given element at the ending of a list.|O(1)
|int size() |It is used to return the number of elements in a list|O(1)
|Object getFirst()|It is used to return the first element in a list.|O(1)
|Object getLast()|It is used to return the last element in a list.|O(1)



### Implementation of Vectors

<br>

```java
// declaration
//eg
LinkedList<String> al=new LinkedList<String>();

```


```java
    import java.util.*;  
    public class LinkedList_Demo{  
     public static void main(String args[]){  
      
      LinkedList<String> al=new LinkedList<String>();  
      al.add("Neel");  
      al.add("Devansh");  
      Iterator<String> itr=al.iterator();  
      while(itr.hasNext()){  
       System.out.println(itr.next());  
      }  
     System.out.println();
 
     //addfirst and last
     
     al.addFirst("chirag");
     al.addLast("hello");
     Iterator<String> itr2 = al.iterator();
     while(itr2.hasNext()){  
       System.out.println(itr2.next());  
     }  
     }  
    }  
	
```
Output:
```
Neel
Devansh

chirag
Neel
Devansh
hello
```

=======
<h1 align="center">Lists</h1>

<h1>Arraylists</h1>

>Java ArrayList class uses a dynamic array for storing the elements. It inherits AbstractList class and implements List interface

>ArrayList in Java can be seen as similar to vector in C++. 

> ArrayList only supports object entries, not the primitive data types(like int, float, char, etc).

>Java ArrayList class maintains insertion order

>Java ArrayList allows random access because array works at the index basis.

>In Java ArrayList class, manipulation is slow because a lot of shifting needs to be occurred if any element is removed from the array list.



### Operations


|<center>Function</center>  |<center>What it does?</center>  |  <center> Complexity </center>
| :------------- | :------------- | :------------- |
| void clear()   | It is used to remove all of the elements from this list.|O(1)
| void add(int index, Object element) | It is used to insert the specified element at the specified position index in a list.|O(1) if added at the end,O(n) if added in the interior
| int indexOf(Object o)  | It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element |O(n)
| int lastIndexOf(Object o)  |It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.|O(n)
| Object[] toArray()   |It is used to return an array containing all of the elements in this list in the correct order.|O(n)
| Object clone()  | It is used to return a shallow copy of an ArrayList.|-
| void trimToSize() |It is used to trim the capacity of this ArrayList instance to be the list's current size.|-


### Implementation of ArrayList

```java
//declaration
//creating new generic arraylist
ArrayList<String> al=new ArrayList<String>();
```
```java
//simple example
    import java.util.*;  
    class TestCollection1{  
     public static void main(String args[]){  
      ArrayList<String> list=new ArrayList<String>();//Creating arraylist  
      list.add("Shivam"); 
      list.add("Tushar");  
      list.add("Chirag");  
      list.add("Neel");  
      //Traversing list through Iterator  
      Iterator itr=list.iterator();  
      while(itr.hasNext()){  
       System.out.println(itr.next());  
      }  
      System.out.println();
     
  
     //addall()
       
      ArrayList<String> al2=new ArrayList<String>();  
	list.add("Devansh");    
	al2.addAll(list);  
	Iterator itr2 = al2.iterator();  
	  
	while(itr2.hasNext()){  
	 System.out.println(itr2.next());  
	}  
	System.out.println();
	
     //indexOf()
     
     int pos1 =list.indexOf("Shivam");
     System.out.println(pos1);
     }

    }  

```
Output:
```
Shivam
Tushar
Chirag
Neel

Shivam
Tushar
Chirag
Neel
Devansh

0

```

<br>

<h1>Vector</h1>
 
 >Vector implements a dynamic array that means it can grow or shrink as required. Like an array, it contains components that can be accessed using an index.

 >They are very similar to ArrayList but Vector is synchronised and have some legacy method which collection framework does not contain. 

 >It extends AbstractList and implements List interfaces.


### Operations

|<center>Function</center>  |<center>What it does?</center>  |  <center> Complexity </center>
| :------------- | :------------- | :------------- |
|void clear()   | It is used to remove all of the elements from this list.|O(1)
|void add(int index, Object element)  | It is used to insert the specified element at the specified position index in a list.|O(1) if added at the end,O(n) if added in the interior
|int indexOf(Object o)  | It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element |O(n)
|int lastIndexOf(Object o) |It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.|O(n)
|Object[] toArray()  |It is used to return an array containing all of the elements in this list in the correct order.|O(n)
|Object clone()  | It is used to return a shallow copy of an ArrayList.|O(n)
|void trimToSize() |It is used to trim the capacity of this ArrayList instance to be the list's current size.|-
|boolean contains(Object o)  |This method returns true if this vector contains the specified element |O(n)
|boolean remove(Object o) |This method removes the first occurrence of the specified element in this Vector If the Vector does not contain the element, it is unchanged.|O(n)
|boolean equals(Object o)| This method compares the specified Object with this Vector for equality.|O(n)


### Implementation of Vectors

```java
//declaration


import java.util.*;
class Vector_demo    
{
    public static void main(String[] arg)
    {
        
        // create default vector
        Vector v = new Vector();

        v.add("Shivam");
        v.add("Chirag");
        v.add("Devansh");
        v.add("Nishchith");
        
        System.out.println("Vector is " + v);
        
        //addall()
        Vector arr = new Vector();
         
        // copying all element of array list int0 vector
        arr.addAll(v);
        System.out.println("vector arr:" + arr);
       
       // check whether vector contains "Nishchith"
       if(v.contains("Nishchith"))
       System.out.println("Nishchith exists");
       
       //equals

        Vector v1 = new Vector();         
        v1.add("Shivam");
        v1.add("Chirag");
        v1.add("Devansh");
        v1.add("Nishchith");
        System.out.println(v.equals(v1);
    }
}
```


Output
```
Vector is [Shivam, Chirag, Devansh, Nishchith]
vector arr:[Shivam, Chirag, Devansh, Nishchith]
Nishchith exists
true
```



<h1 align="center">Difference between ArrayList and Vector</h1>

|<center>ArrayList</center>|<center>Vector</center>
| :------------- | :------------- |
|1)ArrayList is not synchronized.|1)Vector is synchronized.
|2) ArrayList increments 50% of current array size if number of element exceeds from its capacity.|2)Vector increments 100% means doubles the array size if total number of element exceeds than its capacity
|3) ArrayList uses Iterator interface to traverse the elements.|3)Vector uses Enumeration interface to traverse the elements. But it can use Iterator also.
|4)Is is fast|4)It is comparatively slower.

<br>

<h1>LinkedList</h1>

>Java LinkedList class uses doubly linked list to store the elements. It provides a linked-list data structure

>Java LinkedList class can contain duplicate elements.

>Java LinkedList class maintains insertion order.

>Java LinkedList class can be used as list, stack or queue.

###  Operations

|<center>Function</center>  |<center>What it does?</center>  |  <center> Complexity </center>
| :------------- | :------------- | :------------- |
|void clear()   | It is used to remove all of the elements from this list.|O(1)
|void add(int index, Object element) | It is used to insert the specified element at the specified position index in a list.|O(1) if added at the end,O(n) if added in the interior
|int indexOf(Object o) | It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element |O(n)
|int lastIndexOf(Object o)  |It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.in|O(n)
|Object[] toArray()  |It is used to return an array containing all of the elements in this list in the correct order.|O(n)
|Object clone()  | It is used to return a shallow copy of an ArrayList.|O(n)
|void trimToSize() |It is used to trim the capacity of this ArrayList instance to be the list's current size.|O(n)
|void addFirst(Object o)|It is used to insert the given element at the beginning of a list.|O(1)
|void addLast(Object o) |It is used to insert the given element at the ending of a list.|O(1)
|int size() |It is used to return the number of elements in a list|O(1)
|Object getFirst()|It is used to return the first element in a list.|O(1)
|Object getLast()|It is used to return the last element in a list.|O(1)



### Implementation of LinkedList

<br>

```java
// declaration
//eg
LinkedList<String> al=new LinkedList<String>();

```


```java
    import java.util.*;  
    public class LinkedList_Demo{  
     public static void main(String args[]){  
      
      LinkedList<String> al=new LinkedList<String>();  
      al.add("Neel");  
      al.add("Devansh");  
      Iterator<String> itr=al.iterator();  
      while(itr.hasNext()){  
       System.out.println(itr.next());  
      }  
     System.out.println();
 
     //addfirst and last
     
     al.addFirst("chirag");
     al.addLast("hello");
     Iterator<String> itr2 = al.iterator();
     while(itr2.hasNext()){  
       System.out.println(itr2.next());  
     }  
     }  
    }  
	
```
Output:
```
Neel
Devansh

chirag
Neel
Devansh
hello
```

>>>>>>> 3be3264eae84fa93890cb1b9abfad8b78b91b639
