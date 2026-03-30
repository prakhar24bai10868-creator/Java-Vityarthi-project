# Campus Course & Records Manager (CCRM)

## Project Overview

The Campus Course & Records Manager (CCRM) is a console-based Java application designed to manage student records, course information, enrollment processes, and academic transcripts for educational institutions. This comprehensive system demonstrates advanced Java SE concepts including OOP principles, modern I/O operations, design patterns, and robust exception handling.

## How to Run

### Prerequisites
- **JDK Version**: Java 17 or higher
- **IDE**: Eclipse IDE (recommended) or any Java IDE
- **OS**: Windows (installation guide provided below)

### Running the Application
```bash
# Compile the project
javac -d bin src/edu/ccrm/cli/CCRMApplication.java

# Run with assertions enabled
java -ea -cp bin edu.ccrm.cli.CCRMApplication

# Or run directly from Eclipse IDE using the provided run configuration
```

### Sample Commands
```bash
# Enable assertions when running
java -ea -cp bin edu.ccrm.cli.CCRMApplication

# Import sample data
# Use option 5 from main menu -> Import Data -> select test-data/students.csv
```

## Evolution of Java

### Timeline of Java Evolution
- **1995**: Java 1.0 - Initial release by Sun Microsystems
- **1997**: Java 1.1 - Inner classes, JDBC, RMI introduced
- **1998**: Java 1.2 (J2SE) - Collections Framework, Swing GUI
- **2000**: Java 1.3 - HotSpot JVM, JavaSound API
- **2002**: Java 1.4 - Assertions, NIO, Regular expressions
- **2004**: Java 5.0 - Generics, Annotations, Enums, Autoboxing
- **2006**: Java 6 - Performance improvements, Web services
- **2011**: Java 7 - Diamond operator, Try-with-resources
- **2014**: Java 8 - Lambda expressions, Stream API, Date/Time API
- **2017**: Java 9 - Module system, JShell
- **2018**: Java 10 - Local variable type inference (var)
- **2018**: Java 11 - Long-term support (LTS), HTTP Client API
- **2019**: Java 12-13 - Switch expressions, Text blocks
- **2020**: Java 14-15 - Records, Sealed classes (preview)
- **2021**: Java 16-17 (LTS) - Pattern matching, Strong encapsulation
- **2022-Present**: Java 18+ - Continued performance and language enhancements

## Java Platform Editions Comparison

| Feature | Java ME (Micro Edition) | Java SE (Standard Edition) | Java EE (Enterprise Edition) |
|---------|------------------------|----------------------------|-------------------------------|
| **Target Platform** | Mobile devices, embedded systems | Desktop applications, standalone apps | Enterprise web applications, servers |
| **Application Types** | Mobile apps, IoT devices, smart cards | Desktop GUI apps, console applications | Web applications, enterprise services |
| **API Scope** | Minimal API subset for constrained devices | Full core Java APIs | SE APIs + enterprise APIs (servlets, EJB, JPA) |
| **Memory Footprint** | Very small (KBs to few MBs) | Moderate (10s to 100s of MBs) | Large (100s of MBs to GBs) |
| **Deployment** | Embedded in devices | Local installation | Application servers (Tomcat, WebLogic) |
| **Examples** | Feature phones, smart watches | NetBeans, Eclipse IDE, CCRM project | Banking systems, e-commerce websites |

## Java Architecture: JDK, JRE, JVM

### Java Virtual Machine (JVM)
- **Purpose**: Runtime environment that executes Java bytecode
- **Function**: Provides platform independence by translating bytecode to machine code
- **Components**: Class loader, Memory areas (Heap, Stack), Execution engine, Garbage collector

### Java Runtime Environment (JRE)
- **Purpose**: Provides runtime environment for Java applications
- **Components**: JVM + Core libraries + Supporting files
- **Usage**: Required to run Java applications (end-user installation)

### Java Development Kit (JDK)
- **Purpose**: Complete development environment for Java
- **Components**: JRE + Development tools (javac, javadoc, jar, debugger)
- **Usage**: Required for developing Java applications

### How They Interact
```
JDK (Development)
├── JRE (Runtime)
│   ├── JVM (Execution)
│   └── Core Libraries
└── Development Tools (javac, jar, javadoc)
```

## Java Installation on Windows

