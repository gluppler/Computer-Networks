
---

### **Q1-C21**

**Question:** To improve code modularization and utilization, which of the following is used to describe a collection of objects with the same attributes and methods?
**A.** class
**B.** init
**C.** function
**D.** def
**Correct Answer: A**

**Explanation:**

In Object-Oriented Programming (OOP), a **class** is a blueprint or template. It defines the "attributes" (data) and "methods" (behaviors) that a group of objects will share.

* For example, if you have a class called `Router`, all router objects created from it will have attributes like `IP_address` and methods like `get_config()`.
* **`def`** is the keyword used to define a function or method.
* **`__init__`** is a special method inside a class used to initialize new objects.

---

### **Q2-C21**

**Question:** Which of the following methods is used to write data to the telnetlib module?
**A.** read_all()
**B.** close()
**C.** write()
**D.** read_very_eager()
**Correct Answer: C**

**Explanation:**

The `telnetlib` module (historically used in Python for basic network automation) provides a `Telnet` class to interact with remote devices.

* **`write(buffer)`**: This method sends a string (specifically a byte string) to the remote server. For example, `tn.write(b"ls\n")` sends the "ls" command.
* **`read_all()`** and **`read_very_eager()`** are used to *receive* data from the device.
* **`close()`** terminates the session.

---

### **Q3-C21**

**Question:** Which of the following characters can be used as Python identifiers? (Multiple Choice)
**A.** Digits
**B.** @ signs
**C.** Letters
**D.** Underscores
**Correct Answer: ACD**

**Explanation:**

An **identifier** is a name given to variables, functions, or classes. The rules for Python identifiers are:

1. Can contain **Letters** (A-Z, a-z), **Digits** (0-9), and **Underscores** (`_`).
2. **Cannot start with a digit** (e.g., `1variable` is invalid, but `variable1` is okay).
3. **No special characters** (like `@`, `$`, or `%`) are allowed.
4. They are case-sensitive.

---

### **Q4-C21**

**Question:** Which of the following are compiled high-level programming languages? (Multiple Choice)
**A.** C
**B.** C++
**C.** Java
**D.** Python
**Correct Answer: AB**

**Explanation:**

Languages are generally classified by how they are translated into machine code:

* **Compiled (A & B):** The entire source code is translated by a "compiler" into an executable file before it runs. This makes them very fast. **C** and **C++** are classic examples.
* **Interpreted (D):** The code is read and executed line-by-line by an "interpreter." **Python** and JavaScript fall here.
* **Hybrid (C):** **Java** is a bit unique; it is compiled into "Bytecode" and then interpreted (or JIT-compiled) by the Java Virtual Machine (JVM). In the context of "purely compiled" vs "interpreted" in many networking exams, C/C++ are the primary answers for compiled.

---

### **Q5-C21**

**Question:** Python programs use indentation to represent code blocks. Statements in the same code block must have the same number of indented spaces.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Unlike languages like C++ or Java that use curly braces `{ }` to group code, Python uses **indentation**.

* Consistent spacing is a **syntactical requirement**.
* If you have an `if` statement, all the code that should run when the condition is true must be indented to the same level (usually 4 spaces). Mixing 3 spaces and 4 spaces in the same block will cause an `IndentationError`.

---

