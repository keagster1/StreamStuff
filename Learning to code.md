# Learning to Code

Prelude
--

This document is fairly thorough and not all of the information will relate to you so please feel free to jump around as needed.

Introduction
--

Computer Science is a very wide and deep field with seemingly endless topics, ideas, theories, and possibilities. Programming is the reason why millions of lines of data can be processed in seconds. It is the reason why many tasks can be automated. Every company in the world buys or creates software that performs many tedious tasks for them and people are always looking for the next big thing to improve their productivity even more. 

So it is understandable that you would be interested in being a creator of these technologies. There is good moneyin developing and lots of feel-good moments to be had. 

Starting From Scratch
--

Getting started is the most important part of your technical journey. I've seen many avoid computer science because they had a hard time grasping the basics. Well, like most complex things you cannot just simply jump in and expect everything to go smoothly. Properly setting your expectations will ensure that you go a lot further in this field. 

First things first, learn what programming is. Since you may be a complete beginner it is important to make sure that you actually understand what computer science and programming is. So read [this](http://interactivepython.org/courselib/static/pythonds/Introduction/WhatIsComputerScience.html) to learn what Computer Science is, and read [this](http://interactivepython.org/courselib/static/pythonds/Introduction/WhatIsProgramming.html) to learn what programming in general is. Feel free to go back to one of those pages and use the arrow keys at the bottom to read more.

Once you have a basic understanding of what Computer Science is, we can move on to learning to program.

Picking a Language
--

Before giving my two cents on which langauges you should learn, bare in mind that if you go to college they will teach a few popular ones. Actaully I'm not going to straight up tell you what to learn first because that is part of the fun. You can start anywhere, just make sure to take advantage of quality online resources.

I will tell you what some of the popular languages are and a few details about each.

Most Popular Modern Languages:
- [Java](https://java.com/en/download/faq/whatis_java.xml)
  
  - Works out of the box. Just download Java and an IDE (I like Eclipse) and you are already good to go!
  - Lots of online help.
  - Good for desktop applications and web services.
- [JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

  - Fun and versatile.
  - Can be very complex and hard to understand to a beginner due to libraries like AJAX and jQuery.
  - Good for website front end and back end. 
  
- [Python](https://www.python.org/doc/essays/blurb/)

  - difficult to setup at first (especially on Windows)
  - Good for websites, console applications, and even GUI applications.
- [C#](https://docs.microsoft.com/en-us/dotnet/csharp/getting-started/introduction-to-the-csharp-language-and-the-net-framework)
  
  - Easy to learn due to Microsofts Visual Studio which includes a very, very good IDE. 
  - Lots of resources to help.
- [C++](https://www.techopedia.com/definition/26184/c-programming-language)
  
  - Used for a lot of video game development.
  - One of the toughest languages to learn.
- [C](https://computer.howstuffworks.com/c1.htm)

  - Most operating systems are made with C!
  - Not as hard to learn as c++ but still rather difficult
  
Time to Learn
--
Once you have chosen the language start absorbing as much knowledge as you can!

Reading will provide you with a lot of information but it's also boring and sometimes it's nice to just dump in and do some hands on. A great resource to do just that is [Codecademy](https://www.codecademy.com/). I actually learned some basics from there myself. 

Furthermore, a great resource for asking questions and finding answers is [stackoverflow](https://stackoverflow.com/)

Pacing Yourself
--
One thing you really want to be careful of is what you try to learn next. If you get to ambitious or excited you may come up with something that is way out of your ability to do. For example, learning the basics of java and then trying to make the next billion dollar game. Immediatly afterwards.

You should always be trying to learn something that is just beyond your current ability.

  - You are more likely to finish the project(s)
  - It will be less frustrating
  - It will accelerate your technical growth
  
Asking Technical Questions Properly:
--
Many people make the mistake of dumping all of there code and saying something "code broke, please fix for me." There are an endless supply of people out there that want to help but almost no one wants to do everything for you. You find the bad side of many people if you just dump code.

Instead take the time to reasearch and document your issue. Actually provide things you have tried and what you think the problem is. A properly formed question is more likely to be takin seriously by the corresponding community. 


Common Programming Interview/Challenge Tasks:
---
[Here](https://simpleprogrammer.com/programming-interview-questions/) is a site that lists 50 programming questions.

I chose 5 and gave potential solutions in Java.

## How do you reverse an array?

``` Java
	public static void main(String[] args) {
		
		String[] arr = {"1", "2", "3", "4", "5"};
		ReverseArray(arr);
	}
	
	public static String[] ReverseArray(String[] arr) {
		// Create temp array with same length as passed in array
		String[] temp = new String[arr.length];
		
		// Loop through passed in array from the last element to the first element
		for(int i = arr.length; i > 0; i--) {
			// Length is counted from 0 in Java so we have to account for that.
			temp[temp.length - i] = arr[i-1];
			
			// Print out
			System.out.println(temp[temp.length - i]);
		}
		
		return temp;
	}
```

## 2. How do you find the length of a singly linked list?

``` Java
package com;

// Program starts here
public static void main(String[] args) {
	// Define first item in list
	CustomLinkedList ll = new CustomLinkedList("This", null);

	// Add children to list
	// There are multiple ways to go about doing this. I chose the worst way. I'll leave it to you to find a better way :D
	ll.setNext(new CustomLinkedList("is", null));
	ll.next().setNext(new CustomLinkedList("a", null));
	ll.next().next().setNext(new CustomLinkedList("Linked", null));
	ll.next().next().next().setNext(new CustomLinkedList("list", null));

	// Get count
	LinkedListLength(ll);
}

// Get length of linked list
public static int LinkedListLength(CustomLinkedList First){
	CustomLinkedList temp = First;
	int count = 0;
	while(temp.next() != null) {
		count++;
		temp = temp.next();
	}
	System.out.println(count);
	return count;
}

// Basic implementation of a linked list
public class CustomLinkedList {
	
	private String data;
	private CustomLinkedList next;
	
	public CustomLinkedList(String data, CustomLinkedList next){
		this.data = data;
		this.next = next;
	}
	
	public void setNext(CustomLinkedList next) {
		this.next = next;
	}
	
	public void setData(String data) {
		this.data = data;
	}
	
	public CustomLinkedList next() {
		return this.next;
	}
	
	public String getData() {
		return this.data;
	}
}


```

## 3. How do you check if a given string is a palindrome?
## 4. How is a binary tree implemented?
## 5. How is a bubble sort algorithm implemented?

