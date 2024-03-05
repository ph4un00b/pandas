## code & execution

- Code Execution Correctness

  - The code should **execute** without errors❗
  - Question: Is there anything wrong with this code that
    will prevent it from executing?
    Choices:
    No - The code will execute.
    ❌ - The code does not have a class or main method
    ❌ - Collectors.joining() is not implemented correctly

- Code **Output** Correctness

  - The code needs to produce the correct **output**
  - Question: We already know that Response A’s code does not work,
    but syntax errors aside, are they logically correct❓
    Choices:
    Yes
    No

- 👉 Factual Correctness

  - The non-code text/explanations/claims
    are all factual and truthful❓
  - Keep in mind that the code may be functional for the prompter,
    even if it does not compile or run on your setup.
    - a response that points to a file only accessible to the prompter,
    - provides a partial program based on the context provided by the prompter
    - ❌ unless it contains errors that would (likely) manifest in the prompter’s programming context.

- Is the response well written❓
  Briefly explain the issues you found.

  - Minor Issues:

    - A code has minor problems that are straightforward to fix (e.g., missing imports, small syntax errors), or is correct but has misleading comments.

  - 🔥 Major Issues:
    - the code is very hard to follow or is missing critical documentation.

- 👉 Verbosity

  - Question: Which response sections would you say contains additional information
    that is not necessary to answer the prompt❓
    Choices - Select all that apply:
    Response A - contains redundant code examples
    Response A - contains redundant information pertaining to code explanation
    Response B - contains redundant information pertaining to code explanation
    Response B - contains redundant code examples

- 👉 Clean Code

  - Formatting - Perfect formatting that is neat and utilizes white-space effectively.
  - Naming - Variables and function names that make the understanding of code easier.
  - Code Design - Code is nicely de-composed and divided in functions
    that are intelligible and that make sense.
  - Question: Which response’s code is more readable❓
    Choices:

    Response A code
    Response B code

- truthful & correct❓
  - 👉 code execution & code output & factual correctness
  - major issues:
    - a severely false claim about the stream().reduce() method.

# bad answers

## Instruction Following

- Prompt:

input_string=input("enter a string:")
no_spaces_string=input_string.replace(" "," ")
string_length=len(no_spaces_string)
print("length of the string(after removing spaces):",string_length)

```
  if code_prompt contains Error
    return CODE MODIFICATION
  else
    return CODE UNDERSTANDING

  return BAD CONTEXT
```

## Factual Correctness:

- Prompt:

What is a set enumeration tree.

Imagine you have a set \( S = \{a, b, c\} \). The set enumeration tree for \( S \) represents all possible subsets of \( S \), including the empty set and the set itself.

Here's a simple representation of the set enumeration tree for \( S \):

```

                 {}

               / | \

              /  |  \

             a   b   c

            / \  |  / \

           b   c c   b a

          /     |     \

         c      a      a

```

## Code Output Correctness

- Prompt:

Single File Programming Question

Problem Statement

You have been assigned the task of designing a program that converts a given sentence into reverse order, extracts the vowels and consonants from the sentence, and prints them separately.

Input 1 :
Hello, world!

Output 1 :
world! Hello,
eoo
Hllwrld
in c++

```output
Reversed sentence: ,olleH dlrow
Vowels: eoo
Consonants: Hllwrld
```

## Verbosity

- Prompt:
  Write a c program to display all the letters of the alphabet (a-z). Use two for loops: the 1st one will print all
  letters in small letters and the 2nd one will print them in capital letters.
  Example output:
  a b c d e…z
  A B C D E…Z

```
[actual useful code]
...
**Explanation:**❌
...
**How it works:**❌
...
**To compile and run this program:**❌
...
```

## Formatting

- Prompt:
  i'm having trouble adding a key vault key required for customer encryption in azure, can you suggest a fix?

```does not make sense to come up with pre-requisites first
**Here are some common issues and fixes when adding a Key Vault key for customer encryption in Azure:**
**Prerequisites:**
...
**Common Issues and Fixes:**
...
...
```

## both correct

- Response A: correct
  Response B: correct
  Action: see Step 3
- Response A: incorrect
  Response B: incorrect
  Action: see Step 3
- Step 3: Choose the more concise response between the two.
  This means you must choose the one that is shorter,
  when they are both incorrect or they are both correct.
  Please keep this workflow in mind as you complete Code Eval Tasks! This will help you succeed!
