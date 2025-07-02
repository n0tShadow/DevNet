---
icon: python
---

# How to build an application with Python

Whether you're new to Python or just want to create a basic app, this tutorial will walk you through building a small, functional Python application from scratch. By the end, you’ll have a working script and a sense of how to expand it into something bigger.

## ✅ Prerequisites

* Python 3.8+
* Code editor (e.g. VS Code, PyCharm, or just Notepad++)
* Terminal / Command Prompt

Check your Python installation:

```bash
python --version
```

If not installed, download Python here: [https://www.python.org/downloads/](https://www.python.org/downloads/)

---

## 🛠 Step 1: Create a Project Directory

Let's create a folder to hold our app:

```bash
mkdir my_python_app
cd my_python_app
```

Create a Python file:

```bash
touch app.py
```

Or on Windows:

```bash
type nul > app.py
```

---

## ✍️ Step 2: Write Your First App

Open `app.py` and write the following code:

```python
def greet_user(name):
    return f"Hello, {name}! Welcome to DevNet App."

def main():
    user_name = input("Enter your name: ")
    greeting = greet_user(user_name)
    print(greeting)

if __name__ == "__main__":
    main()
```

This is a simple CLI (Command Line Interface) app that greets the user.

---

## ▶️ Step 3: Run the App

In your terminal, run:

```bash
python app.py
```

You’ll be prompted to enter your name. Try it!

```
Enter your name: Alice
Hello, Alice! Welcome to DevNet App.
```

---

## 🧩 Step 4: Add a Feature

Let’s enhance it. Modify `app.py` to let the user choose an action:

```python
def greet_user(name):
    return f"Hello, {name}! Welcome to DevNet App."

def add(a, b):
    return a + b

def main():
    name = input("Enter your name: ")
    print(greet_user(name))

    print("Choose an action:")
    print("1. Add two numbers")
    print("2. Exit")

    choice = input("Your choice: ")
    if choice == "1":
        num1 = int(input("Enter first number: "))
        num2 = int(input("Enter second number: "))
        print(f"The result is: {add(num1, num2)}")
    else:
        print("Goodbye!")

if __name__ == "__main__":
    main()
```

Now it's a **multi-functional CLI app**!

---

## 🚀 What's Next?

From here, you can:

* Add more features (e.g. multiplication, string tools, file saving)
* Turn it into a web app using Flask or FastAPI
* Package it using `pyinstaller` or `setuptools`
* Upload to GitHub or share with friends

---

## 📦 Bonus: How to Create a `requirements.txt`

If your app uses external libraries (like `requests` or `flask`), create a `requirements.txt`:

```bash
pip install requests
pip freeze > requirements.txt
```

Then others can install your app's dependencies with:

```bash
pip install -r requirements.txt
```

---

## 💡 Conclusion

This guide showed you how to build and run a basic Python CLI app, extend it, and prep it for sharing. Python is incredibly versatile — this is just the beginning.

Happy coding! 🧠💻
