
---
**Operators and Expressions  in Python**
---

=>An Operator is a Symbols which is used to Perform Some Operations on Values OR Objects OR Literals.
=>If any Two OR More Values OR Objects Connected with an Operator then It is called Expression.
=>An Expression is a Collection Objects OR Values Connected with an Operator is called Expression.
=>In Python Programming, we have 7 Types of Operators. They are

			1. Arithmetic Operators
			2. Assigment Operator
			3. Relational Operators ( Comparision Operator )
			4. Logical Operators ( Comparision Operator )
			5. Bitwise Operators--Most Imp
			6. MemberShip Operators
					i) in Operator
					ii) not in Operator
			7. Identity Operators
					i) is Operator
					ii) is not Operator
---------------------------------------------------------------------------------------------------------------------------------------------------
NOTE-1: Python Programming Does not Support Unary Operators ( ++ and - - ) 
-----------
NOTE-2: Python Programming Does not Support Ternary Operator ( ?  :  ) of C, Java and C#.net Lang.
------------
NOTE:3: Python Programming is Having Own Ternary Operator ( if..else Operator )
-------------
NOTE:4: Python Programming Having Short Hand Operatiors Like ( +=, -=, *=, /=.....etc)



**1. Arithmetic Operators**

=>The purpose of Arithmetic Operators is that "To Perform Arithmetic Operations such as Addition, Substraction, 
     Multiplcation ...etc"
=>If Two Or More Values Connected with Arithmetic Operators then It is Called Arithmetic Expression.
=>In Python Programming , we have 7 Types of Arithmetic Operators. They are Given in the following table.
---------------------------------------------------------------------------------------------------------------------------------------------------------------
SLNO	SYMBOL			MEANING		EXAMPLES   a=10  b=3
---------------------------------------------------------------------------------------------------------------------------------------------------------------
1.		+				Addition			print(a+b)---------13

2.		-				Substraction		print(a-b) ----------7

3.		*				Multiplication		print(a*b)----------30

4.		/				Division			print(a/b)----------3.3333333333333335
					     (float quotient)

5.		//				Floor Division	print(a//b)---------3
					    (Integer Quotient)

6.		%				Modulo Division	print(a%b)---------1
						(Remainder)

7.		**				Exponentiation	print(a**b)---------1000
						(Power Operator)

NOTE:  a+b, a-b, a*b, a/b , a//b, a%b and a**b are Called Arithmetic Expression.




#Program for Demnstarting the Functionality of Arithmetic Operators
#ArithmeticOperatorsEx1.py
a=float(input("Enter Value of a:"))
b=float(input("Enter Value of b:"))
print("*"*50)
print("\tArithmetic Operators Results")
print("*"*50)
print("\t\tSum({},{})={}".format(a,b,a+b))
print("\t\tSub({},{})={}".format(a,b,a-b))
print("\t\tMul({},{})={}".format(a,b,a*b))
print("\t\tDiv({},{})={}".format(a,b,a/b))
print("\t\tFloorDiv({},{})={}".format(a,b,a//b))
print("\t\tModDiv({},{})={}".format(a,b,a%b))
print("\t\tExp({},{})={}".format(a,b,a**b))
print("*"*50)




#Program for Cal Square Root of Given Number hy using sqrt() of math module
#ArithmeticOperatorsEx2.py
import math
n=float(input("Enter a Number for Finding Square Root:"))
sqrtval=math.sqrt(n)
print("sqrt({})={}".format(n,sqrtval))
print("----------------OR------------------")
print("sqrt({})={}".format(n,round(sqrtval,2)))
print("----------------OR------------------")
print("sqrt(%0.2f)=%0.2f" %(n,sqrtval))



#Program for Cal Square Root of Given Number without using sqrt() of math module
#ArithmeticOperatorsEx3.py
n=float(input("Enter a Number for Finding Square Root:"))
sqrtval=n**0.5  # OR  sqrtval=n**(1/2)
print("sqrt({})={}".format(n,sqrtval))
print("----------------OR------------------")
print("sqrt({})={}".format(n,round(sqrtval,2)))
print("----------------OR------------------")
print("sqrt(%0.2f)=%0.2f" %(n,sqrtval))



#Program for Calculating  "a to the power m"
# Here a is called Base and m is calld Power
#ArithmeticOperatorsEx4.py
a=float(input("Enter Base:"))
m=float(input("Enter Power:"))
res=a**m
print("power({},{})={}".format(a,m,res))
print("--------------OR--------------------")
print(f"power({a},{m})={a**m}")
print("--------------OR--------------------")
print(f"power({a},{m})={round(a**m,2)}")
