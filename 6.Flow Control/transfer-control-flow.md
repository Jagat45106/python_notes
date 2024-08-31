			=======================================================
					Transfer Flow Statements 
			=======================================================
=>The purpose of Transfer Flow Statements is that "To transfer the control of PVM from One  Part of the Program to 
    another part of the Program".
=>In Python Programming, we have 4 Types of Transfer Flow Statements . They are

			1. break
			2. continue
			3. pass
			4. return
====================================================================================




			==============================================
					1. break statement
			==============================================
=>break is a key word
=>break keyword must be used always inside of loops otherwise we get Syntax error
=>The purpose of break statement is that "To terminate the execution of loop logically when certain condition is satisfied  and  PVM control comes of corresponding loop and executes other statements in the program".
=>when break statement takes place inside for loop or while loop then PVM will not execute corresponding else block(bcoz loop is not becoming False)  but it executes other statements in the program.
=>Syntax1:
-------------------
			for varname  in Iterable_object:
			       ------------------------------
			       if (test cond):
			              break
			------------------------------
			------------------------------
------------------
=>Syntax2:
-------------------
			while(Test Cond-1):
			       ------------------------------
			       if (test cond-2):
			              break
			------------------------------
			------------------------------
==========================================X===================================



#Program for Demonstrating the need of break stmt
#BreakStmtEx1.py
s="PYTHON"
print('By using For Loop')
for ch in s:
    print("\t{}".format(ch))
else:
    print("i am from else part of for loop")
print("-------------------------------------")
#My Requirement today is to display "PYTH" without Indexing and Slicing
for ch in s: # s=PYTHON
    if(ch=="O"):
        break
    else:
        print("{}".format(ch),end="")
else:
    print("i am from else part of for loop")
print()
print("-------------------------------------")






#Program for Demonstrating the need of break stmt
#BreakStmtEx2.py
s="PYTHON"
print('By using while Loop')
i=0
while(i<len(s)):
    print("\t{}".format(s[i]))
    i=i+1
else:
    print("I am from else part of while loop")
print("---------------------------------------------")
#My Requirement today is to display "PYTH" without Indexing and Slicing
i=0
while(i<len(s)): # s=PYTHON
    if(s[i]=="O"):
        break
    print(s[i],end="")
    i=i+1
else:
    print("I am from else part of while loop")
print()
print("---------------------------------------------")



#Program for Demonstrating the need of break stmt
#BreakStmtEx3.py
s="MISSISSIPPI"
print("----------------------------")
#My Requirement today is to display "MISS" without Indexing and Slicing
cnt=0
for ch in s:
    if(ch=="I"):
        cnt=cnt+1
    if(cnt==2):
        break
    print(ch,end="")
print()
print("----------------------------")




#Program for Demnstrating Whether the Given Number is Prime Or Not
#BreakStmtEx4.py
n=int(input("Enter a Number:"))
if(n<=1):
    print("{} is Invalid Input".format(n))
else:
    res="PRIME"
    for i in range(2,n):
        if(n%i==0):
            res="NOT PRIME"
            break
    print("{} is {}".format(n,res))



#Program for Demnstrating Whether the Given Number is Prime Or Not
#BreakStmtEx5.py
n=int(input("Enter a Number:"))
if(n<=1):
    print("{} is Invalid Input".format(n))
else:
    i=2
    res="PRIME"
    while(i<n):
        if(n%i==0):
            res="NOT PRIME"
            break
        i=i+1
    print("{} is {}".format(n,res))





#Program for Demnstrating Whether the Given Number is Prime Or Not
#BreakStmtEx6.py
n=int(input("Enter a Number:"))
if(n<=1):
    print("{} is Invalid Input".format(n))
else:
    i=2
    res=True
    while(i<n):
        if(n%i==0):
            res=False
            break
        i=i+1
    r="Prime" if res else "Not Prime"
    print("{} is {}".format(n,r))




#Program for Demnstrating Whether the Given Number is Prime Or Not
#BreakStmtEx6.py
n=int(input("Enter a Number:"))
if(n<=1):
    print("{} is Invalid Input".format(n))
else:
    i=2
    res=True
    while(i<n):
        if(n%i==0):
            res=False
            break
        i=i+1
    print("{} is {}".format(n,"Prime" if res else "Not Prime"))





