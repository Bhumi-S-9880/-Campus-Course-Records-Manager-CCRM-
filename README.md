# -Campus-Course-Records-Manager-CCRM-
# Campus Course & Records Manager (CCRM)

This project is a console-based Java application for managing students, courses, enrollments, and records for an educational institute, as per the project requirements.

## How to Run

1.  **Prerequisites**:
    * Java Development Kit (JDK) Version: `[Enter your JDK version, e.g., JDK 21]` 
    * An IDE like IntelliJ IDEA or Eclipse.

2.  **Execution Commands**:
    * Clone the repository: `git clone [Your Repository URL]`
    * Navigate to the source directory.
    * Compile the project: `javac --enable-preview --source 21 -d out src/edu/ccrm/cli/CCRM_App.java` (Adjust for your specific file structure and JDK version)
    * Run the application: `java -cp out edu.ccrm.cli.CCRM_App` 

3.  **Enabling Assertions**:
    * To run the program with assertions enabled, use the `-ea` flag: `java -ea -cp out edu.ccrm.cli.CCRM_App` 

---

## Java Platform Concepts

This section covers the mandatory theoretical explanations required by the project statement.

### Evolution of Java 
* **1995**: Java 1.0 is officially released by Sun Microsystems.
* **2004**: Java 5 (J2SE 5.0) is released, introducing major features like generics, enums, and annotations.
* **2014**: Java 8 is released, introducing lambdas, the Stream API, and a new Date/Time API.
* **2018**: Java 11 is released as a Long-Term Support (LTS) version.
* **2021/2023**: Java 17 and 21 are released as the latest LTS versions, bringing features like records, sealed classes, and virtual threads.

### Java Editions: ME vs SE vs EE 

| Feature         | Java ME (Micro Edition)              | Java SE (Standard Edition)          | Java EE (Enterprise Edition)         |
| --------------- | ------------------------------------ | ----------------------------------- | ------------------------------------ |
| **Primary Use** | Mobile, embedded devices, IoT        | Desktop & Server applications       | Large-scale, web, enterprise apps    |
| **Core API** | Subset of SE API, device-specific    | Core Java language & standard libs  | Superset of SE API                   |
| **Key Techs** | MIDP, CLDC                           | JDK (Compiler, JVM), Swing, JavaFX  | Servlets, JSP, EJB, JPA, REST APIs   |

### Java Architecture: JDK, JRE, JVM 

* **JVM (Java Virtual Machine)**: An abstract machine that provides the runtime environment in which Java bytecode can be executed. It is platform-dependent and interprets the compiled `.class` files.
* **JRE (Java Runtime Environment)**: A software package that contains what is required to run a Java program. It includes the JVM, standard libraries, and other components. You need the JRE to *run* Java applications.
* **JDK (Java Development Kit)**: A full-featured software development kit for Java. It contains everything in the JRE, plus development tools like the compiler (`javac`) and debugger (`jdb`). You need the JDK to *develop* Java applications.

---

## Design Justifications

### Interface vs. Abstract Class Inheritance 
In this project, `Person` was chosen as an **abstract class** because `Student` and `Instructor` share common state (fields like `id`, `name`) and identity. An abstract class allows us to define this common state and behavior in one place. An **interface** like `Searchable<T>` would be used to define a *capability* (like the ability to be searched) that could be applied to otherwise unrelated classes.

### Errors vs. Exceptions 
* **Error**: Represents serious problems that a reasonable application should not try to catch, such as `OutOfMemoryError` or `StackOverflowError`. These are typically unrecoverable issues related to the JVM environment itself.
* **Exception**: Represents conditions that a reasonable application might want to catch and handle. They are further divided into:
    * **Checked Exceptions**: Must be declared or handled (e.g., `IOException`). They represent predictable problems.
    * **Unchecked (Runtime) Exceptions**: Do not need to be declared (e.g., `NullPointerException`). They often represent programming errors.

---

---

## Acknowledgements
* This project was completed as part of the Programming in Java course.
