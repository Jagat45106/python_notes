**In IT, we have Two Types of Programming Languages. They are**

1. Static Typed Programming Languages.
2. Dynamically Typed Programming Languages.

---

### 1. Static Typed Programming Languages.

In Static Typed Programming Languages, It is mandatory to Declare the Variables along with Data Types otherwise we get Compile Time Errors.  
The Limitations of Static Typed Programming Languages are:
1. If the Complex Values are available and if the Programmer does Know Its Data Types then Programmer Unable to Store those Complex Values.
2. Once of Define a Data Type and stores the value and In Further Statements that Particular Data Types allows to store Same type of Values only But not able store Other Types of Values bcoz It is Static Typed.

    - **Examples:** C, C++, Java, C#.net....etc 

---

### 2. Dynamically Typed Programming Languages.

In Dynamically Typed Programming Languages, It is Not Necessary to Declare the Variables bcoz these Languages Execution environment will assign the Data type dynamically depending on the Type of value the User OR Programmer enters.  
The Advantages of Dynamically Typed Programming Languages are:
1. All types of Complex Values Data types are automatically assigned by Python Lang Execution environment
2. One Variable can contain Different Type of Value during the execution of the Program.

---

**Program Examples**

```
> a=10
> b=20
> c=a+b
> print(a,type(a)) # 10 <class, 'int'>
> print(b,type(b)) # 20 <class, 'int'>
> print(c,type(c)) # 30  <class, 'int'>
--------------------------------
> a=11.4
> b=34.56
> c=a+b
> print(a,type(a))-------------11.4 <class 'float'>
> print(b,type(b))-------------34.56 <class 'float'>
> print(c,type(c))--------------45.96 <class 'float'>

```