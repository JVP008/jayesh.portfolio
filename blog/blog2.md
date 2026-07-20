**most fundamental way to check even/odd:**

===

### what could be the fundamental way to check whether the number is even or odd other than doing modulo (%) operation i.e to observe remainder ? there is one or so indeed!!, and one of them is so close to our computer we often call it as a 'Language of computers' : Bits (0/1) - the only thing computer TRULY understands. 


But how !! how can we check whether the number is odd or even with just those two Numbers or Combination of those Two Numbers ??
We will see it gradually...

Let's start from scratch :
even 5yr old knows what a binary system is (the world has changed) : The binary system is a number or counting system where, Instead of using ten digits (0–9) like we humans normally do, it uses just two: 0 and 1.
Definition of Odd and Even :
Definition of odd and even :

A number is said to be even if it is completely divisible by 2 or the remainder is 0.
On contrary to even no. definition - A number is said to be odd if it is NOT completely divisible by 2 or the remainder of the operation is 1.

in school/colleges we were taught that just like decimal number we can perform arithmetic operations on binary numbers as well:
we can do addition, subtraction, division, multiplication and so on.... and we also learned that, just as we use the '+' operator to add decimal numbers, the binary system uses logic gates or bitwise operation , here XOR' is used to perform addition, 'AND' is used for multiplication, 'NOT' is used for inversion, and so on.

the truth table for few of them is :

---

|Decimal Value|A|B|C|AND|OR|XOR|
|-|-|-|-|-|-|-|
|0|0|0|0|0|0|0|
|1|0|0|1|0|1|1|
|2|0|1|0|0|1|1|
|3|0|1|1|1|1|0|
|4|||||||
|5|||||||
|6|||||||







Now that we've covered the concepts that we will need, let's return to our original question and solve it.
Note: no errors are handled in given programs :)
1] The Decimal Approach: 

Steps :
1. take a number as input from user .
2. try to divide it by 2 
3. if its completely divisible by 2 (as said earlier) we return "Even" if its not we return "Odd" ,as simple as that .

---

Here is the python program :
add the image here : Decimal\_way.png
---


what we used here :
1. A decimal number (n)
---

### 2\. Modulo Operator (%)

3\. Our main character/number (2)
4. Comparison Operator (==).

**Things to take care of:**
 None. just make sure that you dont enter 0 as input.. unless you enjoy crashing programs .
---


2.1] Binary Approach:

Before talking about logic itself , lets understand why and how does it works:
Its all about Observation. see the image below did you notice something? 
Every EVEN number has 0 in the 2⁰ position and ODD has 1 in the 2⁰ position 

---

### | Decimal | Binary | 2⁰ Bit (LSB) | Even/Odd |

### | ------: | :----: | :----------: | :------: |

### |       0 |  0000  |     \*\*0\*\*    |   Even   |

### |       1 |  0001  |     \*\*1\*\*    |    Odd   |

### |       2 |  0010  |     \*\*0\*\*    |   Even   |

### |       3 |  0011  |     \*\*1\*\*    |    Odd   |

### |       4 |  0100  |     \*\*0\*\*    |   Even   |

### |       5 |  0101  |     \*\*1\*\*    |    Odd   |

### |       6 |  0110  |     \*\*0\*\*    |   Even   |

### |       7 |  0111  |     \*\*1\*\*    |    Odd   |

### |       8 |  1000  |     \*\*0\*\*    |   Even   |

|       9 |  1001  |     \*\*1\*\*    |    Odd   |

---

### I hope : By now, you have probably noticed the pattern.

so let try to program it!!
Steps:
1. take a number as input from user .
2. convert that number into binary using '**bin()'** function in python and store it in variable or don't .
	it will return string for e.g : 4 will be equals "100"
3. compare the last string character with "0" 
4. if the last character is "0" , function will return "Even" else "Odd".

Here is the program: 
add the image 2.1 here

what we used here :
---

1. ### A decimal number (n)
2. ### bin() function in python
3. ### Negative Indexing 
4. ### Our main character/number (2)
5. ### Comparison Operator (==).



**Things to take care of :**
Notice that we are not comparing last character/element with the 0 (integer) ; we are comparing it with "0" (string) if you missed that ... well, more power to you.

2.2] Bitwise AND approach :
---

### Earlier, we talked about logic gates and operators, but Program 2.1 didn't use any of them. That was just one approach. Now let's do it using bitwise AND (\&).

### 

### Steps:

1. ### First take a number as input from the user.
2. ### perform a bitwise AND operation between the number and 1 (n \& 1).
3. ### If the result is 0, the last bit is 0, which means the number is Even.
4. Otherwise, the last bit is 1, which means the number is Odd asss simple as that.

   ---

Here is the program:
add the image 2.2 here
---





Things you will notice here:

---

* ### We didn't convert the input to binary this time. Why? Because if we did convert it explicitly using the bin() function, it would return something like "0b10101...".
* ### If we then tried to convert it into an integer directly, the program will throw an error because the string contains "0b". It simply indicates that the number is in binary form.

### Someone: "What if we perform a bitwise operation on a string, i.e., "0b0101" \& 0001?"

* ### We can't, because, as the name suggests, it's a bitwise operator, and it does not work on strings.
* But if you know how to strip a string so that the left part ("0b") and the right part ("0101") get separated, then you can go that way as well by converting "0101" back into an integer first.

  ---

### What we used here :

### A decimal number (n)

### Bitwise AND operator (\&)

### Our main character/number (1)

Comparison operator (==)

That's it ,here is the summary:
- Even numbers have 0 at their last bit, whereas odd numbers have 1.
---

### \- we have learnt about three methods for finding out whether the number is even or odd: modulo (%), binary conversion using bin() function and bitwise AND (\&).

\- Out of the three techniques, the bitwise technique (n \& 1) is the most straightforward and atomic because it directly checks the last bit .
Plz share your thoughts here : DM me on linkdin or email me: jayeshus2008@gmail.com
---

