
# EX 1A Reverse a String
## DATE: 18/02/25
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm

1. Start

2. If the length of s is less than or equal to 1, then: Return s

3. Otherwise: Call Reverse_String(s[1:]) (i.e., the substring from the second character to the end)

4. Concatenate the result with the first character s[0]

5. Return the concatenated result.

6. End

## Program:

Program to implement Reverse a String

Developed by: SANJAY T

Register Number: 212222110039
```PY
def reverse_string(s):
   
    if len(s) <= 1:
        return s
    
    return reverse_string(s[1:]) + s[0]


input_string = input()
print(reverse_string(input_string))
```

## Output:

![image](https://github.com/user-attachments/assets/940964c8-56f9-497b-ba6e-9762429f4f76)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
