#include <iostream>
#include <string>
#include <vector>
using namespace std;

struct Student {
    string name;
    int rollNo;
    vector<int> marks;
    char grade;
};

void calculateGrade(Student& student) {
    int totalMarks = 0;
    for (int mark : student.marks) {
        totalMarks += mark;
    }
    int averageMarks = totalMarks / student.marks.size();

    if (averageMarks >= 90) {
        student.grade = 'A';
    } else if (averageMarks >= 80) {
        student.grade = 'B';
    } else if (averageMarks >= 70) {
        student.grade = 'C';
    } else if (averageMarks >= 60) {
        student.grade = 'D';
    } else {
        student.grade = 'F';
    }
}

int main() {
    int numStudents;

    cout << "Enter the number of students: ";
    cin >> numStudents;

    vector<Student> students(numStudents);

    for (int i = 0; i < numStudents; ++i) {
        cout << "\nStudent " << i + 1 << ":\n";
        cout << "Enter name: ";
        cin >> students[i].name;
        cout << "Enter roll number: ";
        cin >> students[i].rollNo;

        students[i].marks.resize(3);
        cout << "Enter marks in three subjects:\n";
        for (int j = 0; j < 3; ++j) {
            cout << "Subject " << j + 1 << ": ";
            cin >> students[i].marks[j];
        }

        calculateGrade(students[i]);
    }

    cout << "\nReport Card:\n";
    for (const Student& student : students) {
        cout << "\nName: " << student.name << endl;
        cout << "Roll No: " << student.rollNo << endl;
        cout << "Marks: ";
        for (int mark : student.marks) {
            cout << mark << " ";
        }
        cout << std::endl;
        cout << "Grade: " << student.grade << endl;
    }

    return 0;
}
