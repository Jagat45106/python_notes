		=======================================================
					Parameters and Arguments
			=======================================================
---------------------
Parameters
---------------------
=>In Python Programming, we have 2 Types of Parameters. They are
						1. Formal Parameters OR Dummy Parameters
						2. Local Parameters OR Variables

=>Formal Parameter : i) Formal Parameters are Variables used inside of Function Heading.
				      ii) Formal Parameters used for Storing the Inputs coming from function calls.

=>Local Parameter:  i) Local Parameter  are Variables used inside of Function Body
				   ii) Local Parameter used for Storing the Results after function Processing Result 		

=>The Values of 	Formal Parameter	and Local Parameters can be accessed within the corersponding Function Body 
    Only But we can't access in other Part of the Program		   

Example:      def   sumop(a,b):  # here a and b are called formal parameters
			     -----------------------
			     -----------------------
			     c=a+b  # Here c is called Local Parameter OR Local Variable
			     -----------------------
			     -----------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------
Arguments:
-------------------
=>Arguments are the Variables OR Values used inside of Function Calls.
=>Arguments are also called Actual Parameters OR Actual Arguments.
------------------
Examples:
------------------
				a=10
				b=20
				sumop(a,b) # Function call--here a and b are called Arguments
				OR
				sumop(100,200) # Function call--here 100 and 200 are called Argument values

=>The Relationship between Arguments and Parameters is that "Every Value of Argument of function call must pass/send to formal parameter of Function Definition" (This Process is called Arguments Passing Mechanism).



		======================================================
				Types of Arguments OR Parameters
			========================================================
=>Based on The Relationship between Arguments and Parameters is that "Every Value of Argument of function call must pass/send to formal parameter of Function Definition" (This Process is called Arguments Passing Mechanism).
=>In Python, Arguments are Classified into 5 Types. They are

			1. Possitional Arguments
			2. Defualt Arguments
			3. Keyword Arguments
			4. Variable Length Arguments
			5. Keyword Variable Length Arguments





		=========================================================================
						1. Posstional Arguments
			=========================================================================
=>Posstional Arguments Mechanism is the default passing arguments  mechanism used by PVM in Functions for Passing the values of Arguments of Function Call to Formal Parameters of Function Defintion.
=>Possitional Arguments concept says that Every Argument  Value Passing to Every  Formal Parameter Based on their Posstion by maintaining Order and Meaning for Higher Accuracy. In Otherwords The number of arguments must be equal to Number of Formal Parameters.
=>Possitional Arguments concept always used for Passing Specific Data from Function calls to Function Definitions.
 =>PVM gives High Priority for Possitional Arguments
---------------------------------
Syntax:     def  functionname(Param1,Param2,....Param-n):  # Function Definition
			-----------------------------------------------
			-----------------------------------------------
			Block of Statements--perform Operation
			------------------------------------------------
			-----------------------------------------------
-------------
Syntax:       functioname(arg1,arg2,.....,arg-n)  # Function call
-------------
=>Here the values of arg1,arg2,.....,arg-n of  Function call are passing to Param1,Param2,....Param-n of Function Definition Respectively.




		======================================
			2) Default  Parameters (or) arguments
		======================================
=>When there is a Common Value for family of Similar Function Calls then Such type of Common Value(s) must be taken  as default parameter with common value (But not recommended to pass by using Posstional arguments OR Parameters)
----------------------------------------------------------------------------------------
Syntax for Function Definition with Default Parameters
----------------------------------------------------------------------------------------
def   functionname(param1,param2,....param-n-1=Val1, Param-n=Val2):
          ------------------------------------------------------------------
	  ------------------------------------------------------------------

Here param-n-1 and param-n are called "default Parameters".
   and param1,param-2... are called "Formal Possitional parameters".

Rule-: When we use default parameters in the function definition, They must be used as last Parameter(s) otherwise we get Error( SyntaxError: parameter without a default follows parameter with a default)




	============================================
			3) Keyword  Arguments OR Parameters
		============================================
=>In some of the circumstances, we know the function name and formal parameter names and we don't know the order of formal Parameter names and to pass the data / values accurately we must use the concept of Keyword Parameters (or) arguments.
=>The implementation of Keyword Parameters (or) arguments says that all the formal parameter names used as arguments in Function call(s) as keys.

Syntax for function definition:-
-------------------------------------------------
def    functionname(param1,param2...param-n):
         ---------------------------------------------
	 ---------------------------------------------

-------------------------------------------------
Syntax for function call:-
-------------------------------------------------
	functionname(param-n=val-n,param1=val1,param-n-1=val-n-1,.........)

Here param-n=val-n,param1=val1,param-n-1=val-n-1,...... are called Keywords arguments
=>When we specify Keyword arguments before Possitional Arguments in Function Calls(s) then we get 
SyntaxError: positional argument follows keyword argument bcoz PVM gives First Priority for positional arguments.




#Program for Demonstrating Default Arguments
#DefaultArgsEx1.py
def dispstudinfo(sno,sname,marks,crs="PYTHON"):
	print("\t{}\t{}\t{}\t{}".format(sno,sname,marks,crs))

