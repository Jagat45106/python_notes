		================================================
			4) Variables Length Parameters (or) arguments
		================================================
=>When we have familiy of multiple Similar function calls with Variable number of values / arguments then with normal python programming, we must define mutiple function defintions. This process leads to more development time. 
=>To overcome this process, we must use the concept of Variable length Parameters .
=>To Impelement,  Variable length Parameters concept, we must define single Function Definition and takes a formal Parameter preceded with a symbol called astrisk ( * param) and the formal parameter with astrisk symbol is called Variable length Parameters  and whose purpose is to hold / store any number of values coming from similar function calls and whose type is <class, 'tuple'>.
---------------------------------------------------------------------------------------------------
Syntax for function definition with Variables Length Parameters:
--------------------------------------------------------------------------------------------------
	def   functionname(list of Posstional formal params,  *param1 , param2=value) :
	        --------------------------------------------------
		--------------------------------------------------

=>Here *param1 is called Variable Length parameter and it can hold any number of argument values (or) variable number of argument values and *param1 type is <class,'tuple'>

=>Rule:- The *param1 must always written at last part of Function Heading and it must be only one (but not multiple)

=>Rule:- When we use Variable length and default parameters  in function Heading, we use default parameter as last and before we use variable length parameter and in function calls we should not use default parameter as Key word argument bcoz Variable number of values are treated as Posstional Argument Value(s) .



	================================================
			5) Key Word Variables Length Parameters (or) arguments
		================================================
=>When we have familiy of multiple function calls with Key Word Variable number of values / arguments then with normal python programming, we must define mutiple function defintions. This process leads to more development time. 
=>To overcome this process, we must use the concept of Keyword Variable length Parameters .
=>To Implement, Keyword Variable length Parameters concept, we must define single Function Definition and takes a formal Parameter preceded with a symbol called double astrisk  ( ** param) and the formal parameter with double astrisk symbol is called Keyword Variable length Parameters  and whose purpose is to hold / store any number of (Key,Value)  coming from similar function calls and whose type is <class, 'dict'>.
---------------------------------------------------------------------------------------------------
Syntax for function definition with Keyword Variables Length Parameters:
---------------------------------------------------------------------------------------------------
	def   functionname(list of formal params,  **param) :
	        --------------------------------------------------
		--------------------------------------------------

=>Here **param is called Keyword Variable Length parameter and it can hold any number of Key word argument values (or) Keyword variable number of argument values and **param type is <class,'dict'>

=>Rule:- The **param must always written at last part of Function Heading and it must be only one (but not multiple)
---------------------------------------------------------------
Final Syntax for defining a Function
---------------------------------------------------------------
def  funcname(PosFormal parms, *Varlenparam, default params, **kwdvarlenparam):
			-------------------------------------------------
			---------------------------------------------------




#Program for Demonstrating the Need of Variable Length Arguments
#VarLengthArgsEx1.py
#This Program will not execute bcoz PVM rememebers Latest Function Defintion only and more over PVM is performing Interpretation process.
def  disp(a,b,c,d,e):  # Function Def-1 with 5 Parms
	print(a,b,c,d,e)

def  disp(a,b,c,d):  # Function Def-2 with 4 Parms
	print(a,b,c,d)

def  disp(a,b,c):  # Function Def-3 with 3 Parms
	print(a,b,c)

def  disp(a,b):  # Function Def-4 with 2 Parms
	print(a,b)

def  disp(a):  # Function Def-5 with 1 Parm
	print(a)

#Main Program
disp(10,20,30,40,50) # Function Call-1 with 5 Args
disp(10,20,30,40) # Function Call-2 with 4 Args
disp(10,20,30) # Function Call-3 with 3 Args
disp(10,20) # Function Call-4 with 2 Args
disp(10) # Function Call-5 with 1 Args




#Program for Demonstrating the Need of Variable Length Arguments
#VarLengthArgsEx2.py
#This Program will  execute
def  disp(a,b,c,d,e):  # Function Def-1 with 5 Parms
	print(a,b,c,d,e)
disp(10,20,30,40,50) # Function Call-1 with 5 Args
#----------------------------------------------------------------------------------------------
def  disp(a,b,c,d):  # Function Def-2 with 4 Parms
	print(a,b,c,d)
disp(10,20,30,40) # Function Call-2 with 4 Args
#----------------------------------------------------------------------------------------------
def  disp(a,b,c):  # Function Def-3 with 3 Parms
	print(a,b,c)
disp(10,20,30) # Function Call-3 with 3 Args
#----------------------------------------------------------------------------------------------
def  disp(a,b):  # Function Def-4 with 2 Parms
	print(a,b)
disp(10,20) # Function Call-4 with 2 Args
#----------------------------------------------------------------------------------------------
def  disp(a):  # Function Def-5 with 1 Parm
	print(a)

