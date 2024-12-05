# ChatGPT-Prompt-Templates
A concise collection of prompts for generating and reviewing Unity C# code for VR development. Focuses on clean naming conventions, namespace consistency, VR performance optimizations, async/await usage, proper lifecycle management, and writing maintainable, testable code.

## Standard Prompt for Code Generation

```
I need to implement...

[Insert Problem Statement Here]

Which is written in Unity C#.

Key requirements:
1.1) Variable and Method Conventions: Private variables are prefixed with an underscore (_), and no private keyword is used. The same rule applies to private methods.
1.2) Namespace Consistency: Use KOVR.Runtime as the namespace.
1.3) Code Quality: Write clean, modern, and organized code with descriptive variable and method names. Avoid unnecessary comments unless clarification is needed.
1.4) Global Variables: Minimize or eliminate them.
1.5) "Magic Numbers": Avoid them by using constants or configurations instead.
1.6) Line Length: Limit to 100-120 characters for readability.
1.7) Async/Await: Use Async/Await for asynchronous tasks instead of Coroutines.

Additional Considerations:
2.1) Gracefully handle errors and edge cases.
2.2) Structure code for testability, including example unit tests where relevant.
2.3) Follow Unity C# best practices, such as using the Unity Job System or Burst Compiler if applicable.
2.4) Ensure the script handles lifecycle events like OnDestroy gracefully to prevent errors during scene transitions.
Safeguard against ongoing coroutines, async/await(s), events, or callbacks running after destruction.
```

## Reviewing Code (Whether it is AI or Human Generated)

```
Please review the following code written in Unity C#

[Insert Code Here]

Please analyze the code provided above. Consider the following aspects during your review:
1.1) Code Quality and Adherence to Best Practices: Evaluate naming conventions, modularity, and clarity.
1.2) Potential Bugs or Edge Cases: Highlight possible errors or scenarios where the code might fail.
1.3) Performance Optimizations: Suggest ways to improve efficiency, especially for VR or high-performance scenarios if applicable.
1.4) Readability and Maintainability: Assess how easy the code is to understand and modify.
1.5) Security Concerns: Identify any potential vulnerabilities, especially for sensitive operations like networking.
1.6) Lifecycle Handling during Scene Transitions: Ensure the script handles lifecycle events like OnDestroy gracefully to prevent errors during scene transitions.
Safeguard against ongoing coroutines, async/await(s), events, or callbacks running after destruction.

Follow my code style preferences:
2.1) Private variables should not use the private keyword and should be prefixed with _.
2.2) Namespaces should be consistent [Insert Namespace].
2.3) Avoid "magic numbers" and use constants instead.
2.4) Enums over Magic Strings: Replace repetitive strings with enums where applicable to improve maintainability and avoid typos.
2.5) Global Variables: Minimize or eliminate them.
2.6) Line Length: Limit to 100-120 characters for readability.
2.7) Assume this is for a Unity VR application or Mobile application. Optimize the code accordingly.
2.8) Serialization: Clearly define which variables need [SerializeField] or [NonSerialized] attributes, ensuring data integrity between scenes and runtime. Variables with [SerializeField] should follow 2.1) 
2.9) Code Grouping: Organize code logically (e.g., grouping public methods, private methods, and Unity event methods together for clarity).
```

## Generating Unit Tests

```
Generate unit tests in Unity C# for the following function:

[Insert Function Here]

Please include:
1) Setup and Teardown Methods
2) Edge case tests
3) Invalid Input tests
4) Valid Input tests

Use syntax from these Unity C# libraries (if applicable)
a) System.Reflection;
b) NUnit.Framework;
```
