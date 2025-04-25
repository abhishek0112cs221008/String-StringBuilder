
# Java Strings

## String Declaration and Initialization
Java strings are declared using `String` followed by the variable name and assigned a value using the assignment operator `=`.  
**Example:**  
```java
String str = "CollegeWala";
```
Note the capitalization of `String`.

## Taking String Input
Strings can be taken as input using `Scanner`.  
- `sc.nextLine()` reads the entire line of input, including spaces.  
- `sc.next()` stops at the first space.  

## String Length
The length of a string is obtained using `str.length()`.  
Note the parentheses; this is a method, not an attribute.

## Accessing String Characters
Characters are accessed using the `charAt()` method.  
Indexing starts from 0.  
**Example:**  
```java
str.charAt(3); // accesses the fourth character
```

## String Functions
- `length()` – Returns the length of the string.
- `charAt()` – Returns the character at a specific index.
- `indexOf()` – Returns the index of the first occurrence of a specified character or substring.
- `compareTo()` – Compares two strings lexicographically.  
  Returns:
  - 0 if equal
  - positive value if first string is greater
  - negative value if first string is smaller
- `startsWith()` and `endsWith()` – Check if a string starts or ends with a specific substring.
- `toLowerCase()` and `toUpperCase()` – Convert a string to lowercase or uppercase.
- `substring()` – Extracts a portion of a string.

## String Immutability
Java strings are immutable.  
Once a string is created, its value cannot be changed.  
Operations that appear to modify a string actually create a new string.

## String Concatenation
Strings can be concatenated using the `+` operator.  
However, repeated concatenation is inefficient due to immutability.  
Each concatenation creates a new string.

## String Interning
Java uses string interning to optimize memory usage.  
If two strings have the same value, they may point to the same memory location.  
Using `new` creates a new string in memory.

## String Performance
String manipulation can be inefficient due to immutability.  
Use `StringBuilder` for better performance.

---

# Java StringBuilder

## Declaration and Initialization
```java
StringBuilder sb = new StringBuilder();
StringBuilder sb2 = new StringBuilder("initial string");
```

## StringBuilder Methods
- `append()` – Adds characters or strings to the end.
- `insert()` – Inserts characters or strings at a specific position.
- `delete()` – Removes characters.
- `reverse()` – Reverses characters.
- `setCharAt()` – Replaces character at a specific index.

## StringBuilder vs. String
- `StringBuilder` is **mutable**, making it efficient for repeated modifications.
- Avoids creation of intermediate strings.

---

# Palindromes and String Compression

## Palindrome Check
A palindrome is a sequence that reads the same backward as forward.  
Basic algorithm:
```java
String reversed = new StringBuilder(str).reverse().toString();
if (str.equals(reversed)) {
    // It's a palindrome
}
```

## String Compression
Reduce the size of a string by counting consecutive repeating characters.  
**Example:**  
```text
"AAABBBCC" becomes "A3B3C2"
```

---
