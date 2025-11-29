# Assignment5py
#NAME-ANSHIKA
#course- BCA(AI&DS)
#SECTION-A
#SERIAL NUMBER- 44
#ROLL NO- 2501060113

class Person:
    def _init_(self, name, age):
        self.name = name
        self.age = age
    
    def display_person(self):
        print("Name:", self.name)
        print("Age:", self.age)

class Student(Person):
    def _init_(self, name, age, course):
        super()._init_(name, age)
        self.course = course
    
    def display_student(self):
        self.display_person()
        print("Course:", self.course)

class Exam(Student):
    def _init_(self, name, age, course, m1, m2, m3):
        super()._init_(name, age, course)
        self.m1 = m1
        self.m2 = m2
        self.m3 = m3
        self.total = m1 + m2 + m3
    
    def display_exam(self):
        self.display_student()
        print("Marks in Subject 1:", self.m1)
        print("Marks in Subject 2:", self.m2)
        print("Marks in Subject 3:", self.m3)
        print("Total Marks:", self.total)

student1 = Exam("Anshika", 18, "BCA AI & DS", 85, 90, 88)
student1.display_exam()
