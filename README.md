employees = {}

while True:
    print("\n--- Employee Payroll System ---")
    print("1. Add Employee")
    print("2. View Employees")
    print("3. Calculate Salary")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        emp_id = input("Enter Employee ID: ")
        name = input("Enter Name: ")
        hours = float(input("Enter Hours Worked: "))
        rate = float(input("Enter Pay per Hour: "))

        employees[emp_id] = {
            "name": name,
            "hours": hours,
            "rate": rate
        }

        print("Employee added successfully!")

    elif choice == "2":
        print("\nEmployee Details:")
        for emp_id, data in employees.items():
            print("ID:", emp_id,
                  "Name:", data["name"],
                  "Hours:", data["hours"],
                  "Rate:", data["rate"])

    elif choice == "3":
        emp_id = input("Enter Employee ID: ")

        if emp_id in employees:
            hours = employees[emp_id]["hours"]
            rate = employees[emp_id]["rate"]
            salary = hours * rate

            print("Employee Name:", employees[emp_id]["name"])
            print("Total Salary:", salary)
        else:
            print("Employee not found!")

    elif choice == "4":
        print("Exiting program...")
        break

    else:
        print("Invalid choice!")
