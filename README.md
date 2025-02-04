from multi_number_operations import add_five_numbers, divide_three_numbers

print("Simple Calculator")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")
print("5. Add Five Numbers")

choice = int(input("Enter your choice (1-5): "))

if choice in [1, 2, 3, 4]:
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    if choice == 1:
        result = add(num1, num2)
    elif choice == 2:
        result = sub(num1, num2)
    elif choice == 3:
        result = mul(num1, num2)
    elif choice == 4:
        result = div(num1, num2)

elif choice == 5:
    nums = [float(input(f"Enter number {i + 1}: ")) for i in range(5)]
    result = add_five_numbers(*nums)
    
else:
    result = "Error: Invalid choice!"

print("Result:", result)
