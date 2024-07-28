**In IT, we have Two Types of Programming Languages. They are**

1. Static Typed Programming Languages.
2. Dynamically Typed Programming Languages.

---

### 1. Static Typed Programming Languages.

In Static Typed Programming Languages, It is mandatory to declare the variables along with Data Types otherwise we get compile time errors.

The Limitations of Static Typed Programming Languages are:

1. If the Complex Values are available and if the programmer does know Its Data Types then programmer unable to store those complex values.

2. Once of define a Data Type and stores the value and in further statements that particular Data Types allows to store same type of values only but not able store other types of values bcause it is static typed.

    - **Examples:** C, C++, Java, C#.net....etc 

---

### 2. Dynamically Typed Programming Languages.

In dynamically typed programming languages, It is not necessary to declare the variables bcause these languages execution environment will assign the Data Type dynamically depending on the type of value the User OR programmer enters.

The Advantages of Dynamically Typed Programming Languages are:

1. All types of complex values Data Types are automatically assigned by Python language execution environment
2. One variable can contain different type of value during the execution of the program.

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

**Examples: Python, Java Script**
