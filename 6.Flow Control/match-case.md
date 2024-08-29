		================================================================
				 match case statement (Python3.10 Version onwards)
		================================================================
=>match case statement is one of conditional statement available  from Python3.10 Version onwards.
=>The purpose of match case statement is that "To Deal with Pre-Designed Conditions OR Menu Driven Applications".
=>The Menu Driven Applications contains Pre-Designed Conditions
-----------------------------
Syntax:
-------------------------------

			match(Choice Expr):
			       case Choice Label1:
					Block of Stements-1
			       case Choice Label2:
					Block of Stements-2
			       case Choice Label3:
					Block of Stements-3
			       ----------------------------
			       case Choice Label-n:
					Block of Stements-n
			       case _:	 # Default Case Block
					default Block of Statements
			-------------------------------------------------------
			Other Statements in Program
			-------------------------------------------------------
----------------------
Explanation:
----------------------
=>here "match" and "case" are the keywords(proposed)
=>"Choice Expr" represents either int or str  or bool
=>If "Choice Expr" is matching with "case label1" then PVM executes Block of Statements-1 and later executes Other statements in program.
=>If "Choice Expr" is matching with "case label2" then PVM executes Block of Statements-2 and later executes Other statements in program.
=>In General "Choice Expr" is trying to match with case label-1, case label-2,....case label-n then PVM executes corresponding block of statements and later executes Other statements in program.
=>If "Choice Expr" is not matching with  any  of the specified case labels then PVM executes Default Block of Statements which are written under default case block(case _ ) and later executes Other statements in program.
=>Writing default case block is optional and If we write then it must be written at last (Otherwise we get SyntaxError)
=>When we represent multiple case labels under one case then those case labels must be combined with Bitwise OR Operator ( | )  .
-----------------------------------------------------------------------------------------------------------------------------------------------------------------

Examples
---------------------
				****************************************************************************
						Arithmetic Operations
				****************************************************************************
						1. Addition
						2. Substraction
						3. Multiplication
						4. Division
						5. Modulo Division
						6. Exponentiation
						7. Exit
				****************************************************************************
					Enter Ur Choice:
				****************************************************************************
---------------------------------------------------------------------------------------------------------------------------------------------------------------------				
					
					*********************************************************************
						Area of Different Figures
					*********************************************************************
						R. Rectangle
						S. Square
						C. Circle
						T. Triangle
						E. Exit
					*********************************************************************
						Enter Ur Choice: 
					*********************************************************************


Home Work---student must do

					*********************************************************************
						Temprature Conversion Calculator
					*********************************************************************
						1. F to C
						2. F to K
						3. C to F
						4. C to K
						5. K to F
						6. K to C
						7. Exit
					*********************************************************************
						Enter Ur Choice: 1
					*********************************************************************
Fahrenheit to Celcius: C = (F-32) (5/9)
Fahrenheit to Kelvin: K = (F-32) (5/9) + 273.15
Celsius to Fahrenheit: F = C(9/5) + 32
Celsius to Kelvin: K = C + 273.15
Kelvin to Celcius: C = K - 273.15
Kelvin to Fahrenheit: F = (K-273.15) (9/5) + 32




#MatchCaseEx1.py
print("*"*50)
print('Temprature Conversion Calculator')
print("*"*50)
print("\t1. F to C")
print("\t2. F to K")
print("\t3. C to F")
print("\t4. C to K")
print("\t5. K to F")
print("\t6. K to C")
print("\t7. Exit")
print("*"*50)
ch=int(input("Enter Ur Choice:"))
match(ch):
    case 1:
        F=float(input("Enter the Temp in terms of F:"))
        C = (F - 32)*(5 / 9)
        print("\tGiven Temp in terms of F:{}".format(F))
        print("\tEQV . Temp in terms of C:{}".format(C))
    case 2:
        F = float(input("Enter the Temp in terms of F:"))
        K = (F - 32)*(5 / 9) + 273.15
        print("\tGiven Temp in terms of F:{}".format(F))
        print("\tEQV . Temp in terms of K:{}".format(K))
    case 3:
        C = float(input("Enter the Temp in terms of C:"))
        F = C*(9 / 5) + 32
        print("\tGiven Temp in terms of C:{}".format(C))
        print("\tEQV . Temp in terms of F:{}".format(F))
    case 4:
        C = float(input("Enter the Temp in terms of C:"))
        K = C + 273.15
        print("\tGiven Temp in terms of C:{}".format(C))
        print("\tEQV . Temp in terms of K:{}".format(K))
    case 5:
        K = float(input("Enter the Temp in terms of K:"))
        C = K - 273.15
        print("\tGiven Temp in terms of K:{}".format(K))
        print("\tEQV . Temp in terms of C:{}".format(C))
    case 6:
        K = float(input("Enter the Temp in terms of K:"))
        F = (K-273.15)*(9/5) + 32
        print("\tGiven Temp in terms of K:{}".format(K))
        print("\tEQV . Temp in terms of C:{}".format(F))
    case 7:
        print("Thx for Using this program")
    case _:
        print("Ur Selection of Operation is Wrong--try again")
print("Program execution completed")




#MatchCaseEx2.py
s="""*********************************************************************
			Area of Different Figures
*********************************************************************
			R. Rectangle
			S. Square
			C. Circle
    		T. Triangle
			E. Exit
*********************************************************************"""
print(s)
ch=input("Enter Ur Choice:")
match(ch.upper()):
    case "R":
        print("Enter Length and Breadth")
        L,B=float(input()),float(input())
        print("Area of Rect={}".format(L*B))
    case "S":
        s=float(input("Enter Side:"))
        print("Area of Square={}".format(s**2))
    case "C":
        r = float(input("Enter Radius:"))
        print("Area of Circle={}".format(3.14*r ** 2))
    case "T":
        B,H=float(input("Enter Base of Triangle:")),float(input("Enter Hight of Triangle:"))
        print("Area of Triangle={}".format(1/2*B*H))
        print("------------OR---------------------")
        print("Enter Three Side of Triangle")
        a,b,c=float(input()),float(input()),float(input())
        s=(a+b+c)/2
        ta=(s*(s-a)*(s-b)*(s-c))**0.5
        print("Area of Triangle={}".format(ta))
    case "E":
        print("Thx for using this Program")
    case _:
        print("Ur Selection of Operation is wrong--try again")





#MatchCaseEx3.py
s="""*********************************************************************
			Area of Different Figures
*********************************************************************
			R. Rectangle
			S. Square
			C. Circle
    		T. Triangle
			E. Exit
*********************************************************************"""
print(s)
ch=input("Enter Ur Choice:")
match(ch):
    case "R"|'r':
        print("Enter Length and Breadth")
        L,B=float(input()),float(input())
        print("Area of Rect={}".format(L*B))
    case "S"|"s":
        s=float(input("Enter Side:"))
        print("Area of Square={}".format(s**2))
    case "C"|"c":
        r = float(input("Enter Radius:"))
        print("Area of Circle={}".format(3.14*r ** 2))
    case "T"|"""t""":
        B,H=float(input("Enter Base of Triangle:")),float(input("Enter Hight of Triangle:"))
        print("Area of Triangle={}".format(1/2*B*H))
        print("------------OR---------------------")
        print("Enter Three Side of Triangle")
        a,b,c=float(input()),float(input()),float(input())
        s=(a+b+c)/2
        ta=(s*(s-a)*(s-b)*(s-c))**0.5
        print("Area of Triangle={}".format(ta))
    case "E"|'''e''':
        print("Thx for using this Program")
    case _:
        print("Ur Selection of Operation is wrong--try again")
