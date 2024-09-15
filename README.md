# Statically-Typed vs. Dynamically-Typed Languages in Video Game Development
#### By Samantha Mondragon | CPSC-354 LLM Literature Review | LLM Used: ChatGPT

## Introduction

When it comes to making video games, there are many challenging aspects to it. However, before even getting to game mechanic specifics, one has to first start out with the concepts of programming languages. The language one choses to write out their scripts can significantly impact the performance and game development process. Therefore, I set out to find out the trade-offs between static and dynamic languages, and how that may affect or benefit a game. Speciffically, I wanted to look deeper into memory management strategies and optimization.

## References

**[What is a typed language](https://www.geeksforgeeks.org/what-is-a-typed-language/)**

**[Understanding Types; Static vs Dynamic, & Strong vs Weak.](https://medium.com/@cpave3/understanding-types-static-vs-dynamic-strong-vs-weak-88a4e1f0ed5f)**

**[Unity Documentation: Managed Memory](https://docs.unity3d.com/Manual/performance-managed-memory.html#:~:text=Automatic%20memory%20management,Mono%20or%20IL2CPP)**

## Questions with ChatGPT

*What are some of the trade-offs between using statically-typed vs. dynamically-typed languages in video game development. Why would you chose one over the other?*

#### The Trade-offs between Static vs. Dynamic Languages in Video Game Development
   1. **Using Satically-Typed Languages(e.g., C++, C#)**
      * Type Saftey: Errors related to data types are caught at compile-time, reducing runtime errors and leading to more stable code.
      * Performance: Statically-typed languages tend to be faster because type information is known at compile-time, allowing compilers to optimize memory usage and execution paths.
      * Use Cases in Game Development: Many AAA games use statically-typed languages like C++ due to the performance benefits. Unity uses C# as its primary scripting language because it offers a balance of safety and performance.

   2. **Using Dynamically-Typed Languages(e.g., Python, JavaScript)**
      * Flexibility: Dynamically-typed languages allow for faster prototyping and more flexible code since types are determined at runtime. This makes them useful for quick iterations or smaller-scale projects.
      * Performance: They typically perform worse than statically-typed languages because type checking is done at runtime, adding overhead.
      * Use Cases in Game Development: Dynamically-typed languages are often used for scripting game logic or developing smaller games, but they may not be suited for high-performance requirements (though Python, for instance, is sometimes used for AI scripting in games).

  As a small summary, the choice between statically-typed and dynamically-typed languages depends on a game's scale, complexity, and performance needs. For high-performance, large-scale games, *statically-typed languages* offer stability and efficiency. For quick iterations, prototyping, or smaller-scale games, *dynamically-typed languages* provide flexibility and faster development cycles.

---
*How do the different programming languages handle memory management in game development?*

##### How is Memory Management Affected?
   1. Manual Memory Management (e.g., C++)
      * In video game development, statically-typed languages (e.g., C++, C#) offer better performance, type safety, and low-level memory control, making them ideal for large, complex games with high performance needs, such as AAA titles. They catch errors early and have robust tooling, but require more development effort. Dynamically-typed languages (e.g., Python, Lua) are faster for prototyping and iteration due to their flexibility and simpler syntax, making them useful for smaller games, scripting, or rapid development where performance is less critical. The choice depends on the game's complexity, performance needs, and development speed priorities.
   2. Automatic Memory Management (e.g., Java, C#, Python)
      * Languages like C#, Java, and Python use garbage collection to automatically manage memory, making development easier by reducing manual memory handling and minimizing memory leaks. However, this can lead to performance issues, particularly during garbage collection cycles, which may cause frame drops or stutters in games. In game development, especially with engines like Unity (which uses C#), developers often use techniques like object pooling to reduce the performance impact of garbage collection in real-time applications.

## Summary

In video game development, statically-typed languages like C++ and C# provide higher performance, type safety, and better tooling support, making them ideal for complex, performance-critical games. These languages allow developers to catch errors at compile-time and optimize memory usage, which is crucial for large games such as AAA titles or those with advanced graphics and physics. However, they require more development time and effort. In contrast, dynamically-typed languages like Python and Lua enable faster prototyping and flexibility, making them better suited for smaller games, quick iterations, and scripting tasks, though they generally lack the performance necessary for large-scale games.

Memory management is another key factor in game development. Statically-typed languages like C++ offer manual memory management, giving developers fine control over memory usage and hardware resources, which is critical for optimizing performance but adds complexity and risk of errors like memory leaks. On the other hand, dynamically-typed languages like C# and Python use automatic memory management, such as garbage collection, simplifying development by reducing the need for manual memory handling. However, this can introduce performance issues, such as stuttering during garbage collection cycles, requiring techniques like object pooling to mitigate these challenges.

---
