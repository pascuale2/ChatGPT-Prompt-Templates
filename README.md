# ChatGPT-Prompt-Templates
A concise collection of prompts for generating and reviewing Unity C# code for VR development. Focuses on clean naming conventions, namespace consistency, VR performance optimizations, async/await usage, proper lifecycle management, and writing maintainable, testable code.

## Standard Prompt for Code Generation

```
I need to implement [insert problem statement]

Which is written in Unity C#.

Key requirements:
1) Variable and Method Conventions: Private variables are prefixed with an underscore (_), and no private keyword is used. The same rule applies to private methods.
2) Namespace Consistency: Use KOVR.Runtime as the namespace.
3) Code Quality: Write clean, modern, and organized code with descriptive variable and method names. Avoid unnecessary comments unless clarification is needed.
4) Global Variables: Minimize or eliminate them.
5) "Magic Numbers": Avoid them by using constants or configurations instead.
6) Line Length: Limit to 100-120 characters for readability.
7) Async/Await: Use Async/Await for asynchronous tasks instead of Coroutines.

Additional Considerations:
11) Gracefully handle errors and edge cases.
12) Optimize for performance with VR-specific needs, such as minimizing draw calls and optimizing shaders.
13) Structure code for testability, including example unit tests where relevant.
14) Follow Unity C# best practices, such as using the Unity Job System or Burst Compiler if applicable.
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
1.6) Lifecycle Handling during Scene Transitions: Ensure the script handles lifecycle events like OnDestroy gracefully to prevent errors during scene transitions. Safeguard against ongoing coroutines, events, or callbacks running after destruction.

Follow my code style preferences:
2.1) Private variables should not use the private keyword and should be prefixed with _.
2.2) Namespaces should be consistent (KOVR.Runtime).
2.3) Avoid "magic numbers" and use constants instead.
2.4) Global Variables: Minimize or eliminate them.
2.5) "Magic Numbers": Avoid them by using constants or configurations instead.
2.6) Line Length: Limit to 100-120 characters for readability.
2.7) Assume this is for a Unity VR application. Optimize the code accordingly.
2.8) Serialization: Clearly define which variables need [SerializeField] or [NonSerialized] attributes, ensuring data integrity between scenes and runtime. Variables with [SerializeField] should follow 2.1) 
2.9) Code Grouping: Organize code logically (e.g., grouping public methods, private methods, and Unity event methods together for clarity).
2.10) Enums over Magic Strings: Replace repetitive strings with enums where applicable to improve maintainability and avoid typos.
```
