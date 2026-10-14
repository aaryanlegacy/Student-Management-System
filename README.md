# Student Management System

A simple **console-based Student Management System** written in **C++**. The project uses **binary file handling** to store student records permanently in a local file, allowing users to add, view, search, update, and delete student information.

## Features

- **Add Student** – Add a student with ID, name, and marks.
- **Display Students** – View all stored student records.
- **Search Student** – Find a student using their ID.
- **Update Student** – Modify the name and marks of an existing student.
- **Delete Student** – Remove a student record by ID.
- **Persistent Storage** – Records are stored in a binary file named `students.dat`.
- **Menu-Driven Interface** – Easy-to-use command-line menu.

## Technologies Used

- **Language:** C++
- **Libraries:**
  - `iostream` – Console input and output
  - `fstream` – File handling
- **Storage:** Binary file handling (`students.dat`)

## Project Structure

```text
StudentManagementSystem/
│
├── StudentManagementSystem.cpp   # Main C++ source code
├── README.md                     # Project documentation
├── students.dat                  # Student data file (created automatically)
└── temp.dat                      # Temporary file used during deletion
```

> `students.dat` and `temp.dat` are created/used by the program at runtime. They do not need to exist before the first run.

## How to Run

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd StudentManagementSystem
```

### 2. Compile the Program

Using `g++`:

```bash
g++ StudentManagementSystem.cpp -o StudentManagementSystem
```

### 3. Run the Program

**Windows:**

```bash
StudentManagementSystem.exe
```

**Linux/macOS:**

```bash
./StudentManagementSystem
```

## Menu Options

When the program starts, the following menu is displayed:

```text
--- Student Management System ---
1. Add Student
2. Display Students
3. Search Student
4. Update Student
5. Delete Student
6. Exit
```

Choose the required option by entering the corresponding number.

## Data Structure

Each student is represented using the following structure:

```cpp
struct Student {
    int id;
    char name[50];
    float marks;
};
```

The student record contains:

- `id` – Unique identifier for the student
- `name` – Student name
- `marks` – Student marks

## File Handling

The application stores records in `students.dat` using binary file operations:

- `ofstream` is used to add records.
- `ifstream` is used to display and search records.
- `fstream` is used to update records directly in the file.
- A temporary file, `temp.dat`, is used when deleting a record.

## Important Notes

- The current input method uses `cin >> s.name`, so student names containing spaces are not supported.
- Student records are stored locally in binary format and are not human-readable as plain text.
- The program does not include advanced validation for duplicate IDs or invalid marks.
- The data files are created in the same directory from which the program is executed.

## Future Improvements

Some possible improvements for this project include:

- Add input validation and error handling.
- Prevent duplicate student IDs.
- Support names containing spaces using `getline()`.
- Add sorting by ID, name, or marks.
- Calculate grades or percentages automatically.
- Add a graphical user interface (GUI).
- Improve file handling and data recovery mechanisms.

## Learning Outcomes

This project demonstrates the basics of:

- Structures in C++
- Functions and modular programming
- Menu-driven programs
- Binary file handling
- Reading and writing records to files
- Searching, updating, and deleting stored records

## License

This project is open for educational and personal use. You may modify and improve it as needed.
