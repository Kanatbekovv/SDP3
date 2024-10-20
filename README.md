1. Implementation of Design Patterns
1.1. Command Pattern (Command.java)

    Pattern Overview: The Command Pattern encapsulates a request as an object, allowing clients to be parameterized with queues, logs, and callback functions. It separates the object invoking the operation from the one that knows how to perform it, enabling more flexible command execution.
    Implementation Details in Command.java:
        The cmd interface defines an execute() method implemented by various command classes, such as PrintCommand, SaveCommand, and DeleteCommand, which perform specific actions like printing, saving, or deleting a task.
        The TaskCommand class holds task details (e.g., task name) that are passed to the respective command.
        The CallCommand class acts as an invoker, setting the current command and executing it by calling the execute() method.
    Example Execution in Code:
        In the main method, several commands (PrintCommand, SaveCommand, DeleteCommand) are created to perform different actions on a TaskCommand object.
        The CallCommand object sequentially executes the commands by setting each one and calling execute().

1.2. Chain of Responsibility Pattern (Chain.java)

    Pattern Overview: The Chain of Responsibility Pattern allows a request to be passed along a chain of handlers. Each handler decides whether to handle the request or pass it to the next handler in the chain.
    Implementation Details in Chain.java:
        The TaskChain class encapsulates the task details, including its name and priority (low, medium, or high).
        The abstract Handler class defines a handleRequest(TaskChain task) method, implemented by concrete handler classes: LowPH, MedPH, and HighPH. Each handler checks the task's priority and either handles it or passes it to the next handler.
        In the code, the handlers are linked in a chain, processing tasks in order of priority (from low to high).
    Example Execution in Code:
        In the main method, several tasks with different priorities (Low, Medium, High) are created.
        The chain of handlers processes each task based on its priority, either handling it or passing it along.
        
