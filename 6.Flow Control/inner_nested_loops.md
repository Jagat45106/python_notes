
		==================================================
						Inner OR Nested Loops
			==================================================
=>The Process of Defining One Loop inside of another Loop is called Inner OR Nested Loop.
=>The Execution Process of Inner Loops is that "For Every Value of Outer Loop, Inner loop Executed  repeteatedly for 
    finite number of times until Inner Loop Test Condition becomes False".
=>In Python Programming, we can use Inner Loops in 4 Ways. They are
----------------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-1:    for loop in for loop
----------------------------------------------------------------------------------------------------------------------------------------------------------------
			for varname1 in Iterable-Object:  # Outer Loop
				---------------------------
				for varname2 in Iterable-Object: # Inner Loop
					------------------------------------
					------------------------------------
				else:
				      -------------------------------------
				      -------------------------------------
			else:
				-------------------------------------
				-------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-2:    while loop in while loop
----------------------------------------------------------------------------------------------------------------------------------------------------------------
			----------------------------------------
			while(Test Cond1):
				------------------------------
				------------------------------
				while(Test Cond2):
					-------------------------
					-------------------------
				else:
					--------------------------
					--------------------------
			else:
				---------------------------------
				---------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-3:   for loop in while loop
----------------------------------------------------------------------------------------------------------------------------------------------------------------
			----------------------------------------
			while(Test Cond1):		# Outer Loop
				------------------------------
				------------------------------
				for varname in Iterable-Object: # Inner Loop
					------------------------------------
					------------------------------------
				else:
				      -------------------------------------
				      -------------------------------------
			else:
				---------------------------------
				---------------------------------


----------------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-4:		while loop in for loop
----------------------------------------------------------------------------------------------------------------------------------------------------------------
			for varname1 in Iterable-Object:  # Outer Loop
				---------------------------
				while(Test Cond2): # Inner loop
					-------------------------
					-------------------------
				else:
					--------------------------
					--------------------------
			else:
				-------------------------------------
				-------------------------------------





#Program for Demonstrating Loop in loop called Inner Loops
#InnerLoopEx1.py=-----for in for loop
for i in range(1,6):
    print("="*50)
    print("Outer Loop: Value of i={}".format(i))
    print("-" * 50)
    for j in range(1,4):
        print("\tInner Loop: Value of j={}".format(j))
    else:
        print("\tOut-off Inner Loop")
        print("-" * 50)
else:
    print("Out-off outer Loop")




#Program for Demonstrating Loop in loop called Inner Loops
#InnerLoopEx2.py=-----while in while loop
i=1
while(i<=5):
    print("="*50)
    print("Outer Loop: Value of i={}".format(i))
    print("-" * 50)
    j=1
    while(j<=3):
        print("\tInner Loop: Value of j={}".format(j))
        j=j+1
    else:
        i=i+1
        print("\tOut-off Inner Loop")
        print("-" * 50)
else:
    print("Out-off outer Loop")






#Program for Demonstrating Loop in loop called Inner Loops
#InnerLoopEx3.py=-----for in while loop
i=5
while(i>=1): # Outer loop
    print("="*50)
    print("Outer Loop: Value of i={}".format(i))
    print("-" * 50)
    for j in range(3,0,-1): # Inner loop
        print("\tInner Loop: Value of j={}".format(j))
    else:
        i=i-1
        print("\tOut-off Inner Loop")
        print("-" * 50)
else:
    print("Out-off outer Loop")





#Program for Demonstrating Loop in loop called Inner Loops
#InnerLoopEx4.py-----while in for loop
for i in range(5,0,-1): # Outer Loop
    print("="*50)
    print("Outer Loop: Value of i={}".format(i))
    print("-" * 50)
    j = 3
    while (j >= 1): # Inner Loop
        print("\tInner Loop: Value of j={}".format(j))
        j = j - 1
    else:
        print("\tOut-off Inner Loop")
        print("-" * 50)
else:
    print("Out-off outer Loop")



#Program for Generating Mul Tables for n numbers where n is +ve
#InnerLoopEx5.py
n=int(input("Enter How Many Mul Tables u want:"))
if(n<=0):
    print("{} is Invalid Input".format(n))
else:
    for num in range(1,n+1): # Outer loop--Supply the Num
        print("------------------------------------")
        print("Mul Table for :{}".format(num))
        print("------------------------------------")
        for i in range(1,11): # Inner Loop generates Mul Table for the number suuplied by outer loop
            print("\t{}x{}={}".format(num,i,num*i))
        else:
            print("------------------------------------")




#Program for Generating Mul Tables for n random numbers where n is +ve
#InnerLoopEx6.py
n=int(input("Enter How Many Mul Tables u want:"))
if(n<=0):
    print("{} is Invalid Input".format(n))
