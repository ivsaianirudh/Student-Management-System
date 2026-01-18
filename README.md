# Student-Management-System
students = {}

def add_student():
    roll = int(input("Enter Roll No: "))
    name = input("Enter Name: ")
    marks = float(input("Enter Marks: "))
    students[roll] = {"Name": name, "Marks": marks}
    print("Student added successfully")

def view_students():
    for roll, data in students.items():
        print("Roll:", roll, "Name:", data["Name"], "Marks:", data["Marks"])

def search_student():
    roll = int(input("Enter Roll No to search: "))
    if roll in students:
        print(students[roll])
    else:
        print("Student not found")

while True:
    print("1.Add Student 2.View Students 3.Search Student 4.Exit")
    choice = int(input("Enter Choice: "))
    if choice == 1:
        add_student()
    elif choice == 2:
        view_students()
    elif choice == 3:
        search_student()
    elif choice == 4:
        break
