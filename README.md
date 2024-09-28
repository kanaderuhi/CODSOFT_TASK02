# CODSOFT_TASK02
def add(x, y):
        return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        raise ValueError("Cannot divide by zero!")
    return x / y

def calculator():
    print("Simple Calculator")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")

    while True:
        choice = input("Enter your choice (1/2/3/4) or 'q' to quit: ")

        if choice.lower() == 'q':
            break
        elif choice in ['1', '2', '3', '4']:
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))

                if choice == '1':
                    print(f"{num1} + {num2} = {add(num1, num2)}")
                elif choice == '2':
                    print(f"{num1} - {num2} = {subtract(num1, num2)}")
                elif choice == '3':
                    print(f"{num1} * {num2} = {multiply(num1, num2)}")
                elif choice == '4':
                    try:
                        print(f"{num1} / {num2} = {divide(num1, num2)}")
                    except ValueError as e:
                        print(e)
            except ValueError:
                print("Invalid input. Please enter a number.")
        else:
            print("Invalid choice. Please choose a valid option.")

if __name__ == "__main__":
    calculator()