else:
    lst=[] # creating an empty list
    for i in range(1,n+1):
        num=int(input("Enter {} Number:".format(i)))
        lst.append(num)
    else:
        print("Given Numbers:{}".format(lst)) # lst=[11, -12, 14, 19, 0]
        print("-----------------------------------")
        for num in lst: # Outer Loop
            if(num<=0):
                print("{} Is Invalid Input:".format(num))
            else:
                print("-"*50)
                print("Mul Table for :{}".format(num))
                print("-" * 50)
                for i in range(1,11): # Inner loop
                    print("\t{} x {}={}".format(num,i,num*i))
                else:
                    print("-" * 50)








#Program for Obtaining List of Primes from List of Numbers
#InnerLoopEx6.py
n=int(input("Enter How Many Numbers u want:"))
if(n<=0):
    print("{} is Invalid Input".format(n))
else:
    lst=[] # creating an empty list
    for i in range(1,n+1):
        num=int(input("Enter {} Number:".format(i)))
        lst.append(num)
    else:
        print("Given Numbers:{}".format(lst)) # [4, 5, 9, 7, 2]
        print("-----------------------------------")
        ps=[]
        for num in lst: # outer loop--supply the value
            if(num<=1):pass
            else:
                res=True
                for i in range(2,num): # inner loop
                    if(num%i==0):
                        res=False
                        break # makes the PVM to come-out-off inner Loop
                if(res):
                    ps.append(num)
        else:
            print("Primes Numbers")
            print(ps)




#StudentMarksReportEx.py
#Accept Student Number and Validate
while(True):
    sno=input("Enter Student Number:")
    if(sno.isdigit()) and (int(sno) in range(100,201)):
        break
    print("\t{} is Invalid Student Number-try again".format(sno))
#accept name and Validation of name
while(True):
    name=input('Enter Ur Name:') # Guido V2an Rossum
    namewords=name.split() # ['Guido', 'V2an', 'Rossum']
    if(len(namewords)==0):
        print("\tDon't Enter Space---enter Ur Name")
    else:
        res=True
        for word in namewords:
            if(not word.isalpha()):
                res=False
                break
        if(res):
            break
        else:
            print("\t{} is Invalid Name-try again".format(name))

#Accept C Lang Marks and Validate
while(True):
    cm=input("Enter Marks in C:")
    if (cm.isdigit()) and (int(cm) in range(0, 101)):
        break
    print("\t{} is Invalid Marks in C Lang-try again".format(cm))
#Accept C++ Lang Marks and Validate
while(True):
    cppm=input("Enter Marks in C++:")
    if (cppm.isdigit()) and (int(cppm)>=0 and int(cppm)<=100):
        break
    print("\t{} is Invalid Marks in C Lang-try again".format(cppm))
#Accept Python Lang Marks and Validate
while(True):
    pym=input("Enter Marks in Python:")
    if (pym.isdigit()) and (0<=int(pym)<=100):
        break
    print("\t{} is Invalid Marks in C Lang-try again".format(pym))
#Calculate totam Marks and Percentage of Marks
totmarks=int(cm)+int(cppm)+int(pym)
percent=(totmarks/300)*100
#Code for getting Fail student
if(int(cm)<40) or (int(cppm)<40) or (int(pym)<40):
    grade="FAIL"
else:
    if(totmarks in range(250,301)):
        grade="DISTINCTION"
    elif(200<=totmarks<=249):
        grade = "FIRST"
    elif(totmarks>=150 and totmarks<=199):
        grade="SECOND"
    elif(totmarks in range(120,150)):
        grade="THIRD"
print("="*50)
print("STUDENT MARKS REPORT")
print("="*50)
print("\tStudent Number:{}".format(sno))
print("\tStudent Name:{}".format(name))
print("\tStudent Marks in C :{}".format(cm))
print("\tStudent Marks in C++ :{}".format(cppm))
print("\tStudent Marks in PYTHON:{}".format(pym))
print("-"*50)
print("\tStudent total Marks:{}".format(totmarks))
print("\tStudent Percentage of Marks:{}".format(percent))
print("\tStudent Grade:{}".format(grade))
print("="*50)





#Program for Deciding wether the citizen is eligible to vote or not
#VoterEx1.py
age=int(input("Enter Age of Citizen:"))
if(age>=18):
    print("{} Years Citizen is Eligible to vote".format(age))
else:
    print("{} Years Citizen is not Eligible to vote".format(age))




#Program for Deciding wether the citizen is eligible to vote or not
#VoterEx2.py
while(True):
    age=int(input("Enter Age of Citizen:"))
    if(age>=18):
        print("\t{} Years Citizen is Eligible to vote".format(age))
        break
    print("\t{} Years Citizen is not Eligible to vote".format(age))




    