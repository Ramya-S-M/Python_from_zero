**Python Learning Journey — Week 1: Building Blocks**



Documenting a weekly Python learning series. This week covers the fundamentals: tokens, keywords, and indentation — with real-world analogies and traced examples.



>Python source code never runs directly on a CPU — it's first compiled into bytecode, then executed instruction-by-instruction by the Python Virtual Machine (PVM). Everything in this post happens \*before\* that translation step even begins.



**Core Concepts:**



**Tokens**

The smallest units Python parses from a line, before applying any rules to it.



```python

x = 5

```

Tokens: `x`, `=`, `5` — the same way a sentence splits into words before grammar checks apply.



**Keywords**

Reserved identifiers Python won't let you repurpose as variable names.



```python

for = 5   # SyntaxError — `for` is reserved

```

***Analogy***<i>: a trademarked name you can't reuse as your own — the word already has a fixed job in the language.</i>



**Indentation**

Unlike most languages where whitespace is cosmetic, in Python \*\*indentation is the syntax\*\*. It defines block scope directly — no `{ }` braces involved.



**Real-world analogy:**

Indentation works like a building's floor plan. Walls (indentation) define which rooms (code blocks) a hallway connects to. Move a wall a few inches, and a room that was "inside" the house is suddenly outside it — same idea, different meaning.



**Traced Example**



```python

age = 16

if age >= 18:

&#x20;   print("You can vote")

print("hello world")

```



\*\*Output:\*\*

```

hello world

```



Indent that last line by mistake, and it becomes part of the `if` block — meaning it would never print, since the condition was False. The layout of the code directly determines what executes.



**Practice Code**



```python

line = "if x == 5: print('hello')"

keywords = \["if", "else", "for", "while", "def", "return", "print"]



**for word in keywords:**

&#x20;   if word in line:

&#x20;       print(f"Found keyword: {word}")

```



Output:

```

Found keyword: if

Found keyword: print

```



***Note*** <i>on `in` — a Pythonic pattern worth internalizing</i>





One operator, one mental model, reused across types — this consistency is a core part of what makes code "Pythonic."



**What Confused Me**



The hardest adjustment was treating whitespace as logic rather than style. Misaligned indentation kept throwing `IndentationError` until it clicked that Python uses indentation the way other languages use `{ }` — the error is pointing to exactly where the structural "wall" doesn't line up, not punishing arbitrary formatting choices.

