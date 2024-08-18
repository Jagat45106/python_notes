
---
**Display the Result of the Python Program on the Console**
---

=>To Display the Result of the Python Program on the Console, we use a Pre-Defined function called print().
=>In Otherwords, print() is used for displaying the Result of Python Program on the Console.
=>print() can be used in 6 Syntaxes. They are
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-1:		print(val1)
				OR
			print(val1,val2,....,val-n)
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>This Syntax is used for Displaying Either One Value or Multiple Values at a time on the console.
---------------------
Examples
---------------------
>>> a=10
>>> print(a)--------------10
>>> a=100
>>> b=200
>>> c=a+b
>>> print(a,b,c)-----------100 200 300
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-2:    print(msg1)
			OR
		    print(msg1,msg2,msg3.......,msg-n)
			OR
		    print(msg1+msg2+......+msg-n)
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>Here msg1,msg2,.....msg-n are calles String Data.
=>Here + is symbol used for Concatenating Two OR More Strings.
=>This Syntax display String Data.
---------------------------
Examples
---------------------------
>>> print("Hello Python")--------------Hello Python
>>> print("Hello",'python')-------------Hello python
>>> print("Hello"+"Python")-----------HelloPython
>>> print("Hello"+" "+"Python")-----Hello Python
>>> print("Python"+3.12)-----------TypeError: can only concatenate str (not "float") to str
>>> print("Python"+str(3.12))--------Python3.12
>>> print("Python",3.12)--------------Python 3.12
>>> print("Python","3.12")-------------Python 3.12
>>> print("Python"+" "+"3.12")-------Python 3.12
>>> print(2+3)------------------------------5
>>> print("2"+"3")-------------------------23
>>> print("2"+"3"+4)----------------------TypeError: can only concatenate str (not "int") to str
>>> print("2"+"3"+str(4))----------------234
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-3: print(Message cum Value)
			OR
		print(Value cum Message)
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>This Syntax display Values Cum Messages OR Messages Cum Values.
--------------------------
Examples
--------------------------
>>>a=10
>>> print("Val of a=",a)--------------Val of a= 10
>>> print("Val of a="+str(a))------Val of a=10
>>> a=10
>>> print(a,"is the val of a")----------10 is the val of a
>>> print(str(a)+" is the val of a")----10 is the val of a
---------------------------------------------------------------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum=",c)--------------sum= 30
>>> print(c,"is the sum")--------30 is the sum
>>> print("sum of ",a," and ",b,"=",c)----sum of  10  and  20 = 30
>>> print("Sum of "+str(a)+" and "+str(b)+"="+str(c))-----Sum of 10 and 20=30
----------------
>>> a=10
>>> b=20
>>> c=30
>>> d=a+b+c
>>> print("sum of ",a,",",b," and ",c,"=",d)-----------sum of  10 , 20  and  30 = 60
>>> print("Sum of "+str(a)+str(",")+str(b)+" and "+str(c)+str("=")+str(d))----Sum of 10,20 and 30=60
---------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum(",a,",",b,")=",c)-------------sum( 10 , 20 )= 30
>>> print("sum("+str(a)+str(",")+str(b)+str(")=")+str(c))-----------sum(10,20)=30
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-4:   print(Message cum Value with format() )
				(OR)
		   print(Value cum Message with format() )
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>This Syntax display Values Cum Messages OR Messages Cum Values by using format()
--------------------------
Examples
--------------------------
>>> a=10
>>> print("Val of a={}".format(a))-------------Val of a=10
>>> print("{} is the val of a".format(a))-----10 is the val of a
---------------------------
>>> a=10
>>> print("Val of a={}".format(a))-----------Val of a=10
>>> print("{} is the val of a".format(a))----10 is the val of a
----------------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum={}".format(c))------------sum=30
>>> print("sum of {} and {}={}".format(a,b,c))-----sum of 10 and 20=30
>>> print("sum({},{})={}".format(a,b,c))---------sum(10,20)=30
>>> a=10
>>> b=20
>>> c=30
>>> d=a+b+c
>>> print("sum of {},{} and {}={}".format(a,b,c,d))----sum of 10,20 and 30=60
				OR
>>> a=10
>>> print(f"val of a={a}")----------------val of a=10
--------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print(f"sum of {a},{b}={c}")-----------sum of 10,20=30
>>> print(f"sum({a},{b})={c}")-------------sum(10,20)=30
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-5:    print(Message cum Value with format Specifiers)
-----------------------------------------------------------------------------------------------------------------------------------------------------------

