
					-------------------------------------
						2. continue statement
						-------------------------------------
=>continue is a keyword
=>continue statement is used for making the PVM to go to the top of the loop without executing the following statements which are written after continue statement for that current Iteration only.
=>continue statement  to be used always inside of loops.
=>when we use continue statement inside of loop then else part of corresponding loop also executes provided loop condition becomes false.
-----------------
=>Syntax:-
----------------
			for varname   in Iterable-object:
			     ------------------------------------------
			     if ( Test Cond):
			          continue 
				  ------------ # written after continue statement
				  ------------- # written after continue statement
				  -------------# written after continue statement
			     statement-1  
			     statement-2
			     statement-n
			-----------------------------------------
			-----------------------------------------


=>Syntax:-
----------------
			while (Test Cond):
			     ------------------------------------------
			     if ( Test Cond):
			          continue 
				  -------------- # written after continue statement
				  -------------- # written after continue statement
				  -------------- # written after continue statement
			     statement-1  
			     statement-2
			     statement-n
			-----------------------------------------
			-----------------------------------------




#Program for Demnstrating the need of continue statement
#ContinueStmtEx1.py
s="PYTHON"
print("By using for Loop")
for ch in s:
    print("\t{}".format(ch))
else:
    print("i am from else part of for loop")
print("------------------------------------------")
#My Requirement is to display PYHON
for ch in s:
    if(ch=="T"):
        continue
    print("{}".format(ch),end="")
else:
    print()
    print("i am from else part of for loop")
print("------------------------------------------")



#Program for Demnstrating the need of continue statement
#ContinueStmtEx2.py
s="PYTHON"
print("By using while Loop")
i=0
while(i<len(s)):
    print(s[i])
    i=i+1
else:
    print("i am from else part of for loop")
print("------------------------------------------")
#My Requirement is to display PYHON
i=0
while(i<len(s)):
    if(s[i]=="T"):
        i+=1
        continue
        #i=i+1---Not Recommended to write
    else:
        print(s[i],end="")
        i=i+1
else:
    print()
    print("i am from else part of for loop")
print("------------------------------------------")






#Program for Demnstrating the need of pass without using continue statement
#PassStmtEx1.py
s="PYTHON"
print("By using for Loop")
for ch in s:
    print("\t{}".format(ch))
else:
    print("i am from else part of for loop")
print("------------------------------------------")
#My Requirement is to display PYHON
for ch in s: # s="PYTHON"
    if(ch=="T"):pass
    else:
        print("{}".format(ch),end="")
else:
    print()
    print("i am from else part of for loop")
print("------------------------------------------")





#Program for Demnstrating the need of pass without using continue statement
#PassStmtEx2.py
s="PYTHON"
print("By using while Loop")
i=0
while(i<len(s)):
    print(s[i])
    i=i+1
else:
    print("i am from else part of for loop")
print("------------------------------------------")
#My Requirement is to display PYHON
i=0
while(i<len(s)):
    if(s[i]=="T"):
        i+=1
    else:
        print(s[i],end="")
        i=i+1
else:
    print()
    print("i am from else part of for loop")
print("------------------------------------------")



#Program for Demnstrating the need of continue statement
#ContinueStmtEx5.py
s="PYTHON"
print("By using for Loop")
for ch in s:
    print("\t{}".format(ch))
else:
    print("i am from else part of for loop")
print("------------------------------------------")
#My Requirement is to display PYHN
for ch in s:
    if(ch=="T") or (ch=="O"):
        continue
    print("{}".format(ch),end="")
else:
    print()
    print("i am from else part of for loop")
print("------------------------------------------")




#Program for Demnstrating the need of continue statement
#ContinueStmtEx5.py
s="PYTHON"
print("By using for Loop")
for ch in s:
    print("\t{}".format(ch))
else:
    print("i am from else part of for loop")
print("------------------------------------------")
#My Requirement is to display PYHN
for ch in s:
    if ch in ["T","O"]:
        continue
    print("{}".format(ch),end="")
else:
    print()
    print("i am from else part of for loop")
print("------------------------------------------")




#Program for Demnstrating the need of continue statement
#ContinueStmtEx7.py
lst=[10,-20,30,40,-50,-60,35,-67,-12,0,14]
print("List of +Ve Vaues")
for val in lst:
    if(val<=0):
        continue
    print("\t{}".format(val))
print("-----------------------------------")
print("List of -Ve Vaues")
for val in lst:
    if(val>=0):pass
    else:
        print("\t{}".format(val))
print("-----------------------------------")



#Program for accepting list of Values from KBD and find their sum and avg
#DynamicValuesSumEx1.py
n=int(input("Enter Many Number of Values u want:"))
if(n<=0):
    print("{} is invalid Input".format(n))
else:
    lst=[] # lst=list()---creating empty list for storing Values
    for i in range(1,n+1):
        value=float(input("Enter {} Value:".format(i)))
        lst.append(value)
    else:
        print("-----------------------------------------")
        print("Content of lst={}".format(lst)) # [10.0, 20.0, 30.0, 40.0, 50.0]
        #Code for finding Sum and Avg of list of Elements
        s=0
        for val in lst:
            s=s+val
        else:
            print("Sum={}".format(s))
            print("Average={}".format(s/len(lst)))
            print("-----------------------------------------")




#Program for accepting list of Values from KBD and find their sum and avg
#DynamicValuesSumEx2.py
print("Enter List of Values (press @ to stop):")
lst=list() # Create an empty list
while(True):
    value=input()
    if(value=="@"):
        break
    lst.append(float(value))
print("--------------------------------------------")
print("List of Elements=",lst)
#Code for finding Sum and Avg of list of Elements
s=0
for val in lst:
    s=s+val
else:
    print("Sum={}".format(s))
    if(len(lst)>0):
        print("Average={}".format(s/len(lst)))
    print("-----------------------------------------")





#Program for Reading the Values dynamically from KBD
#ReadValuesEx1.py
n=int(input("Enter Many Number of Values u want:"))
if(n<=0):
    print("{} is invalid Input".format(n))
else:
    lst=[] # lst=list()---creating empty list for storing Values
    for i in range(1,n+1):
        value=float(input("Enter {} Value:".format(i)))
        lst.append(value)
    else:
        print("Content of lst={}".format(lst))





#Program for Reading the Values dynamically from KBD
#ReadValuesEx2.py
print("Enter List of Values (press @ to stop):")
lst=list() # Create an empty list
while(True):
    value=input()
    if(value=="@"):
        break
    lst.append(float(value))
print("List of Elements=",lst)