#Prografm adding of Two Numbers by using Functions
#ApproachEx1.py
#INPUT   : Taking from Function Calls
#PROCESS : Done in Function Definition
#RESULT  : Given to Function Call
def sumop(a,b): # here a,b are called Formal Params
    c=a+b  # Here c is called Local Variable
    return c
#Main Program
x=float(input("Enter First value:"))
y=float(input("Enter Second Value:"))
res=sumop(x,y) # Function call
print("sum({},{})={}".format(x,y,res))
print("-----------OR--------------------")
a=float(input("Enter First value:"))
b=float(input("Enter Second Value:"))
c=sumop(a,b) # Function call
print("sum({},{})={}".format(a,b,c))



#Prografm adding of Two Numbers by using Functions
#ApproachEx2.py
#INPUT   : Taking Inside of Function Definition
#PROCESS : Done Inside of Function Definition
#RESULT  : Displayed Inside of Function Definition
def sumop():
    #Accept the Input from KBD
    a=float(input("Enter First Value:"))
    b=float(input("Enter Second Value:"))
    #Process the Input
    c=a+b
    #display the Result
    print("sum({},{})={}".format(a,b,c))

#Main Program
sumop() # Function Call



#Prografm adding of Two Numbers by using Functions
#ApproachEx3.py
#INPUT   : Taking from Function Calls
#PROCESS : Done in Function Definition
#RESULT  : Displayed Inside of Function Definition
def sumop(k,v):
    r=k+v
    print("Sum({},{})={}".format(k,v,r))

#Main Program
a=float(input("Enter First Value:"))
b=float(input("Enter Second Value:"))
sumop(a,b) # Function call


#Prografm adding of Two Numbers by using Functions
#ApproachEx4.py
#INPUT   : Taking Inside of Function Definition
#PROCESS : Done in Function Definition
#RESULT  : Given to Function Call
def sumop():
    # Accept the Input from KBD
    a = float(input("Enter First Value:"))
    b = float(input("Enter Second Value:"))
    # Process the Input
    c = a + b
    #give Result
    return a,b,c # return stmt return either one value OR More Number of Values

#Main Program
k,v,r=sumop() # Function call with Multi Line assigment
print("Sum({},{})={}".format(k,v,r))
print("-----------------------------------")
res=sumop() # Function call with Suingle Line assigment
#here res is type <class, tuple>
print("sum({},{})={}".format(res[0],res[1],res[2]))
print("------------OR-----------------")
print("sum({},{})={}".format(res[-3],res[-2],res[-1]))





#Program for Displaying Iterable Object Data
#IterableObjectDispEx.py
def disp(obj):
    print("-" * 50)
    print("Type of obj=", type(obj))
    print("-" * 50)
    if(type(obj) in [int,float,bool,complex]):
        print("Non-Iterable Object Data={}".format(obj))
    elif(type(obj)!=dict) and type(obj) in [str,bytes,bytearray,range,list,tuple,set,frozenset] :
        for val in obj:
            print("\t{}".format(val))
        print("-" * 50)
    elif(type(obj)==dict):
        for k,v in obj.items():
            print("\t{}--->{}".format(k,v))
    else:
        print("Value of obj=", obj)
    print("-" * 50)

#Main Program
lst=[10,20,"Python","C",True,2+3j]#Iterable Object
disp(lst) # Function Call
tpl=(100,"RS",34.56,True,-34)  #Iterable Object
disp(tpl) # Function Call
s1={10,20,-45,-56,3+4.5j,"HYD"} #Iterable Object
disp(s1) # Function Call
fs1=frozenset({10,20,-45,-56,3+4.5j,"HYD"})#Iterable Object
disp(fs1) # Function Call
d1={1:"Python",2:"C",3:"C++",4:"Java"}#Iterable Object
disp(d1) # Function Call
s="MISSISSIPPI"
disp(s) # Function Call
a=10 #Non-Iterable Object
disp(a)# Function Call
a=10.45 #Non-Iterable Object
disp(a)# Function Call
a=1.5+4.5j #Non-Iterable Object
disp(a)# Function Call
a=True #Non-Iterable Object
disp(a)# Function Call
r=range(10,21,3) #Iterable Object
disp(r)# Function Call
b=bytes([10,20,30,40])  #Iterable Object
disp(b)# Function Call
ba=bytearray([10,20,30,40])  #Iterable Object
disp(ba)# Function Call
a=None
disp(a)# Function Call




#Program for generating Mul Table for a Given Number
#MulTableFunEx.py
def multable(n):
    if(n<=0):
        print("{} is Invalid Input".format(n))
    else:
        print("-"*50)
        print("Mul Table for :{}".format(n))
        print("-" * 50)
        for i in range(1,11):
            print("\t{}x{}={}".format(n,i,n*i))
        print("-" * 50)
#Main Program
n=int(input("Enter a Number for Generating Mul Table:"))
multable(n) # Function Call




#Program getting Unique Values from given word without using set()
#UniqueValuesFun.py
def uniquevalues(value): # value="MISSISSIPPI"
    lst=[]
    for val in value:
        if(val not in lst):
            lst.append(val)
    return lst

#Main Program
word=input("Enter a Word:")
uniqwords=uniquevalues(word)
print("Given Word={}".format(word))
print("Unique Words={}".format(uniqwords))
print("Number of Unique Letters={}".format(len(uniqwords)))
print("Unique Letters Word={}".format("".join(uniqwords)))



#Program fro accepting a Line of Text and Find length of each word
#WordLengthFunEx1.py
def getline():
    line=input("Enter Line of Text:")
    return line

def getwordslength(line): # line=Python is an oop lang
    words=line.split() # words=["Python","is","an","oop","lang"]
    for word in words:
        print("\t{}--->{}".format(word,len(word)))

#Main Program
line=getline() # Function Call
getwordslength(line)



#Program fro accepting a Line of Text and Find length of each word
#WordLengthFunEx2.py
def getline():
    line=input("Enter Line of Text:")
    return line

def getwordslength():
    line=getline() # One Function Call another Function--Funtion Chain
    words=line.split() # words=["Python","is","an","oop","lang"]
    for word in words:
        print("\t{}--->{}".format(word,len(word)))

#Main Program
getwordslength()






#Program fro accepting a Line of Text and Find length of each word
#WordLengthFunEx3.py
def getline():
    line=input("Enter Line of Text:")
    return line
def getwordslength():
    line=getline() # One Function Call another Function--Funtion Chain
    words=line.split() # words=["Python","is","an","oop","lang"]
    return words
def countwordslength(words):
    if(len(words)==0):
        print("No Data Present")
    else:
        d={} # Create an empty dict for storing word and its length
        for word in words:
            d[word]=len(word)
        else:
            print("="*50)
            for word,wordlen in d.items():
                print("\t{}-->{}".format(word,wordlen))
            print("=" * 50)

#Main Program
words=getwordslength()
countwordslength(words) # Function Call





#Program fro accepting a Line of Text and Find length of each word
#WordLengthFunEx4.py
def getline():
    line=input("Enter Line of Text:")
    return line
def getwordslength():
    line=getline() # One Function Call another Function--Funtion Chain
    words=line.split() # words=["Python","is","an","oop","lang"]
    return words
def countwordslength():
    words = getwordslength() # One Function Call another Function--Function Chain
    if(len(words)==0):
        print("No Data Present")
    else:
        d={} # Create an empty dict for storing word and its length
        for word in words:
            d[word]=len(word)
        else:
            print("="*50)
            for word,wordlen in d.items():
                print("\t{}-->{}".format(word,wordlen))
            print("=" * 50)

#Main Program
countwordslength() # Function Call