disp(10) # Function Call-5 with 1 Args
#----------------------------------------------------------------------------------------------

#This Process is not Recommened 
# bcoz If we have 1000 Similar Family Function Calls then we must Define 1000 Function Defs
#It is One of the Time Consuming Process.
#I expecting 1000 Similar Family Function Calls ---we want to define 1 function def-- then we must go for Variable Length Arguments




#Program for Demonstrating the Need of Variable Length Arguments
#PureVarLengthArgsEx1.py

#Single function def where can store Variable length args
def  disp( *kvr): # Here *kvr is called Variable Length Param and whose type is tuple
	print(kvr,type(kvr))


#Main Program
disp(10,20,30,40,50) # Function Call-1 with 5 Args
disp(10,20,30,40) # Function Call-2 with 4 Args
disp(10,20,30) # Function Call-3 with 3 Args
disp(10,20) # Function Call-4 with 2 Args
disp(10) # Function Call-5 with 1 Args
disp() #  # Function Call-6 with 0 Args



#Program for Demonstrating the Need of Variable Length Arguments
#PureVarLengthArgsEx2.py

#Single function def where can store Variable length args
def  disp( *kvr): # Here *kvr is called Variable Length Param and whose type is tuple
	print("----------------------------------------------")
	print("Number of Values={}".format(len(kvr)))
	for val in kvr:
		print("\t{}".format(val))
	print("----------------------------------------------")


#Main Program
disp(10,20,30,40,50) # Function Call-1 with 5 Args
disp(10,20,30,40) # Function Call-2 with 4 Args
disp(10,20,30) # Function Call-3 with 3 Args
disp(10,20) # Function Call-4 with 2 Args
disp(10) # Function Call-5 with 1 Args
disp() #  # Function Call-6 with 0 Args




#Program for Demonstrating the Need of Variable Length Arguments
#PureVarLengthArgsEx3.py
#Single function def where can store Variable length args
def  disp(sno,sname, *kvr): # Here *kvr is called Variable Length Param and whose type is tuple
	print("----------------------------------------------")
	print("Student Number:{}".format(sno))
	print("Student Name:{}".format(sname))
	s=0
	for val in kvr:
		print("\t{}".format(val))
		s=s+val
	print("--------------------------------------")
	print("\tSum={}".format(s))

#Main Program
disp(100,"RS",10,20,30,40,50) # Function Call-1 with 5 Args
disp(200,"TR",10,20,30,40) # Function Call-2 with 4 Args
disp(300,"DR",10,20,30) # Function Call-3 with 3 Args
disp(400,"JH",10,20) # Function Call-4 with 2 Args
disp(500,"ST",10) # Function Call-5 with 1 Args
disp(600,"KV") #  # Function Call-6 with 0 Args



#Program for Demonstrating the Need of Variable Length Arguments
#PureVarLengthArgsEx4.py
#Single function def where can store Variable length args
def  disp(sno,sname, *kvr,city="HYD"): # Here *kvr is called Variable Length Param and whose type is tuple
	print("----------------------------------------------")
	print("Student Number:{}".format(sno))
	print("Student Name:{}".format(sname))
	print("Student City:{}".format(city))
	s=0
	for val in kvr:
		print("\t{}".format(val))
		s=s+val
	print("--------------------------------------")
	print("\tSum={}".format(s))

#Main Program
disp(100,"RS",10,20,30,40,50) # Function Call-1 with 5 Args
disp(200,"TR",10,20,30,40) # Function Call-2 with 4 Args
disp(300,"DR",10,20,30) # Function Call-3 with 3 Args
disp(400,"JH",10,20) # Function Call-4 with 2 Args
disp(500,"ST",10) # Function Call-5 with 1 Args
disp(600,"KV") #  # Function Call-6 with 0 Args
#disp(700,"DT",city="USA",1.2,2.3,4.5,6.7,city="USA") #  SyntaxError
disp(700,"DT",1.2,2.3,4.5,6.7,city="USA") #  # Function Call-6 with 0 Args





#Program for Demonstrating the need of Keyword Varfiable Length Args
#KeywordVarlengthArgsEx1.py
#This Program will  not execute 
def disp(sno,sname,marks) :# Function Def-1 with 3 Kwd Params
	print(sno,sname,marks)

def disp(eno,ename,sal,dsg): # Function Def-2 with 4 Kwd Params
	print(eno,ename,sal,dsg)

def disp(tno,tname): # Function Def-3 with 2 Kwd Params
	print(tno,tname)

#Main Program
disp(sno=10,sname="RS",marks=67) # Function call-1 with 3 Kwd Args
disp(eno=20,ename="TR",sal=21,dsg="SE") # Function call-2 with 4 Kwd Args
disp(tno=30,tname="KVR") # Function call-3 with 2 Kwd Args