#Main Program
print("-"*50)
print("\tSNO\tNAME\tMarks\tCOURSE")
print("-"*50)
dispstudinfo(10,"RS",45.67) # Function Call with 3 Args
dispstudinfo(20,"TR",75.67) # Function Call with 3 Args
dispstudinfo(30,"DR",25.17) # Function Call with 3 Args
dispstudinfo(40,"KV",11.11) # Function Call with 3 Args
dispstudinfo(50,"JH",33.33) # Function Call with 4 Args
dispstudinfo(60,"DD",23.33,"JAVA") # Function Call with 4 Args
dispstudinfo(70,"SD",53.33) # Function Call with 3 Args
dispstudinfo(crs="HTML",marks=45.67,sname="RR",sno=80) # # Function Call with 4 Keyword Args
print("-"*50)



#Program for Demonstrating Default Arguments
#DefaultArgsEx2.py
def dispstudinfo(sno,sname,marks,crs="PYTHON",city="HYD"):
	print("\t{}\t{}\t{}\t{}\t{}".format(sno,sname,marks,crs,city))

#Main Program
print("-"*50)
print("\tSNO\tNAME\tMarks\tCOURSE\tCITY")
print("-"*50)
dispstudinfo(10,"RS",45.67) # Function Call with 3 Args
dispstudinfo(20,"TR",75.67) # Function Call with 3 Args
dispstudinfo(30,"DR",25.17) # Function Call with 3 Args
dispstudinfo(40,"KV",11.11) # Function Call with 3 Args
dispstudinfo(50,"JH",33.33) # Function Call with 4 Args
dispstudinfo(60,"DD",23.33,"JAVA") # Function Call with 4 Args
dispstudinfo(70,"SD",53.33) # Function Call with 3 Args
dispstudinfo(crs="HTML",marks=45.67,sname="RR",sno=80) # # Function Call with 4 Keyword Args
dispstudinfo(80,"DT",11.23,city="USA")
print("-"*50)



#Program for Demonstrating Keyword Arguments
#KeyWordArgsEx1.py
def  disp(a,b,c,d):
	print("\t{}\t{}\t{}\t{}".format(a,b,c,d))

#Main Program
print("-"*50)
print("\tA\tB\tC\tD")
print("-"*50)
disp(10,20,30,40) # Fucntion Call with 4 Pos Args
disp(d=40,c=30,b=20,a=10) # Fucntion Call with 4 Keyword Args
disp(c=30,d=40,b=20,a=10) # Fucntion Call with 4 Keyword Args
disp(10,20,d=40,c=30) # Fucntion Call with 2 Pos Args and 2 Keyword Args
#disp(d=40,c=30,10,20) ------ SyntaxError: positional argument follows keyword argument
print("-"*50)





#Program for Demonstrating Keyword Arguments
#KeyWordArgsEx2.py
def  disp(a,b,c,d,city="HYD"):
	print("\t{}\t{}\t{}\t{}\t{}".format(a,b,c,d,city))

#Main Program
print("-"*50)
print("\tA\tB\tC\tD\tCity")
print("-"*50)
disp(10,20,30,40) # Fucntion Call with 4 Pos Args
disp(d=40,c=30,b=20,a=10) # Fucntion Call with 4 Keyword Args
disp(c=30,d=40,b=20,a=10) # Fucntion Call with 4 Keyword Args
disp(10,20,d=40,c=30) # Fucntion Call with 2 Pos Args and 2 Keyword Args
#disp(d=40,c=30,10,20) ------ SyntaxError: positional argument follows keyword argument
disp(c=30,a=10,b=20,city="AP",d=40) # Fucntion Call  1 Default and 4 Keyword Args
print("-"*50)



#Program for Demonstrating Postional Arguments
#PosArgsEx1.py
def dispstudinfo(sno,sname,marks):
	print("\t{}\t{}\t{}".format(sno,sname,marks))




#Main Program
print("-"*50)
print("\tSNO\tNAME\tMarks")
print("-"*50)
dispstudinfo(10,"RS",45.67) # Function Call with 3 Args
dispstudinfo(20,"TR",75.67) # Function Call with 3 Args
dispstudinfo(30,"DR",25.17) # Function Call with 3 Args
dispstudinfo(40,"KV",11.11) # Function Call with 3 Args
dispstudinfo(50,"JH",33.33) # Function Call with 3 Args
#dispstudinfo(60,"SD") # Function Call with 2 Args--Gives TypeError
print("-"*50)




#Program for Demonstrating Postional Arguments
#PosArgsEx2.py
def dispstudinfo(sno,sname,marks,crs):
	print("\t{}\t{}\t{}\t{}".format(sno,sname,marks,crs))


#Main Program
print("-"*50)
print("\tSNO\tNAME\tMarks\tCOURSE")
print("-"*50)
dispstudinfo(10,"RS",45.67,"PYTHON") # Function Call with 4 Args
dispstudinfo(20,"TR",75.67,"PYTHON") # Function Call with 4 Args
dispstudinfo(30,"DR",25.17,"PYTHON") # Function Call with 4 Args
dispstudinfo(40,"KV",11.11,"PYTHON") # Function Call with 4 Args
dispstudinfo(50,"JH",33.33,"PYTHON") # Function Call with 4 Args
print("-"*50)




