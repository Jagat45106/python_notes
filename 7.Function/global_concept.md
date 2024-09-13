============================================
		global  and local variables and globals()
	============================================
=>When we come across same global Variable names and Local Variable Names in same function definition then PVM gives preference for local variables but not for global variables.
=>In this context, to extract / retrieve the values of global variables names along with local variables, we must use globals() and it returns an object of <class,'dict'> and this dict object stores all global variable Names as Keys and global variable values as values of value.

=>Syntax:-
		var1=val1
		var2=val2
		--------------
		var-n=val-n  # var1, var2...var-n are called global Variables
		def    functionname():
		       ------------------------
		       var1=val11
		       var2=val22
		       ------------------------
		       var-n=val-nn  #  var1, var2...var-n are called local Variables
		       # Extarct  the global variables values
		       dictobj=globals()
		       ------------------------
		       globalval1=dictobj['var1']  #  or  dictobj.get("var1") or globals()['var1'] or global().get('var1')
		       globalval2=dictobj['var2']  # or dictobj.get("var2") or globals()['var2']
		       -----------------------------------------------------
		       -----------------------------------------------------



#Program for Demonstrating the Need of globals()
#In this Program PVM is having Clarity in Global and Local Variables
#GlobalsFunsEx1.py
a=10
b=20 # here a,b are global Variables
def  operation():
	x=100
	y=200  # Here x and y are called Local Variables
	c=a+b+x+y
	print("sum=",c)

#Main Program
operation() # Function call



#Program for Demonstrating the Need of globals()
#In this Program PVM  not having the clarify between global and local variables bcoz They have on same name
# we can differentiate by using globals()
#GlobalsFunsEx2.py
a=10
b=20 
c=30
d=40  # here a,b,c,d are global Variables
def  operation():
	a=100
	b=200  
	c=300
	d=400 # Here a  b, c and d are called Local Variables
	x=a+b+c+d+globals()['a']+globals().get('b')+globals()['c']+globals().get('d')
	print("Sum=",x)
	
#Main Program
operation() # Function call




#GlobalsFunsEx3.py
a=10
b=20 #  # here a,b are global Variables
def getglobalvariables():
	dobj=globals() # here dobj is of type <class,dict>
	print("--------------------------------------------------------------------")
	print("Invisible and Programmer-Defined Global Variables")
	print("--------------------------------------------------------------------")
	for gvn,gvv in dobj.items():
		print("\t{}-->{}".format(gvn,gvv))
	print("--------------------------------------------------------------------")
	print("Programmer-Defined Global Variables-way-1")
	print("--------------------------------------------------------------------")
	print("Global Var a:",dobj['a'])
	print("Global Var b:",dobj['b'])
	print("--------------------------------------------------------------------")
	print("Programmer-Defined Global Variables-way-2")
	print("--------------------------------------------------------------------")
	print("Global Var a:",dobj.get('a'))
	print("Global Var b:",dobj.get('b'))
	print("--------------------------------------------------------------------")
	print("Programmer-Defined Global Variables-way-3")
	print("--------------------------------------------------------------------")
	print("Global Var a:",globals().get('a'))
	print("Global Var b:",globals().get('b'))
	print("--------------------------------------------------------------------")
	print("Programmer-Defined Global Variables-way-4")
	print("--------------------------------------------------------------------")
	print("Global Var a:",globals()['a'])
	print("Global Var b:",globals()['b'])
	print("--------------------------------------------------------------------")

#Main Program
getglobalvariables()




