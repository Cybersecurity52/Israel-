#include <iostream>
#include <fstream>
#include <string>

using namespace std;

struct Student {
  string name;
  string department;
  string college;
  int level;
  string hostel;
};

void allocateHostel(Student &student) {
  if (student.department == "Cyber security" && student.level == 100) {
    student.hostel = "mark hostel";
  } else if (student.department == "cyber security" && student.level == 200) {
    student.hostel = "mark hostel";
  } else if (student.department == "Cyber security" && student.level == 300) {
    student.hostel = "special hostel";
  } else if (student.department == "cyber security" && student.level == 400) {
    student.hostel = "john hostel";
  } else if (student.department == "Electrical Engineering" && student.level == 100) {
    student.hostel = "luke hostel";
  } else if (student.department == "Electrical Engineering" && student.level == 200) {
    student.hostel = "luke hostel";
  } else if (student.department == "Electrical Engineering" && student.level == 300) {
    student.hostel = "luke hostel";
  } else if (student.department == "Electrical Engineering" && student.level == 400) {
    student.hostel = "mathew hostel";
  } else if (student.department == "Electrical Engineering" && student.level == 500) {
    student.hostel = "john hostel";
  } else {
    student.hostel = "nh";
  }
}

int main() {
  // Open the input file
  ifstream inputFile("students.txt");

  // Read the students from the input file and allocate them to hostels
  string name; 
  string department; 
  string college;
  int level;
  while (inputFile >> name >> department >> college >> level) {
    Student student = {name, department, college, level};
    allocateHostel(student);
    cout << student.name << " has been assigned to " << student.hostel << endl;
  }

  // Close the input file
  inputFile.close();

  return 0;
}

# Israel-
Assignment 
