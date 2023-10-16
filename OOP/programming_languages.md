# Java
## Java Virtual Machine

**The Java Virtual Machine (JVM)** is an execution environment for Java applications. It is one of the most crucial components of the Java platform, ensuring hardware and operating system independence during the execution of Java applications. A Java application doesn't run directly on the operating system but instead operates within a virtual machine running on the system, providing an abstraction layer between the Java application and the underlying system.

The virtual machine enables several functions, including:

- Bytecode interpretation
- Interaction with the operating system
- Memory management through garbage collection

Its operation is somewhat analogous to that of a computer: it executes instructions that manipulate various dedicated memory areas within the JVM.

A Java application does not make direct calls to the operating system (except when using JNI). It solely utilizes APIs, which are largely written in Java, with a few being native. This approach allows Java to make applications independent of the runtime environment.

The virtual machine doesn't have knowledge of the Java language itself; it only deals with the bytecode resulting from the compilation of source code written in Java.

# C#

## .NET

**.NET** is a software development platform developed by Microsoft. It provides a comprehensive development environment and a framework for creating a wide variety of applications, ranging from desktop applications to web and mobile applications.

- .NET Core uses JIT(Just-in-Time Compilation) compilation, which means that the source code is compiled into native machine code at runtime. This allows .NET Core to adapt to the specificities of each target operating system.

- .NET Core introduced universal libraries that offer enhanced compatibility across different platforms. These libraries are designed to be platform-independent and support a wide range of scenarios.
