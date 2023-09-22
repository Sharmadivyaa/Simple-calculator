# Simple-calculator
Design a simple calculator with basic arithmetic operations. Prompt the user to input two numbers and an operation choice.  Perform the calculation and display the result.
# Function to add two numbers
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y
    
def divide(x, y):
    if y == 0:
        return "Cannot divide by zero"
    return x / y

while True:
    print("Options:")
    print("Enter 'add' for addition")
    print("Enter 'subtract' for subtraction")
    print("Enter 'multiply' for multiplication")
    print("Enter 'divide' for division")
    print("Enter 'quit' to end the program")

    choice = input("Enter your choice: ")

    if choice == "quit":
        break

    if choice in ("add", "subtract", "multiply", "divide"):
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if choice == "add":
            print(f"Result: {add(num1, num2)}")
        elif choice == "subtract":
            print(f"Result: {subtract(num1, num2)}")
        elif choice == "multiply":
            print(f"Result: {multiply(num1, num2)}")
        elif choice == "divide":
            print(f"Result: {divide(num1, num2)}")
    else:
        print("Invalid input. Please enter a valid operation.")
