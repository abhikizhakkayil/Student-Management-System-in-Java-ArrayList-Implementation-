# Student-Management-System-in-Java-ArrayList-Implementation-

This is a simple Java program that stores and manages student details using an ArrayList. It includes student ID, name, and marks, displays all records, and finds the top-scoring student.  This project helps beginners understand classes, objects, ArrayList, and basic data handling in Java.



import java.util.ArrayList;

// Student class
class Student {
    int id;
    String name;
    double marks;

    // Constructor
    Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    // Method to display student details
    void display() {
        System.out.println("ID    : " + id);
        System.out.println("Name  : " + name);
        System.out.println("Marks : " + marks);
        System.out.println("----------------------");
    }
}

// Main class
public class StudentManagement {
    public static void main(String[] args) {

        // Create ArrayList
        ArrayList<Student> list = new ArrayList<>();

        // Add students
        list.add(new Student(1, "Ravi", 85.5));
        list.add(new Student(2, "Teja", 90.0));
        list.add(new Student(3, "Kumar", 78.0));

        // Display all students
        System.out.println("📚 Student Details:\n");
        for (Student s : list) {
            s.display();
        }

        // Find topper
        Student top = list.get(0);
        for (Student s : list) {
            if (s.marks > top.marks) {
                top = s;
            }
        }

        // Display topper
        System.out.println("🏆 Topper Details:\n");
        top.display();
    }
}
