# Personal Expense Tracker in Python

expenses = []

while True:
    print("\n===== PERSONAL EXPENSE TRACKER =====")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Total Expense")
    print("4. Exit")

    choice = input("Enter your choice: ")

    # Add Expense
    if choice == '1':
        item = input("Enter expense name: ")
        amount = float(input("Enter amount: "))

        expenses.append([item, amount])
        print("Expense Added Successfully!")

    # View Expenses
    elif choice == '2':
        print("\n--- Expense List ---")

        if len(expenses) == 0:
            print("No expenses recorded.")
        else:
            for i in expenses:
                print("Item:", i[0], "| Amount:", i[1])

    # Total Expense
    elif choice == '3':
        total = 0

        for i in expenses:
            total += i[1]

        print("Total Expense =", total)

    # Exit
    elif choice == '4':
        print("Thank You for Using Expense Tracker")
        break

    else:
        print("Invalid Choice! Please Try Again.")