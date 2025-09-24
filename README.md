Course-and-Credit-Management-CCRM-
CCRM is an application in Java to manage students, courses and their enrollments. It has CRUD (Create, Read, Update, Delete) operations, data import/export, data backup, and report generation.

How to Run Prerequisites: Java Development Kit (JDK) 21 or higher. Clone the repository: git clone [your-repository-url] Navigate to project root: cd CCRM Compile: javac -d bin -cp bin src/edu/ccrm/cli/MainApp.java Run the application: java -cp bin edu.ccrm.cli.MainApp

Evolution of Java 1996 (Java 1.0): Included core features like JVM and Applets. 2004 (Java 5): Introduced generics, annotations, autoboxing and enums. 2014 (Java 8): Functional programming to Java, Lambda expressions, new Date/Time API and Streams. 2017 - Present (Java 9+): Java Platform Module System (JPMS), local-variable type inference (var) and enhanced garbage collectors.

Java Platform Comparison Java SE (Java Standard Edition): General-purpose desktop & server applications. Java EE (Java Enterprise Edition): Used for building complex web services and business-tier applications. Java ME (Java Micro Edition): Formerly used for feature phone games now replaced by Android and iOS.

JDK, JRE, and JVM JDK (Java Development Kit): Full development kit for Java. It includes JRE, Java compiler (javac), debugger, and archiver. JDK is used to write and compile Java code. JRE (Java Runtime Environment): The environment required to run compiled Java programs. It includes JVM and necessary class libraries and files. JVM (Java Virtual Machine): Virtual machine that executes Java bytecode. JVM makes Java platform-independent by translating compiled bytecode into a specific operating system's native machine code.

Windows Install & Eclipse Setup:

Windows Installation Steps
Download JDK 25 installer from the official Oracle website.
Run the installer and follow the on-screen prompts.
Verify the installation by opening a new Command Prompt and typing javac -version.
Eclipse Setup Steps:

Download and Eclipse IDE for Java Developers.
Run the installer and follow the on-screen prompts.
Go to File > New > Java Project.
Provide a project name and select your installed JDK.
Syllabus Topics

Encapsulation: Student, Course and Enrollment classes. Fields are private with public getters and setters. Abstraction: StudentService, CourseService, EnrollmentService. They expose simple methods like addStudent() and enroll() and hide the underlying data structures (e.g., ArrayList). Singleton Pattern: The AppConfig class, which uses a private constructor and a get() method to ensure only one instance is ever created.

Builder Pattern: The Course.Builder inner class, used to construct Course objects with an easy-to-read, fluent syntax. Exception Handling: The try-catch blocks in MainApp and EnrollmentService that handle custom exceptions like CourseDuplicateException. File I/O: The FileUtil class, with exportData() and importData() methods. Generics: FileUtil uses generics () to handle different types of data (e.g., List) in a type-safe way. Assertions: MainApp methods such as readString() and readInt() to ensure valid user input. Lambda Expressions: showTopStudents() method in MainApp uses stream().sorted().limit().forEach() for concise data processing.

Enabling Assertions: Assertions are disabled by default at runtime for performance. To enable them, use a command-line flag. Syntax: assert : "Optional error message"; Run Command: java -ea -cp bin edu.ccrm.cli.MainApp. The -ea flag stands for "enable assertions". Sample Command: java -ea -cp bin edu.ccrm.cli.MainApp

Class vs. Interface Use Class Inheritance when the classes share a "is-a" relationship. Use it when a subclass is a specialized version of a superclass and inherits its implementation. Use Interface Implementation when the classes share a "can-do" relationship. Use it when different classes need to perform a similar action but in different ways. Errors vs. Exceptions In Java both Error and Exception are subclasses of Throwable.

Exceptions: Problems that can be handled by the program. They represent situations that can occur during normal execution like a file not being found or invalid user input.E.g IOException, NullPointerException Errors: Problems that cannot be handled by the program.They are serious unrecoverable issues that occur outside the program's control like running out of memory. E.g StackOverflowError, OutOfMemoryError.
