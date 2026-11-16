# Algorithm Battle – Which Data Structure Wins?

## Student details
- **Name:** Mohamed Naffies J
- **Register Number:** RA2511042050007

## Project overview
A C-based Student Record Management System comparing:
- **Binary Search Tree (BST)** for ordered record storage.
- **AVL Tree** for self-balancing search.
- **Hash Table with Linear Probing** for key-based lookup.

Each record contains a Student ID, name, department and marks.

## Dataset
The program uses 30 new records in a mixed insertion order. IDs range from 4103 to 4196 (not every ID in the range is used).

| Student ID | Name | Department | Marks |
|---:|---|---|---:|
| 4103 | Aarav | CSE | 88 |
| 4120 | Ahamed | ECE | 76 |
| 4137 | Akash | IT | 91 |
| 4154 | Arjun | EEE | 83 |
| 4171 | Ashwin | AIML | 96 |
| 4188 | Bharath | CSE | 72 |
| 4109 | Charvik | ECE | 89 |
| 4126 | Dhanush | IT | 94 |
| 4143 | Faris | EEE | 81 |
| 4160 | Gautham | AIML | 98 |
| 4177 | Harish | CSE | 77 |
| 4194 | Ibrahim | ECE | 90 |
| 4115 | Jeevan | IT | 92 |
| 4132 | Karthik | EEE | 79 |
| 4149 | Lokesh | AIML | 86 |
| 4166 | Madhan | CSE | 93 |
| 4183 | Naveen | ECE | 75 |
| 4105 | Pranav | IT | 88 |
| 4122 | Rahul | EEE | 97 |
| 4139 | Sanjay | AIML | 84 |
| 4156 | Tharun | CSE | 95 |
| 4173 | Umar | ECE | 80 |
| 4190 | Varun | IT | 91 |
| 4111 | Vignesh | EEE | 82 |
| 4128 | Yashwanth | AIML | 89 |
| 4145 | Abinash | CSE | 74 |
| 4162 | Dinesh | ECE | 99 |
| 4179 | Ezhil | IT | 87 |
| 4196 | Faizal | EEE | 93 |
| 4117 | Gokul | AIML | 85 |

## Operations
1. Search using BST
2. Search using AVL Tree
3. Search using Hashing
4. Display BST traversals
5. Display AVL traversals
6. Display Hash Table
7. Insert a new student
8. Run performance experiment
9. Display all student records
0. Exit

## Configuration
| Parameter | Value |
|---|---|
| Initial records | 30 |
| Maximum capacity | 100 |
| Hash table size | 47 |
| Hash function | `h(id) = id % 47` |
| Collision handling | Linear probing |
| Successful search key | 4166 |
| Unsuccessful search key | 4299 |
| Insert test | 4201 |

## Measured performance
These values were obtained by compiling and running the supplied `student.c` with the dataset above.

| Measurement | BST | AVL Tree | Hash Table |
|---|---:|---:|---:|
| Height (nodes) | 9 | 6 | Not applicable |
| Successful search (4166) | 7 comparisons | 4 comparisons | 1 probes |
| Unsuccessful search (4299) | 8 comparisons | 5 comparisons | 2 probes |
| Insertion collisions | Not applicable | Not applicable | 7 |

The results depend on the insertion order and hash function. The mixed order avoids a fully skewed BST, while the AVL tree maintains balance.

## Compile and run
```bash
gcc -std=c99 -Wall -Wextra student.c -o student
./student
```
On Windows with GCC/MinGW:
```bash
gcc -std=c99 -Wall -Wextra student.c -o student.exe
student.exe
```

## Repository structure
```text
Algorithm_Battle_Submission/
├── student.c
├── student
├── README.md
├── report.docx
└── Screenshots/
    ├── initial_dataset.png
    ├── bst_successful_search_4166.png
    ├── avl_successful_search_4166.png
    ├── hash_successful_search_4166.png
    ├── bst_unsuccessful_search_4299.png
    ├── avl_unsuccessful_search_4299.png
    ├── hash_unsuccessful_search_4299.png
    ├── bst_traversals.png
    ├── avl_traversals.png
    ├── hash_table.png
    ├── performance_comparison.png
    └── insert_student_4201.png
```

## GitHub reference
https://github.com/Navin-13/algorithm-Battle

The GitHub URL is a reference link. The files in this ZIP are a separate locally revised copy.
