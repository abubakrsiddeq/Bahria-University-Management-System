# Bahria University Management System

A console-based C++ project that combines multiple university workflows in a single application, including admission, user management, course management, student/teacher portals, communication, and reporting.

## Overview

This repository contains several standalone C++ modules and combined builds created for academic project work. The most complete integrated entry point appears to be in **final.cpp**, which provides a unified main menu for:

- Admin Panel
- Student Admission Portal
- Teacher Portal
- Student Portal
- Short Courses Portal

## Key Features

- **Admin authentication** (password-protected admin menu)
- **User management** (teacher/student creation and credential handling)
- **Admission management** (student admission workflows)
- **Course management** (course-related admin operations)
- **Teacher dashboard** (lectures, assignments, quizzes)
- **Student dashboard** (view profile, lectures, assignments, quizzes)
- **Reporting and communication modules** (in dedicated source files)

## Repository Structure

- `final.cpp` — integrated system build with full menu-driven flow
- `BKRs-Combined.cpp` — large combined variant
- `combined-faizan.cpp` — alternative combined variant
- `structure.cpp` — structured/combined variant
- `admissionportal.cpp` — student-facing admission portal logic
- `admissionmanagement-admin.cpp` — admin-side admission management
- `admission-portal-combined.cpp` — combined admission implementation
- `course_portal.cpp` — course portal features
- `coursemanage-admin.cpp` — admin course management
- `student-cms.cpp` — student CMS module
- `teacherportal.cpp` — teacher portal module
- `usermange-admin.cpp` — admin user management module
- `comunication-admin.cpp` — communication module
- `reports-adminpanel.cpp` — report generation/admin reports

## Requirements

- C++ compiler with C++11+ support (GCC/Clang/MSVC)
- Terminal/console environment
- Standard C++ libraries

> Note: Some files include `conio.h` and `_getch()`, which are compiler/platform-specific (commonly available on Windows toolchains). On macOS/Linux, this may require adaptation or replacement.

## Build and Run

### Option 1: Build integrated version (recommended)

Compile and run `final.cpp` as a standalone program.

Example (macOS with Clang):

```bash
clang++ -std=c++17 final.cpp -o bums
./bums
```

Example (GCC):

```bash
g++ -std=c++17 final.cpp -o bums
./bums
```

### Option 2: Build any standalone module

Each `.cpp` file in this repository has its own `main()` in most cases, so compile one file at a time:

```bash
g++ -std=c++17 teacherportal.cpp -o teacherportal
./teacherportal
```

## Default Credentials / Access

- In the integrated `final.cpp`, the predefined admin password is:
  - **`admin123`**

Update this value in source code before production/demo use if needed.

## Usage Notes

1. Start the executable.
2. Choose the required portal from the main menu.
3. For admin actions, enter the admin password.
4. Use menu prompts to navigate module-specific operations.

## Known Limitations

- Multiple files represent parallel versions of similar functionality.
- Cross-platform compatibility may be limited by `conio.h` usage.
- Data persistence is basic and depends on file/module implementation.
- Security is educational/basic (plain-text style credential logic in places).

## Suggested Improvements

- Replace `conio.h` with portable input handling.
- Split monolithic files into headers + source modules.
- Introduce centralized data models and persistent storage (e.g., SQLite).
- Add validation, error handling, and role-based authorization.
- Add unit tests and CI build checks.

## Contributing

1. Create a feature branch.
2. Keep modules focused and avoid duplicate logic across combined files.
3. Test the target `.cpp` build before submitting changes.
4. Open a pull request with a clear summary.

## License

This project currently has no explicit license file. Add a license (e.g., MIT) if you plan to distribute or collaborate publicly.