#Program for Demonstrating the need of Keyword Varfiable Length Args
#KeywordVarlengthArgsEx2.py
#This Program will   execute 
def disp(sno,sname,marks) :# Function Def-1 with 3 Kwd Params
	print(sno,sname,marks)

disp(sno=10,sname="RS",marks=67) # Function call-1 with 3 Kwd Args
#----------------------------------------------------------------------------------------------------------
def disp(eno,ename,sal,dsg): # Function Def-2 with 4 Kwd Params
	print(eno,ename,sal,dsg)
disp(eno=20,ename="TR",sal=21,dsg="SE") # Function call-2 with 4 Kwd Args
#----------------------------------------------------------------------------------------------------------
def disp(tno,tname): # Function Def-3 with 2 Kwd Params
	print(tno,tname)
disp(tno=30,tname="KVR") # Function call-3 with 2 Kwd Args



#Program for Demonstrating the need of Keyword Varfiable Length Args
#PureKeywordVarlengthArgsEx1.py

def  disp( **kvr): # Here **kvr is called Keyword Variables Length args and whose type dict
	print(kvr,type(kvr))

#Main Program
disp(sno=10,sname="RS",marks=67) # Function call-1 with 3 Kwd Args
disp(eno=20,ename="TR",sal=21,dsg="SE") # Function call-2 with 4 Kwd Args
disp(tno=30,tname="KVR") # Function call-3 with 2 Kwd Args
disp()



#Program for Demonstrating the need of Keyword Varfiable Length Args
#PureKeywordVarlengthArgsEx2.py

def  disp( **kvr): # Here **kvr is called Keyword Variables Length args and whose type dict
	print("Number of Values={}".format(len(kvr)))
	print("-----------------------------------------------------")
	for key,val in kvr.items():
		print("\t{}--->{}".format(key,val))
	print("-----------------------------------------------------")

#Main Program
disp(sno=10,sname="RS",marks=67) # Function call-1 with 3 Kwd Args
disp(eno=20,ename="TR",sal=21,dsg="SE") # Function call-2 with 4 Kwd Args
disp(tno=30,tname="KVR") # Function call-3 with 2 Kwd Args
disp()


#Program for Demonstrating the need of Keyword Varfiable Length Args
#PureKeywordVarlengthArgsEx3.py
def findtotalmarks(sno,sname,cls,city="HYD",**submarks):
	print("-"*50)
	print("\tStudent Number:{}".format(sno))
	print("\tStudent Name:{}".format(sname))
	print("\tStudent Class:{}".format(cls))
	print("\tStudent City:{}".format(city))
	print("-"*50)
	if(len(submarks)>0):
		print("\tSubjectName\tMarks")
		print("-"*50)
		totmarks=0
		for subject,marks in submarks.items():
			print("\t{}\t\t{}".format(subject,marks))
			totmarks=totmarks+marks
		print("-"*50)
		print("\tTotal Marks={}".format(totmarks))
		print("-"*50)
#Main Program
findtotalmarks(100,"HariPriya","X",Tel=50,Hindi=80,Eng=95,Maths=90,Sci=78,soc=67)
findtotalmarks(200,"Usha","XII",Sanskrit=90,Eng=85,Maths=70,Phy=60,Che=40)
findtotalmarks(300,"Shiva","B.Tech(CSE)",OS=30,DBMS=90,CM=80)
findtotalmarks(400,"Rossum","Research",city="NL")



#Program for Demonstrating the need of Keyword Variable Length Args
#PureKeywordVarlengthArgsEx4.py
def findtotalmarks(sno,sname,cls,*vals,city="HYD",**submarks):
	print("-"*50)
	print("\tStudent Number:{}".format(sno))
	print("\tStudent Name:{}".format(sname))
	print("\tStudent Class:{}".format(cls))
	print("\tStudent City:{}".format(city))
	print("Variable length args={}".format(vals))
	print("-"*50)
	if(len(submarks)>0):
		print("\tSubjectName\tMarks")
		print("-"*50)
		totmarks=0
		for subject,marks in submarks.items():
			print("\t{}\t\t{}".format(subject,marks))
			totmarks=totmarks+marks
		print("-"*50)
		print("\tTotal Marks={}".format(totmarks))
		print("-"*50)
#Main Program
findtotalmarks(100,"HariPriya","X",10,20,30,40,Tel=50,Hindi=80,Eng=95,Maths=90,Sci=78,soc=67)
findtotalmarks(200,"Usha","XII",1.2,2.3,3.4,Sanskrit=90,Eng=85,Maths=70,Phy=60,Che=40)
findtotalmarks(300,"Shiva","B.Tech(CSE)",100,200,OS=30,DBMS=90,CM=80)
findtotalmarks(400,"Rossum","Research",12,3.4,5.6,city="NL")
findtotalmarks(500,"KVR","Trainer",sub1=11,Sub2=22)