=>Here Format Spefiers represents what type value we are displaying
=>Here %d Represents Integer Data
=>here %f Represents Floating Point Data.
=>here %s Represnts str data.
=>If any value does not contain Format Specifier then we must that Value into str type by using str() and use %s.
---------------------------
Examples
---------------------------
>>> a=10
>>> print("Val of a=%d" %a)------------Val of a=10
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum of %d and %d=%d" %(a,b,c))----sum of 10 and 20=30
>>> print("sum(%d,%d)=%d" %(a,b,c))-----sum(10,20)=30
>>> print("sum(%f,%f)=%f" %(a,b,c))----------sum(10.000000,20.000000)=30.000000
>>> print("sum(%0.2f,%0.2f)=%0.3f" %(a,b,c))----sum(10.00,20.00)=30.000
--------------------
>>> a=1.2
>>> b=2.3
>>> c=a+b
>>> print("sum(%f,%f)=%f" %(a,b,c))------------sum(1.200000,2.300000)=3.500000
>>> print("sum(%0.2f,%0.2f)=%0.3f" %(a,b,c))------sum(1.20,2.30)=3.500
>>> a=1.2
>>> b=2.3
>>> c=a+b
>>> print("sum(%f,%f)=%f" %(a,b,c))----------sum(1.200000,2.300000)=3.500000
>>> print("sum(%0.2f,%0.2f)=%0.3f" %(a,b,c))---sum(1.20,2.30)=3.500
>>> a=2.345678
>>> print("val of a=%f" %a)-----------val of a=2.345678
>>> print("val of a=%0.20f" %a)-----val of a=2.34567799999999992977
-----------------
>>> sno=10
>>> sname="Rossum"
>>> marks=3.4
>>> print("My Number is %d and Name is %s and Marks is %0.2f" %(sno,sname,marks))
			My Number is 10 and Name is Rossum and Marks is 3.40
>>> lst=[10,"Rossum",34.56]
>>> print("Content of lst={}".format(lst))-----------Content of lst=[10, 'Rossum', 34.56]
>>> print("Content of lst=%d" %lst)------------TypeError: %d format: a real number is required, not list
>>> print("Content of lst=%s" %str(lst))--------Content of lst=[10, 'Rossum', 34.56]
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-6 : print(value,end="Delimiter")
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>This Syntax is used for Displaying the Horizontally by giving space with Specified Delimter.
=>Here delimeter can be eithet space or -> or any Symbol
-------------------------
Examples
-------------------------
r=range(10,20)
>>> for i in r:
...		print(i,end=" ")  ---------   10 11 12 13 14 15 16 17 18 19
------------------------
>>> for i in r:
...		print(i,end="->")------10->11->12->13->14->15->16->17->18->19



---
**Reading the Data Dynamically from Key Board--Most Imp**
---

=>To Read the Data Dynamically from Key Board , we have 2 Pre-Defined Functions. They are
				1. input()
				2. input(Message)
--------------------------------------------------------------------------------------------------------------------------------------------------------
1. input()
--------------------------------------------------------------------------------------------------------------------------------------------------------
=>Syntax:    varname=input()
=>This is Used Reading any Type of Data from Keyboard and Placed in LHS Variable and whose type is <class,str>
=>We can convert str type value in Our Desired Type by using Type Casting Functions.
--------------------------------------------------------------------------------------------------------------------------------------------------------
2. input(Message)
--------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax:    varname=input(Message)
=>Here Message Represents User-Prompting Message
=>This Syntax is used for Reading any type of Data from Key Board and  Placed in LHS Variable and whose type is <class,str>  and with this Syntax additionally we can display User-Prompting Message.



#Program for Reading the from KeyBaord and Display
#DataReadEx1.py
print("Enter any Value:")
x=input()
print(x,type(x))



#Program for Reading the from KeyBaord and Display
#DataReadEx2.py
x=input("Enter Any Value:")
print(x,type(x))


#Program for Reading the data from KeyBaord and  convert into float or int
#DataReadEx3.py
x=input('Enter Any value:')
print(x,type(x))
#Convert x into int type
y=float(x)
print(y, type(y))
print("---------------OR-----------------")
y=float(input("Enter Another Value:"))
print(y, type(y))


#DataReadEx4.py
#Program for Cal Area of Rect
#Area of Rect = Length x Breadth
length=float(input("Enter Length:"))
breadth=float(input("Enter Breadth:"))
#Cal Area of Rect
area=length*breadth
#Display the Result
print("*"*50)
print("\t\tLength={}".format(length))
print("\t\tBreadth={}".format(breadth))
print("\t\tArea of Rect={}".format(area))
print("*"*50)


#Program for Finding Multiplication or Product Two Numbers
#DataReadEx5.py
a=float(input("Enter First Value:"))
b=float(input("Enter Second Value:"))
#Multiply
c=a*b
print("product({},{})={}".format(a,b,round(c,2)))



#Program for Finding Multiplication or Product Two Numbers
#DataReadEx6.py
print("Enter Two values:")
x=float(input())
y=float(input())
z=x*y
print("product({},{})={}".format(x,y,round(z,2)))


#Program for Finding Multiplication or Product Two Numbers
#DataReadEx7.py
print("Enter Two values:")
z=float(input())*float(input())
print("Product={}".format(round(z,2)))



#Program for Finding Multiplication or Product Two Numbers
#DataReadEx8.py
z=float(input("Enter First Value:"))*float(input("Enter Second Value:"))
print("Product={}".format(round(z,2)))



#Program for Finding Multiplication or Product Two Numbers
#DataReadEx8.py
print("Product={}".format(round(float(input("Enter First Value:"))*float(input("Enter Second Value:")),2)))


#DataReadEx10.py
#Program for Cal Perimter of Rect
#Area of Rect = 2(Length + Breadth)
length=float(input("Enter Length:"))
breadth=float(input("Enter Breadth:"))
#Cal Area of Rect
per=2*(length+breadth)
#Display the Result
print("*"*50)
print("\t\tLength={}".format(length))
print("\t\tBreadth={}".format(breadth))
print("\t\tPerimeter of Rect={}".format(per))
print("*"*50)




