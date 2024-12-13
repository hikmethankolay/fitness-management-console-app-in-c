# Fitness Management System App

## **I. Introduction**

The Fitness Management System is a project built using C with CMake for cross-platform support, along with Doxygen for code documentation and unit tests. It is a console application that uses keyboard inputs for navigation.

## **II. System Architecture**

The system uses standard C and C# file input/output libraries with custom file operation functions designed for this project:

- **file_read()** – Reads data from a file
- **file_write()** – Deletes all existing data and writes new data to the file
- **file_edit()** – Modifies a specified record line
- **file_line_delete()** – Deletes a specified record line
- **file_append()** – Adds a new record at the end of the file

## **III. Functionalities**

The system provides functionalities to view, register, update, and delete records through a menu-driven interface. Additional features include search and sort capabilities. The system manages the following types of data:

### **a. Member Management:**
- MemberID
- Full Name
- Birth Date
- Phone Number
- First Registration Date

### **b. Subscription Management:**
- MemberID
- Starting Date
- Finishing Date
- Subscription Tier

### **c. Class Management:**
- Tutor Name
- Date
- Starting Hour
- Finishing Hour
- Student List

### **d. Payment Management:**
- MemberID
- Paid Amount
- Payment Date
- Next Payment Date

Additional features include:
- **LCS System:** Warns users when entering very similar records.
- **OTP System:** Requires users to enter a one-time password when logging in.
- **Huffman Coding Algorithm:** Compresses files for efficient storage.

## **IV. Testing and Validation**

The system has been thoroughly tested and documented using GoogleTest (gtest), CTest, and Xunit. The tests achieved 95% coverage with 100% success in unit test results.

## **Requirements**

- **CMake** ≥ 3.12
- **C++ Standard** ≥ 11
- **GoogleTest** (for testing modules)
- **Visual Studio Community Edition** (for Windows generator)
- **Ninja** (for WSL/Linux)

## **Setup Development Environment**

### **Step 1: Pre-commit Setup** (Run on Windows, May Affect WSL)
Run `1-configure-pre-commit.bat` to copy the pre-commit script to `.git/hooks`. This script validates README.md, `.gitignore`, and Doxygen files, and formats the code using the AStyle tool.

### **Step 2: Create Gitignore** (Run on Windows, May Affect WSL)
If `.gitignore` is missing, execute `2-create-git-ignore.bat` to generate it.

### **Step 3: Install Package Managers** (Only Windows)
Run `3-install-package-manager.bat` to install `choco` and `scoop` package managers.

### **Step 4: Install Required Applications** (Only Windows)
Execute `4-install-windows-environment.bat` to install the necessary applications.

### **Step 5: Setup WSL Environment** (Only WSL)
Open PowerShell as administrator, enter WSL, navigate to the project folder, and run `4-install-wsl-environment.sh` to configure the WSL environment.

## **Generate Development Environment**

To generate a Visual Studio Community Edition project, run `9-clean-configure-app-windows.bat`. Alternatively, you can use CMake for project development within Visual Studio.

## **Build, Test, and Package the Application**

### **On Windows:**
Run `7-build-app-windows.bat` to build, test, and generate packaged binaries for the application.

Additional scripts:
- `7-build-doc-windows.bat`: Generate documentation only
- `8-build-test-windows.bat`: Test the application only

### **On WSL:**
Run `7-build-app-linux.sh` to build, test, and generate packaged binaries in the WSL environment.

## **Clean Project**

Run `9-clean-project.bat` to clean all project outputs.

## **Supported Platforms**

![Ubuntu badge](assets/badge-ubuntu.svg)
![macOS badge](assets/badge-macos.svg)
![Windows badge](assets/badge-windows.svg)

## **Test Coverage Ratios**

> **Note**: Due to a known bug in Doxygen, badges with the same name in different folders may overwrite each other in the output directory. Refer to the README.md and web pages for the correct badges.

### **Coverage Comparison**

| Coverage Type | Windows OS                                                             | Linux OS (WSL-Ubuntu 20.04)                                              |
| ------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Line Based    | ![Line Coverage](assets/codecoveragelibwin/badge_linecoverage.svg)     | ![Line Coverage](assets/codecoverageliblinux/badge_linecoverage.svg)     |
| Branch Based  | ![Branch Coverage](assets/codecoveragelibwin/badge_branchcoverage.svg) | ![Branch Coverage](assets/codecoverageliblinux/badge_branchcoverage.svg) |
| Method Based  | ![Method Coverage](assets/codecoveragelibwin/badge_methodcoverage.svg) | ![Method Coverage](assets/codecoverageliblinux/badge_methodcoverage.svg) |

### **Documentation Coverage Ratios**

|                    | Windows OS                                                        | Linux OS (WSL-Ubuntu 20.04)                                         |
| ------------------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Coverage Ratio** | ![Line Coverage](assets/doccoveragelibwin/badge_linecoverage.svg) | ![Line Coverage](assets/doccoverageliblinux/badge_linecoverage.svg) |

---

$End-Of-File$

