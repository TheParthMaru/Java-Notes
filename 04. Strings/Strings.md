# Strings in Java

- An object used to represent sequence of character values.
- An array of characters works as same as string.

```java
char ch[] = {'p', 'a', 'r', 't', 'h'};
String s = new String(ch);

// is same as

String s = "parth";
```

- The `java.lang.String` class implements `Serializable`, `Comparable` and `CharSequence` interfaces.
- The `CharSequence` interface is used to represent the sequence of characters.
- We can create string with `String`, `StringBuffer` and `StringBuilder` classes as these classes implement `CharSequence` interface.

## Ways to create a string

### 1. String literal

- String is created using double quotes.

```java
String name = "Parth";

String s1 = "welcome";
String s2 = "welcome"; // Does not create a new instance
```

- Each time you create a string literal, the JVM checks the "string constant pool" first.
- If the string already exists in the pool, a reference to the pooled instance is returned.
- If the string doesn't exist in the pool, a new string instance is created and placed in the pool.
- String objects are stored in a special memory area known as the string constant pool.
- We use string literal to make Java more memory efficient as no new objects are created if it already exists in the string constant pool.

![picture 1](../images/f972873933ace4b38539c62c4dd28b559d8b1c875e994933fd22d7ff52b8320e.png)

### 2. new keyword

```java
String s = new String("Parth");
```

- In such case, JVM will create a new string object in normal (non-pool) heap memory, and the literal "Parth" will be placed in the string constant pool.
- The variable s will refer to the object in a heap (non-pool).

## List of string class methods

| Method                                                                                  | Description                                                      |
| --------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| `char charAt(int index)`                                                                | returns char value for the particular index                      |
| `int length`                                                                            | returns string length                                            |
| `static String format(String format, Object... args)`                                   | returns a formatter string                                       |
| `static String format(Locale l, String format, Object... args)`                         | returns formatted string with given locale                       |
| `String substring(int beginIndex)`                                                      | returns substring for given begin index                          |
| `String substring(int beginIndex, int endIndex)`                                        | returns substring for given begin index and end index            |
| `boolean contains(CharSequence s)`                                                      | returns true or false after matching the sequence of char value  |
| `static String join(CharSequence delimiter, CharSequence... elements)`                  | returns a joined string                                          |
| `static String join(CharSequence delimiter, Iterable<? extends CharSequence> elements)` | returns a joined string                                          |
| `boolean equals(Object another)`                                                        | checks the equality of string with the given object              |
| ` boolean isEmpty()`                                                                    | checks if string is empty                                        |
| `String concat(String str)`                                                             | concatenates the specified string                                |
| `String replace(char old, char new)`                                                    | replaces all occurrences of the specified char value             |
| `String replace(CharSequence old, CharSequence new)`                                    | replaces all occurrences of the specified CharSequence           |
| `static String equalsIgnoreCase(String another)`                                        | compares another string. It doesn't check case.                  |
| `String[] split(String regex)`                                                          | returns a split string matching regex                            |
| `String[] split(String regex, int limit)`                                               | returns a split string matching regex and limit                  |
| `String intern()`                                                                       | returns an interned string                                       |
| `int indexOf(int ch)`                                                                   | returns the specified char value index                           |
| `int indexOf(int ch, int fromIndex)`                                                    | returns the specified char value index starting with given index |
| `int indexOf(String substring)`                                                         | returns the specified substring index                            |
| `int indexOf(String substring, int fromIndex)`                                          | returns the specified substring index starting with given index  |
| `String toLowerCase()`                                                                  | returns a string in lowercase                                    |
| `String toLowerCase(Locale l)`                                                          | returns a string in lowercase using specified locale             |
| `String toUpperCase()`                                                                  | returns a string in uppercase                                    |
| `String toUpperCase(Locale l)`                                                          | returns a string in uppercase using specified locale             |
| `String trim()`                                                                         | removes beginning and ending spaces of this string               |
| `static String valueOf(int value)`                                                      | converts given type into string. It is an overloaded method.     |
