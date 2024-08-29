
			==============================================
				2. for loop  or   for ...else  loop
			==============================================
Syntax1:-
-----------
			for varname  in  Iterable_object:
				----------------------------------------
				Indentation block of stmts
				----------------------------------------
			---------------------------------------------------
			Other statements in Program
			---------------------------------------------------
		
---------------
Syntax2:
---------------
			for   varname   in  Iterable_object:
				----------------------------------------
				Indentation block of stmts
				----------------------------------------
			else:
				----------------------------------------
				else block of statements
				----------------------------------------
			---------------------------------------------------
			Other statements in Program
			---------------------------------------------------

Explanation:
-----------------------
=>Here 'for' , "in" and 'else' are keywords
=>Here Iterable_object can be Sequence(bytes,bytearray,range,str), 
    list(list,tuple),set(set,frozenset) and dict.
=>The execution process of for loop is that " Each of Element of Iterable_object selected , placed in varname and executes Indentation block of statements".This Process will be repeated until all elements of Iterable_object completed.
=> when all the elements of Iterable Object completed  then PVM  comes out of for loop and executes else block of statements which are written under else block 
=>Writing else block is optional.



#ForLoopEx1.py
word=input("Enter Any Word:") # word=PYTHON
print("-"*50)
for val in word:
    print(val)
else:
    print("-"*50)




#ForLoopEx2.py
word=input("Enter Any Word:") # word=PYTHON
print("-"*50)
for k in range(0,len(word)):
    print(word[k])


#ForLoopEx3.py
word=input("Enter Any Word:") # word=PYTHON
print("-"*50)
for val in word[::-1]:
    print(val)
else:
    print("-"*50)



#ForLoopEx4.py
word=input("Enter Any Word:") # word=PYTHON
print("-"*50)
for k in range(len(word)-1,-1,-1):
    print(word[k])
print("--------------OR--------------")
for k in range(-1,-(len(word)+1),-1):
    print(word[k])
    



#Program for List of Even Number within in specified range
#ForLoopEx5.py
n=int(input("Enter the Range in which even numbers to generate:"))
if(n<=0):
    print("{} is Invalid".format(n))
else:
    print("-"*50)
    print("List of Even Numbers within:{}".format(n))
    for v in range(2,n+1,2):
        print(v)
    else:
        print("-" * 50)



#Program for List of Odd Number  in reverse Order within in specified range
#ForLoopEx6.py
n=int(input("Enter the Range in which Odd numbers to generate:"))
if(n<=0):
    print("{} is Invalid".format(n))
else:
    if(n%2==0):
        n=n-1
    print("-"*50)
    print("List of Odd Numbers within:{}".format(n))
    for v in range(n,0,-2):
        print(v)



#Program for Generating Mul table by using for loop
#ForLoopEx7.py
n=int(input("Enter Any Number for Generating Mul Table:"))
if(n<=0):
    print("{} is Invalid Input".format(n))
else:
    print("-"*50)
    print("Mul Table for :{}".format(n))
    print("-" * 50)
    for i in range(1,11):
        print("\t{} x {}={}".format(n,i,n*i))
    else:
        print("-" * 50)




#Program for Finding number of words from line of Text
#ForLoopEx8.py
line=input("Enter Line of Text:")
print("Given Line={}".format(line))
words=line.split()
print("----------------------")
print("Given Words")
for word in words:
    print(word)
print("----------------------")
print("Number of Words=",len(words))
print("----------------------")




#Program for Finding Sum of N Natural Numbers where N is +ve
#ForLoopEx9.py
n=int(input("Enter How Many Natural Numbers sum u want to Find:"))
if(n<=0):
    print("{} is Invalid Input".format(n))
else:
    print("="*50)
    print("Natural Nums Sum within {}".format(n))
    print("=" * 50)
    s=0 # Initial Sum and It is called Additive Identity
    for i in range(1,n+1):
        print("\t{}".format(i**2))
        s+=i
    else:
        print("=" * 50)
        print("Sum=",s)
        print("=" * 50)




