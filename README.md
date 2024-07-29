def add(x, y):
  """Adds two numbers together and returns the sum."""
  return x + y

def subtract(x, y):
  """Subtracts one number from another and returns the difference."""
  return x - y

def multiply(x, y):
  """Multiplies two numbers together and returns the product."""
  return x * y

def divide(x, y):
  """Divides one number by another and returns the quotient.
  Raises a ZeroDivisionError if y is zero."""
  if y == 0:
    raise ZeroDivisionError("Cannot divide by zero")
  return x / y

# Get user input for operation and numbers
while True:
  print("\nBasic Calculator")
  print("1. Add")
  print("2. Subtract")
  print("3. Multiply")
  print("4. Divide")
  print("5. Exit")
  choice = input("Enter your choice (1-5): ")

  if choice in ('1', '2', '3', '4'):
    try:
      num1 = float(input("Enter the first number: "))
      num2 = float(input("Enter the second number: "))
    except ValueError:
      print("Invalid input. Please enter numbers only.")
      continue

    if choice == '1':
      print(f"{num1} + {num2} = {add(num1, num2)}")
    elif choice == '2':
      print(f"{num1} - {num2} = {subtract(num1, num2)}")
    elif choice == '3':
      print(f"{num1} * {num2} = {multiply(num1, num2)}")
    else:
      try:
        print(f"{num1} / {num2} = {divide(num1, num2)}")
      except ZeroDivisionError as e:
        print(e)
  elif choice == '5':
    print("Exiting the calculator.")
    break
  else:
    print("Invalid choice.")

<!---
Shandya2004/Shandya2004 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
