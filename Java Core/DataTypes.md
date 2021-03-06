## Data Types

- Primitive Type
They have no methods
They are not objects
They do not need an invocation to be created
short, int, char, boolean

- Object Type
Commonly called wrapper
With methods
They need an invocation to be created
Types of the standard library - String, it is for text chain others are (Scanner, TreeSet, ArrayList ...), include Classes, Intefaces and Arrays.
User-defined types, example (Car, Bus, People etc)
Array types - vector or matrix type elements, they are special objects that lack methods
Wrapper types, the same as primitive types but as objects (Byte, Short, Integer etc.)

Note: ```The difference between int and Integer is that Integer being a wrapper allows null```

<p align="center">
<img height="450" src="https://user-images.githubusercontent.com/13514156/120518760-855ee980-c397-11eb-8fc2-84834caf286a.jpeg">
</p>

<p align="center">
<img height="450" src="https://user-images.githubusercontent.com/13514156/120518815-96a7f600-c397-11eb-8a32-eb8498f14de1.jpeg">
</p>

There are 8 types of primitive data types:

- boolean data type
- byte data type
- char data type
- short data type
- int data type
- long data type
- float data type
- double data type

<p align="center">
<img height="450" src="https://user-images.githubusercontent.com/13514156/120518877-a6bfd580-c397-11eb-954d-01ecb05d631d.jpeg">
</p>

**Boolean Data Type**
The Boolean data type is used to store only two possible values: true and false. This data type is used for simple flags that track true/false conditions.

The Boolean data type specifies one bit of information, but its "size" can't be defined precisely.

Example: 
```java
Boolean one = false
```

**Byte Data Type**
The byte data type is an example of primitive data type. It isan 8-bit signed two's complement integer. Its value-range lies between -128 to 127 (inclusive). Its minimum value is -128 and maximum value is 127. Its default value is 0.

The byte data type is used to save memory in large arrays where the memory savings is most required. It saves space because a byte is 4 times smaller than an integer. It can also be used in place of "int" data type.

Example: 
```java
byte a = 10, byte b = -20
```

**Short Data Type**
The short data type is a 16-bit signed two's complement integer. Its value-range lies between -32,768 to 32,767 (inclusive). Its minimum value is -32,768 and maximum value is 32,767. Its default value is 0.

The short data type can also be used to save memory just like byte data type. A short data type is 2 times smaller than an integer.

Example:
```java
short s = 10000, short r = -5000
```

**Int Data Type**
The int data type is a 32-bit signed two's complement integer. Its value-range lies between - 2,147,483,648 (-2^31) to 2,147,483,647 (2^31 -1) (inclusive). Its minimum value is - 2,147,483,648and maximum value is 2,147,483,647. Its default value is 0.

The int data type is generally used as a default data type for integral values unless if there is no problem about memory.

Example: 
int a = 100000, int b = -200000

**Long Data Type**
The long data type is a 64-bit two's complement integer. Its value-range lies between -9,223,372,036,854,775,808(-2^63) to 9,223,372,036,854,775,807(2^63 -1)(inclusive). Its minimum value is - 9,223,372,036,854,775,808and maximum value is 9,223,372,036,854,775,807. Its default value is 0. The long data type is used when you need a range of values more than those provided by int.

Example:
```java 
long a = 100000L, long b = -200000L
``` 

**Float Data Type**
The float data type is a single-precision 32-bit IEEE 754 floating point.Its value range is unlimited. It is recommended to use a float (instead of double) if you need to save memory in large arrays of floating point numbers. The float data type should never be used for precise values, such as currency. Its default value is 0.0F.

Example: 
```java
float f1 = 234.5f
```

**Double Data Type**
The double data type is a double-precision 64-bit IEEE 754 floating point. Its value range is unlimited. The double data type is generally used for decimal values just like float. The double data type also should never be used for precise values, such as currency. Its default value is 0.0d.

Example: 
```java
double d1 = 12.3
```

**Char Data Type**
The char data type is a single 16-bit Unicode character. Its value-range lies between '\u0000' (or 0) to '\uffff' (or 65,535 inclusive).The char data type is used to store characters.

Example: 
```java
char letterA = 'A'
```

### Type casting**

Type casting is when you assign a value of one primitive data type to another type.

In Java, there are two types of casting:

Widening Casting (automatically) - converting a smaller type to a larger type size
byte -> short -> char -> int -> long -> float -> double

Narrowing Casting (manually) - converting a larger type to a smaller size type
double -> float -> long -> int -> char -> short -> byte