### Step 1: Download JDK
1. Visit [Oracle JDK Downloads](https://www.oracle.com/java/technologies/javase-downloads.html)
2. Select JDK 17 or higher for Windows x64
3. Download the installer (.exe file)

### Step 2: Install JDK
1. Run the downloaded installer as administrator
2. Follow installation wizard (default settings recommended)
3. Note installation path (typically `C:\Program Files\Java\jdk-17`)

### Step 3: Set Environment Variables
1. Open System Properties → Advanced → Environment Variables
2. Add `JAVA_HOME`: `C:\Program Files\Java\jdk-17`
3. Update `PATH`: Add `%JAVA_HOME%\bin`

### Step 4: Verify Installation
```cmd
java -version
javac -version
```

**Screenshot**: `screenshots/java-installation-verification.png`

## Eclipse IDE Setup

### Step 1: Download Eclipse
1. Download Eclipse IDE for Java Developers
2. Extract to desired location (e.g., `C:\eclipse`)

### Step 2: Create New Project
1. File → New → Java Project
2. Project name: `CCRM`
3. Use default JRE (should detect installed JDK)
4. Create separate folders for source and class files

### Step 3: Configure Run Configuration
1. Right-click project → Run As → Run Configurations
2. Create new Java Application configuration
3. Main class: `edu.ccrm.cli.CCRMApplication`
4. VM arguments: `-ea` (enable assertions)

**Screenshots**:
- `screenshots/eclipse-project-setup.png`
- `screenshots/eclipse-run-configuration.png`

## Project Structure

```
CCRM/
├── src/
│   └── edu/
│       └── ccrm/
│           ├── cli/           # Command-line interface
│           ├── config/        # Configuration and builders
│           ├── domain/        # Domain models and entities
│           ├── io/           # File I/O operations
│           ├── service/      # Business logic services
│           └── util/         # Utility classes
├── test-data/               # Sample CSV files
├── screenshots/            # Project screenshots
├── exports/               # Generated export files
├── backups/              # Backup directories
└── README.md
```

## Syllabus Topics Mapping Table

| Syllabus Topic | File/Class/Method Location | Description |
|----------------|---------------------------|-------------|
| **Language & Core** |
| Main class & Java syntax | `edu.ccrm.cli.CCRMApplication.main()` | Entry point with proper Java syntax |
| Package organization | `edu.ccrm.*` packages | Clear package structure as specified |
| Primitive variables | `domain/Student.java`, `domain/Course.java` | int id, boolean status, double gpa |
| Objects & operators | `util/ValidationUtils.java.validateEmail()` | String operations, logical operators |
| Operator precedence | `service/GradeService.computeGPA()` | Documented arithmetic precedence |
| **Decision Structures** |
| if/if-else/nested if-else | `cli/StudentMenu.handleStudentOperations()` | Nested decision logic |
| Switch statement | `cli/CCRMApplication.handleMainMenu()` | Enhanced switch for menu |
| **Loops & Control** |
| while loop | `cli/InputValidator.getValidatedInput()` | Input validation loop |
| do-while loop | `cli/CCRMApplication.main()` | Main program loop |
| for loop | `service/ReportService.generateGPADistribution()` | Array/collection iteration |
| Enhanced for | `service/CourseService.searchByDepartment()` | Collection traversal |
| break/continue | `io/CSVParser.parseStudentLine()` | Loop control with labeled break |
| **Arrays & Strings** |
| Arrays & Arrays class | `util/SortingUtils.sortStudentsByGPA()` | Array sorting and searching |
| String methods | `util/StringUtils.formatName()` | substring, split, join, equals, compareTo |
| **OOP - Four Pillars** |
| Encapsulation | `domain/Student.java` | Private fields with getters/setters |
| Inheritance | `domain/Person.java` → `Student.java`, `Instructor.java` | Abstract parent class |
| Abstraction | `domain/Person.java.getDisplayInfo()` | Abstract methods implementation |
| Polymorphism | `service/PersonService.processPersons()` | Virtual method invocation |
| **Access Levels** |
| private | `domain/Course.credits` | Private field access |
| protected | `domain/Person.dateCreated` | Protected for subclasses |
| default | `util/ValidationHelper` | Package-private utility class |
| public | `service/*.java` public methods | Public API methods |
| **Inheritance & Constructors** |
| Constructor inheritance | `domain/Student.java` constructors | super() calls demonstration |
| Types of inheritance | `domain/Person` hierarchy | Single inheritance example |
| super keyword | `domain/Student.toString()` | Calling parent methods |
| **Immutability** |
| Immutable class | `domain/CourseCode.java` | Final fields, defensive copying |
| Final fields | `domain/CourseCode.code` | Immutable value object |
| **Nested Classes** |
| Static nested class | `domain/Course.Builder` | Builder pattern implementation |
| Inner class | `cli/MenuHandler.InputListener` | Non-static inner class |
| **Interfaces** |
| Interface definition | `service/Persistable.java` | save(), load() methods |
| Generic interface | `service/Searchable<T>.java` | Generic search contract |
| Diamond problem | `service/StudentService` implements multiple | Default method resolution |
| Interface vs class | README section | Design decision justification |
| **Functional Programming** |
| Functional interfaces | `util/StudentComparators.java` | Comparator lambdas |
| Lambda expressions | `service/ReportService.filterByGPA()` | Predicate lambdas |
| Anonymous inner class | `cli/MenuHandler.createExitHandler()` | Event handler implementation |
| **Enums** |
| Enum with constructor | `domain/Semester.java` | Constructor and fields |
| Enum with fields | `domain/Grade.java` | Grade points and descriptions |
| **Advanced OOP** |
| Upcast & downcast | `service/PersonService.processSpecialized()` | instanceof checks |
| Method overriding | `domain/Student.toString()` | Override parent methods |
| Method overloading | `domain/Student.updateInfo()` | Multiple signatures |
| **Design Patterns** |
| Singleton pattern | `config/AppConfig.getInstance()` | Thread-safe singleton |
| Builder pattern | `domain/Course.Builder.java` | Fluent builder interface |
| **Exception Handling** |
| Checked exceptions | `io/FileOperations.java` | IOException handling |
| Unchecked exceptions | `service/EnrollmentService.java` | RuntimeException subclasses |
| Custom exceptions | `exception/DuplicateEnrollmentException.java` | Domain-specific exceptions |
| try/catch/finally | `io/BackupService.createBackup()` | Resource management |
| Multi-catch | `io/ImportService.importData()` | Multiple exception types |
| throw/throws | `service/ValidationService.validate()` | Exception propagation |
| Assertions | `domain/Course.setCredits()` | Invariant checking |
| **File I/O (NIO.2)** |
| Path & Files API | `io/FileOperations.java` | Path manipulation |
| File operations | `io/BackupService.java` | copy, move, exists, delete |
| Stream I/O | `io/CSVExporter.writeStudents()` | Lines processing |
| File walking | `util/DirectoryUtils.calculateSize()` | Recursive directory traversal |
| **Streams API** |
| Stream pipeline | `service/ReportService.generateStatistics()` | filter, map, collect operations |
| Aggregation operations | `service/GradeService.calculateAverages()` | reduce, groupingBy collectors |
| **Date/Time API** |
| LocalDateTime | `domain/Enrollment.enrollmentDate` | Modern date/time usage |
| Timestamp formatting | `io/BackupService.generateTimestamp()` | DateTimeFormatter usage |
| **Recursion** |
| Recursive method | `util/DirectoryUtils.calculateSizeRecursive()` | Directory size calculation |
| Recursive file listing | `util/FileTreePrinter.printTree()` | Depth-based file listing |

## Enabling Assertions

Assertions are used throughout the project to validate invariants and preconditions. To enable assertions:

### Command Line
```bash
java -ea edu.ccrm.cli.CCRMApplication
# or
java -enableassertions edu.ccrm.cli.CCRMApplication
```

### Eclipse IDE
1. Run → Run Configurations
2. Select your configuration
3. Arguments tab → VM arguments: `-ea`

### Sample Assertion Usage
```java
// In Course.setCredits()
assert credits > 0 && credits <= 6 : "Credits must be between 1 and 6";

// In Student.enroll()
assert course != null : "Course cannot be null for enrollment";
```

## Sample Data Files

The `test-data/` folder contains sample CSV files for testing import functionality:

- `students.csv` - Sample student records
- `courses.csv` - Sample course catalog
- `enrollments.csv` - Sample enrollment data

## Program Screenshots

1. **JDK Installation Verification**: `screenshots/java-installation-verification.png`
2. **Eclipse Project Setup**: `screenshots/eclipse-project-setup.png`
3. **Program Main Menu**: `screenshots/program-main-menu.png`
4. **Student Management Operations**: `screenshots/student-operations.png`
5. **Export/Backup Structure**: `screenshots/export-backup-structure.png`

## Architecture Notes

### Why Interface vs Class Inheritance

**Interfaces Used When**:
- `Persistable` - Multiple unrelated classes need save/load capability
- `Searchable<T>` - Generic search behavior across different entity types
- Multiple inheritance of type needed (behavior contracts)

**Abstract Classes Used When**:
- `Person` - Shared implementation and state between Student/Instructor
- Common fields and methods with specialized behavior
- Single inheritance hierarchy with shared code

### Java SE vs ME vs EE in This Project

This CCRM project is built using **Java SE** because:
- **Desktop Application**: Console-based local application
- **Core APIs**: Uses standard collections, I/O, date/time APIs
- **No Enterprise Features**: No web services, distributed computing, or server deployment
- **Standalone Deployment**: Runs independently without application server

## Acknowledgments

- Java Documentation and Oracle tutorials for best practices
- Design pattern examples from Gang of Four patterns
- NIO.2 implementation patterns from Java documentation
- All code implementation is original work by the author

## License

This project is created for educational purposes as part of Java programming coursework.
