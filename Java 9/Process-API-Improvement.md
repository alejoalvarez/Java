# Process API Improvement

Java has improved its process API in Java 9 version that helps to manage and control operating system processes.

In earlier versions, it was complex to manage and control operating system processes by using Java programming. Now, new classes and interfaces are added to perform this task.

New methods are added to the **java.lang.Process** class that are tabled below.

|Modifier and Type|	Method|	Description|
|---|---|---|
|boolean	| supportsNormalTermination()	|It returns true if the implementation of destroy() is to normally terminate the process, else returns false.|
|ProcessHandle |	toHandle() |	It returns a ProcessHandle for the Process.|
|long |	pid()	| It returns the native process ID of the process.|
|Stream<ProcessHandle>	| children()	| It returns a snapshot of the direct children of the process.|
|Stream<ProcessHandle> |	descendants()	|It returns a snapshot of the descendants of the process.|
|ProcessHandle.Info	|info()|	It returns a snapshot of information about the process.|
|CompletableFuture<Process>	|onExit() |	It returns a CompletableFuture<Process> for the termination of the Process.|

New interfaces ProcessHandle and ProcessHandle.Info are added.

## ProcessHandle Interface

ProcessHandle helps to handle and control processes. We can monitor processes, list its children, get information etc.

This interface contains static factory methods that return instances that are value-based, immutable and thread-safe.

## ProcessHandle Interface Signature

```java
public interface ProcessHandle extends Comparable<ProcessHandle>  
```

This interface contains the following methods.

| Modifier and Type|	Method|	Description|
|---|---|---|
|static Stream<ProcessHandle>|	allProcesses() |	It returns a snapshot of all processes visible to the current process.|
|Stream<ProcessHandle>	| children()	| It returns a snapshot of the current direct children of the process.|
|int	|compareTo(ProcessHandle other)	|It compares this ProcessHandle with the specified ProcessHandle for order.|
|static ProcessHandle	|current()	|It returns a ProcessHandle for the current process.|
|Stream<ProcessHandle>	|descendants()	|It returns a snapshot of the descendants of the process.|
|boolean	|destroy()|	It requests the process to be killed.|
|boolean	|destroyForcibly()|	It requests the process to be killed forcibly.|
|boolean	|equals(Object other)	| It returns true if other object is non-null, is of the same implementation, and represents the same system process; otherwise it It returns false.|
|int	|hashCode() |	It returns a hash code value for this ProcessHandle.|
| ProcessHandle.Info|info()|	It returns a snapshot of information about the process.|
|boolean |	isAlive()	|It tests whether the process represented by this ProcessHandle is alive.|
|static Optional<ProcessHandle>	|of(long pid)	|It returns an Optional<ProcessHandle> for an existing native process.|
|CompletableFuture<ProcessHandle>	|onExit()	|It returns a CompletableFuture<ProcessHandle> for the termination of the process.|
|Optional<ProcessHandle>|	parent()	|It returns an Optional<ProcessHandle> for the parent process.|
|long	|pid()|	It returns the native process ID of the process.|
|boolean|	supportsNormalTermination()	|It returns true if the implementation of destroy() normally terminates the process.|


## ProcessHandle.Info Interface

It is added to Java 9, and used to provide information about the process. It is nested interface of ProcessHandle interface.

Java ProcessHandle.Info Interface Signature

```java
public static interface ProcessHandle.Info  
```

|Modifier and Type|	Method	|Description|
|---|---|---|
|Optional<String[]>	|arguments()	|It returns an array of Strings of the arguments of the process.|
|Optional<String>	|command()	|It returns the executable pathname of the process.|
|Optional<String>	|commandLine()	|It returns the command line of the process.|
|Optional<Instant>	|startInstant()	|It returns the start time of the process.|
|Optional<Duration>	|totalCpuDuration()	|It returns the total cputime accumulated of the process.|
|Optional<String>	|user()	|It returns the user of the process.|

Java 9 Process API Example

```java
public class ProcessApiExample {  
    public static void main(String[] args) {  
        ProcessHandle currentProcess = ProcessHandle.current();     // Current processhandle  
        System.out.println("Process Id: "+currentProcess.pid());    // Process id   
        System.out.println("Direct children: "+ currentProcess.children()); // Direct children of the process  
        System.out.println("Class name: "+currentProcess.getClass());       // Class name  
        System.out.println("All processes: "+ProcessHandle.allProcesses()); // All current processes   
        System.out.println("Process info: "+currentProcess.info());         // Process info  
        System.out.println("Is process alive: "+currentProcess.isAlive());   
        System.out.println("Process's parent "+currentProcess.parent());  // Parent of the process  
    }  
} 
```

