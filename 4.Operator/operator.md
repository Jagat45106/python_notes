
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


## 2. Assignment Operator

=>The purpose of Assigment Operator is that to "To store or Transfer  LHS Variable or LHS Expression Value to RHS 
    Variable"
=>The Symbol for assignment Operator is single equal to ( = )
=>In Python Programming, we can use Assigment Operator in Two Ways. They are

			1. Single Line Assigment
			2. Multi Line Assigment
-----------------------------------------------------------------------------------------------------------------------------
1. Single Line Assigment
-----------------------------------------------------------------------------------------------------------------------------
=>Syntax:     varname=Value
				OR
			varname=Expression
=>The Single Assigment Operator is used for Transfering at a time One Value from RHS to LHS Variable.
------------------------
Examples
------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print(a,b,c)----------10 20 30
--------------
>>> sno=10
>>> name="Rossum"
>>> marks=34.56
>>> print(sno,name,marks)----------10 Rossum 34.56
--------------------------------------------------------------------------------------------------------------------------------------------------
2. Multi Line Assigment
--------------------------------------------------------------------------------------------------------------------------------------------------
=>Syntax:     Var1,Var2,......,Var-n = Val1,Val2,....,Val-n
					OR
		     Var1,Var2,......,Var-n = Expr1, Expr2,.....,Expr-n
=>The Multi  Line Assigment Operator is used for Transfering at a time Multiple Values from RHS to LHS Variables.  
=>In The Above Syntax, the Values of Val1,Val2,....,Val-n(RHS Values) are Assigned to Var1,Var2,......,Var-n(LHS ) 
   Respectively OR the Values of Expr1, Expr2,.....,Expr-n (RHS Values) are Assigned to Var1,Var2,......,Var-n(LHS ) 
   Respectively 
-------------------------------
Examples
-------------------------------
>>> a,b=10,20
>>> c,d,e=a+b,a-b,a*b
>>> print(a,b)-------------------10 20
>>> print("Add=",c)-----------Add= 30
>>> print("Sub=",d)-----------Sub= -10
>>> print("Mul=",e)-----------Mul= 200
--------------------------
>>> sno,name,marks,colname=100,"Rossum",45.67,"JNTU"
>>> print(sno)--------------100
>>> print(name,marks,colname)----------Rossum 45.67 JNTU
-----------------------------
Most IMP---Swapping logic
-----------------------------
>>> a,b=10,20
>>>print(a,b)---------10 20
>>>a,b=b,a
>>>print(a,b)---------20 10


```
#Program for Demonstrating Assignment Operator
#AssigmentOperatorEx1.py
a,b=float(input("Enter First Value:")),float(input("Enter Second Value:"))
sum1,sub1,mul1,div1,fdiv1,mod1,exp1=a+b,a-b,a*b,a/b,a//b,a%b,a**b
print("*"*50)
print("\t\tResults of Assignment Operator")
print("*"*50)
print("\t\t\t{} + {}={}".format(a,b,sum1))
print("\t\t\t{} - {}={}".format(a,b,sub1))
print("\t\t\t{} * {}={}".format(a,b,mul1))
print("\t\t\t{} / {}={}".format(a,b,div1))
print("\t\t\t{} // {}={}".format(a,b,fdiv1))
print("\t\t\t{} % {}={}".format(a,b,mod1))
print("\t\t\t{} ** {}={}".format(a,b,exp1))
print("*"*50)
```

```
#Program for Swapping OR Interchaning of Two values by using Multi Line Assigment
#AssigmentOperatorEx2.py--Logic-1
a,b=input("Enter Value of a:"),input("Enter Value of b:")
print('-'*50)
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
#Swapping Logic by using Multi Line assignment
a,b=b,a # OR   b,a=a,b
print("\tSwapped value of a={}".format(a))
print("\tSwapped value of b={}".format(b))
print('-'*50)

```

```
#Program for Swapping OR Interchaning of Two values
#AssigmentOperatorEx3.py--Logic-2
a=input("Enter Value of a:")
b=input("Enter Value of b:")
print('-'*50)
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
#Swapping Logic
k=a  # here k temp Var, which is Holding the value of a
a=b
b=k
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
```

```
#Program for Swapping OR Interchaning of Two values for Numerical Inetger values Only
#AssigmentOperatorEx4.py--Logic-3
a=int(input("Enter Value of a:"))
b=int(input("Enter Value of b:"))
print('-'*50)
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
#Swapping Logic
a=a+b
b=a-b
a=a-b
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
```

```
#Program for Swapping OR Interchaning of Two values for Numerical Inetger values Only
#AssigmentOperatorEx5.py--Logic-4
a=int(input("Enter Value of a:"))
b=int(input("Enter Value of b:"))
print('-'*50)
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
#Swapping Logic
a=a*b
b=a//b
a=a//b
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
```

```
#Program for Swapping OR Interchaning of Two values for Numerical Inetger values Only
#AssigmentOperatorEx6.py--Logic-5
a=int(input("Enter Value of a:"))
b=int(input("Enter Value of b:"))
print('-'*50)
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
#Swapping Logic
a=a^b
b=a^b
a=a^b
print("\tOriginal value of a={}".format(a))
print("\tOriginal value of b={}".format(b))
print('-'*50)
```

