	============================================================
				 Local and Global Variables 
		============================================================
-----------------------
Local variables
----------------------
=>Local variables are used in Function Body
=>The Purpose of Local Variables is that "To store Temporary Results after Function Processing".
=>Local Variables can be accessed inside of Corresponding function definition only but not possible to access other 
    part of the program (Local Access )
------------------------
Global Variables
------------------------
=>Global Variables are those which are used for Providing Common Value for all Different Function Definitions 
    (Global Access)
=>In Memory Management point of view, Global Variable Values takes Less Memory Space.
=>Global Variables to be defined before all the function calls(Don't Consider Function Definitions). So that we can 
    access global variable values in all those Function definitions.
=>Syntax:
---------------
			def  fun1():
			     ------------
			     ------------
			def  fun2():
			     ------------
			     ------------
			------------------
			------------------
			def  fun-n():
			     ------------
			     ------------

#Main Program
Var1=Val1
Var2=val2
--------------
Var_n=Val_n # Here Var1,Var2,.....Var-n are called Global Variables
fun1() # Function Call-1
fun2() # Function Call-2
-------
fun-n() # Function Call-n

Hence Var1,Var2,.....Var-n are the Global Variables defined before Function Calls. 
so that We can access those values inside of corresponding Function Definitions.



	======================================
				global key word  
		======================================
=>When we want MODIFY the GLOBAL VARIABLE values in side of function defintion  then global variable names must be preceded with 'global' keyword otherwise we get "UnboundLocalError: local variable names referenced before assignment"
------------
Syntax:
-----------
	var1=val1
	var2=val2
	var-n=val-n    #  var1,var2...var-n are called global variable names.
	------------------
	def   fun1():
		------------------------
		global var1,var2...var-n
		# Modify var1,var2....var-n
	    --------------------------
	def   fun2():
	       ------------------------
	        global var1,var2...var-n
	     # Modify var1,var2....var-n
	       ---------------------------------

NOTE: To MODIFY Global variable Values inside of Function Definition, we use global Keyword (Mandatory to write)
NOTE: To ACCESS Global variable Values inside of Function Definition, we Don't use global Keyword



#Program for Demonstrating the need of global Keyword
#GlobalKwdEx1.py

def incr():
	global a
	a=a+1

def updateval():
	global a
	a=a*2

#Main Program
a=10 # Global variable
print("Main Program-->Val of a before incr()={}".format(a)) # 10
incr() # Function Call
print("Main Program-->Val of a after incr()={}".format(a))  # 11
updateval()
print("Main Program-->Val of a after updateval()={}".format(a))  # 22




#Program for Demonstrating the need of global Keyword
#GlobalKwdEx2.py
def modify1():
	global a,b
	a=a+1
	b=b+1
def modify2():
	#global a,b---No need to write global kwd bcoz we are just accessing global var but not doing modifications
	c=a*2
	d=b*2
	print("Local Var vals c={}  d={}".format(c,d))

#Main Program
a,b=10,20 # Global variables
print("Main Program--> before modify1() a={},b={}".format(a,b)) # 10 20
modify1() # Function Call
print("Main Program--> after modify1() a={},b={}".format(a,b)) # 11 21
modify2()
print("Main Program--> after modify2() a={},b={}".format(a,b)) # 11 21



#Program for Demonstrating the Need of Global Variables
#GlobalLocalVarEx1.py
def learnAI():
	sub1="AI"   # here sub1 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub1,lang))
	#print(sub2)----we can't access sub2 bcoz sub2 is local in other function
def learnML():
	sub2="ML" # here sub2 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub2,lang))
	#print(sub1)-----we can't access sub1 bcoz sub1 is local in other function

#Main Program
lang="PYTHON" # here lang is called Global Variable
learnAI()
learnML()



#Program for Demonstrating the Need of Global Variables
#GlobalLocalVarEx2.py
lang="PYTHON" # here lang is called Global Variable
def learnAI():
	sub1="AI"   # here sub1 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub1,lang))

def learnML():
	sub2="ML" # here sub2 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub2,lang))

#Main Program
learnAI()
learnML()



#Program for Demonstrating the Need of Global Variables
#GlobalLocalVarEx3.py
def learnAI():
	sub1="AI"   # here sub1 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub1,lang))

lang="PYTHON" # here lang is called Global Variable

def learnML():
	sub2="ML" # here sub2 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub2,lang))

#Main Program
learnAI()
learnML()



#Program for Demonstrating the Need of Global Variables
#GlobalLocalVarEx4.py
def learnAI():
	sub1="AI"   # here sub1 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub1,lang))
	

def learnML():
	sub2="ML" # here sub2 is local variable 
	print("{} Based Applications Developed by Using {} Lang".format(sub2,lang))

#Main Program
#learnAI()----------we can't access global Var lang in learnAI() bcoz It defined after Its Call.
lang="PYTHON" # here lang is called Global Variable
learnML()



