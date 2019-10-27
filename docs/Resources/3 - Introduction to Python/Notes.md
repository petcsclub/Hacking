title: Meeting 3 & 4 Notes

## Meeting 3: Introduction to Python

## Resources
1. [Repl.it](https://repl.it/)
2. [Python Documentation](https://docs.python.org/2.7/tutorial/index.html)
3. [Python Library Reference (for standard modules)](https://docs.python.org/2/library/)
4. [Example Hangman Game made in Python](https://hangman.redapple410.repl.run)


## Notes

Follow along with the steps below to create your own Hangman/word guessing game in Python! Each step builds on the code from the previous step.  
Note that we will be using Python 2 for this lesson.  
  
Example: [https://hangman.redapple410.repl.run](https://hangman.redapple410.repl.run)  
Example code: [https://repl.it/@redapple410/hangman](https://repl.it/@redapple410/hangman)  


---
### 0: Getting Started

**Explanation:**

Go to [repl.it](https://repl.it/) and create a new repl (project). Choose Python 2 as the language.


---
### 1: Output

**Explanation:**

Imagine that you are playing hangman, and need to pick a word. Output this word using `print "The correct word is ..."`.  

**Example:**

- [https://repl.it/@redapple410/hangman-01](https://repl.it/@redapple410/hangman-01)


---
### 2: Variables

**Explanation:**

Take your word from Step 1, and create a variable (perhaps call it `word`?) to store it using `<name> = <value>`. Then, output its value using `print "The correct word is %s." % (<name>)`.  

**Example:**

- [https://repl.it/@redapple410/hangman-02](https://repl.it/@redapple410/hangman-02)


---
### 3: Input

**Explanation:**

Create a new variable (perhaps call it `guess`?) and use `<name> = raw_input("Guess the word: ")` to get input from the user. It's also a good idea to output the user's guess.   

**Example:**

- [https://repl.it/@redapple410/hangman-03](https://repl.it/@redapple410/hangman-03)


---
### 4: If/Else Statements

**Explanation:**

After getting input, check to see if the user's guess matches the correct word using `if guess == word:`. If it matches, output something nice! Otherwise, use `else:` to tell them that the guess is incorrect.  

**Example:**

- [https://repl.it/@redapple410/hangman-04](https://repl.it/@redapple410/hangman-04)


---
### 5: While Loops

**Explanation:**

Use a `while` loop to let the user keep guessing the word until they get it right (ie. keep guessing `while guess != word`). You can even implement another variable to keep count of how many guesses it takes!

**Example:**

- [https://repl.it/@redapple410/hangman-05](https://repl.it/@redapple410/hangman-05)


---
### 6: For Loops

**Explanation:**

Now, instead of asking the user to guess the entire word, ask them to guess just one letter instead. Every time they guess a letter, use a `for` loop to go through every letter of the correct word and compare it to the user's guess. If they match, output something (eg. `print "Found letter %s at index %d" % (guess, i)`).  

**Example:**

- [https://repl.it/@redapple410/hangman-06](https://repl.it/@redapple410/hangman-06)


---
### 7: String Operations

**Explanation:**

Use string concatenation and string slicing like `word[:i] + guess + word[i+1:]` to keep track of which letters the user has correctly guess so far, and output them to the screen. 

**Example:**

- [https://repl.it/@redapple410/hangman-07](https://repl.it/@redapple410/hangman-07)


---
### 8: Lists

**Explanation:**

Create a pre-defined list of words (perhaps call it `words`?) that you can choose from.  

**Example:**

- [https://repl.it/@redapple410/hangman-08](https://repl.it/@redapple410/hangman-08)


---
### 9: Importing Modules

**Explanation:**

Import the `random` module using `import random`. Then, use `word = random.choice(words)` to randomly choose a word from the list you created in Step 8, and use it as the correct word for Hangman.  
(For those who are too lazy to consult the Library Reference, `random.choice(<list>)` returns a random item from the given list.)  

**Example:**

- [https://repl.it/@redapple410/hangman-08](https://repl.it/@redapple410/hangman-08)
