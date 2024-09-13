	==========================================
					comprehension
		==========================================
=>Python is famous for allowing you to write code that’s elegant, easy to write, and almost as easy to read as plain English. One of the language’s most distinctive features is the list comprehension, which you can use to create powerful functionality within a single line of code rather than writing legacy lines of Code.
=>The purpose of List comprehension is that to read the values dynamically from key board separated by a delimeter ( space, comma, colon..etc)  
=>List comprehension is the most effective way for reading the data for list instead tradtional reading the data.
=>Syntax:-        listobj=[ expression   for  varname  in  Iterable_object   if test Cond ] 
=>here expression represents either type casting or mathematical  expression

Examples:
----------------------
print("Enter List of values separated by space:")  # [10 2  22  50  10 4 55  -3  0  22]
lst=  [float(val)  for val  in input().split() ]
print("content of lst",lst)
------------------
Examples:
------------------
lst=[4,3,7,-2,6,3]
newlst=[ val*2  for val  in lst ]
print("new list=",newlst)  # [ 8, 6, 14,-4,12,6 ]



#Program for reading the values from Key board
#ListComprEx1.py
print("Enter List of Values separated by space:")
lst=[  float(val)  for val in input().split()  ]
print(lst,type(lst))



#Program for reading the values from Key board and obtains +Ve Values
#ListComprEx2.py
print("Enter List of Values separated by comma:")
pslst=[  float(val)  for val in input().split(",")  if float(val)>0 ]
print("Enter List of Values separated by comma:")
nglst=[  float(val)  for val in input().split(",")  if float(val)<0 ]
print("List of +Ve Values={}".format(pslst))
print("List of -Ve Values={}".format(nglst))





#Program for reading the values from Key board and Find their squares
#DictComprEx1.py
print("Enter List of Values separated by space:")
dobj={ float(val):float(val)**2   for val in input().split()  }
for num,sqval in dobj.items():
	print("\t{}---->{}".format(num,sqval))




#Program for reading the values from Key board and Find their squares
#DictComprEx2.py
print("Enter List of Values separated by space:")
dobj={ float(val):float(val)**2   for val in input().split() if float(val)>0 }
print("------------------------------------------------")
for num,sqval in dobj.items():
	print("\t{}---->{}".format(num,sqval))
print("------------------------------------------------")




#Program for reading the Words from Key board and Find their length
#DictComprEx3.py
print("Enter List of Words separated by Comma:")
words={ word:len(word)   for word in input().split(",") }
print("-------------------------------------------------------")
for word,wlen in words.items():
	print("\t{}--->{}".format(word,wlen))
print("-------------------------------------------------------")


#Program for reading the values from Key board
#SetComprEx1.py
print("Enter List of Values separated by space:")
s1={  float(val)  for val in input().split()  }
print(s1,type(s1))


#Program for reading the values from Key board
#TupleComprEx1.py
print("Enter List of Values separated by space:")
s1=( float(val)  for val in input().split()  )
print(s1,type(s1)) # Here s1 is an object of <class, generator>
#Convert generator object into tuple object by using tuple()
t1=tuple(s1)
print(t1,type(t1))
