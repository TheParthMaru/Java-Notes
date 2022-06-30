# Widening or typeconversion

- Smaller data type is implicitly converted to larger data type.

```java
int a = 10;
float f = a;
System.out.println(a); // 10
System.out.println(f); // 10.0
```

# Narrowing or Typecasting

- Converting larger data type to smaller data type.
- May result in loss of data.
- Explicit conversion.

```java
float f = 10.987f;
// int a = f; Compile time error
int a = (int)f;
System.out.println(f); // 10.987
System.out.println(a); // 10
```

# Overflow and Underflow

- Exceeding the range of any data may result in overflow or underflow.

```java
int num1 = Integer.MAX_VALUE; // Stores the maximum possible value for int data type
int num2 = num1 + 1;
System.out.println(num1); // 2147483647 → Maximum value of int
System.out.println(num2); // -2147483648 → Overflow, as we cannot store more than its max limit

int num3 = Integer.MIN_VALUE; // Stores the minimum possible value for int data type
int num4 = num3 - 1;
System.out.println(num3); // -2147483648 → Minimum value of int
System.out.println(num4); // 2147483647 → Underflow, as we cannot store less than its min limit
```
