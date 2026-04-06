# Student-Management-System-in-Java-ArrayList-Implementation-

This is a simple Java program that stores and manages student details using an ArrayList. It includes student ID, name, and marks, displays all records, and finds the top-scoring student.  This project helps beginners understand classes, objects, ArrayList, and basic data handling in Java.


import java.util.*;
class Student {
    int id;
    String name;
    double marks;
    Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }
    void display() {
        System.out.println(id + " " + name + " " + marks);
    }
}
public class StudentManagement {
    public static void main(String[] args) {
        ArrayList<Student> list = new ArrayList<>();
        list.add(new Student(1, "Ravi", 85.5));
        list.add(new Student(2, "Teja", 90.0));
        list.add(new Student(3, "Kumar", 78.0));
        System.out.println("Student Details:");
        for (Student s : list) {
            s.display();
        }
        Student top = list.get(0);
        for (Student s : list) {
            if (s.marks > top.marks) {
                top = s;
            }
        }

        System.out.println("\nTopper:");
        top.display();
    }
}
