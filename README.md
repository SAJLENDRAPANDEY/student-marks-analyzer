# student-marks-analyzer
A simple Python program to analyze student marks – shows average, highest, lowest, and pass/fail status."


# topic array 
# project 1 -- Student Marks Analyzer
def input_marks():
    n=int(input("Enter total number of students: "))
    marks=[]
    for i in range(n):
        mark=int(input("Enter your marks:"))
        marks.append(mark)
    return marks
def display_marks(marks):
    print("Student marks ")
    for i ,mark in enumerate(marks,start=1):
        print(f"Student{i}:marks {mark}")
def average_marks(marks):
    return sum(marks)/len(marks)
def max_marks(marks):
    return max(marks)
def min_marks(marks):
    return min(marks)
def pass_fail(marks):
    print("\n--- Pass/Fail Status ---")
    for i, mark in enumerate(marks, start=1):
        if mark >= 33:
            print(f"Student {i}: Pass")
        else:
            print(f"Student {i}: Fail")
marks=input_marks()
display_marks(marks)
print("\nAverage Marks:", average_marks(marks))
print("Highest Marks:", max_marks(marks))
print("Lowest Marks:", min_marks(marks))

pass_fail(marks)

