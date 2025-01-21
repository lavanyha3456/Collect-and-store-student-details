# Collect-and-store-student-details
CODING:

import java.util.ArrayList;

import java.util.Scanner;

class Student {

private String name;

private int age;

private String grade;

// Constructor

public Student(String name, int age, String grade) {

this.name = name;

this.age = age;
this.grade = grade;

}

// Method to display student details

public void displayDetails() {

System.out.println("Name: " + name + ", Age: " + age + ", Grade: " + grade);

}

}

public class StudentDetails {

public static void main(String[] args) {

Scanner scanner = new Scanner(System.in);

ArrayList<Student> students = new ArrayList<>();

System.out.print("Enter the number of students: ");

int numStudents = scanner.nextInt();

scanner.nextLine(); // Consume the newline character

// Collect student details

for (int i = 0; i < numStudents; i++) {

System.out.println("\nEnter details for student " + (i + 1) + ":");

System.out.print("Enter name: ");

String name = scanner.nextLine();

System.out.print("Enter age: ");

int age = scanner.nextInt();

scanner.nextLine(); // Consume the newline character

System.out.print("Enter grade: ");

String grade = scanner.nextLine();

// Create a Student object and add it to the list

students.add(new Student(name, age, grade));
}
// Display all student details

System.out.println("\nStudent Details");

for (Student student : students) {

student.displayDetails();

}

scanner.close();

}

}

OUTPUT:

Enter the number of students: 2

Enter details for student 1:

Enter name: Divya

Enter age: 20

Enter grade: A

Enter details for student 2:

Enter name: Priya

Enter age: 19

Enter grade: B

Student Details

Name:Divya, Age: 20, Grade: A

Name:Priya, Age: 19, Grade: B
