# Object Orientation vs. Functional Programming

OO felt right when I first learnt it. And I was happily using it through C# for almost 9+ years. Then I came across [Clojure](https://clojure.org/) and it felt like someone has slapped me hard 😃. In a project just prior to learning Clojure, our whole team had spent countless hours in implementing `ToString` (so that the contents could be displayed properly for debugging) and `Equals` (so that the objects could be compared for equality based on value). And Clojure teaches `value equality` (also called `structural equality`) in the very beginning.

So, in short, here are the concepts which OO languages got it **wrong**:

1. **No Interactive Environment or the REPL** - though there are some open source ones for C#, like [DotNet REPL](https://github.com/jonsequitur/dotnet-repl), and [JShell - the Java Shell](https://openjdk.org/jeps/222) introduced in Java 9
2. **Reference Equality as the default** - apart from use in ORMs (Object-Relational Mappers), there are not many practical scenarios where Reference Equality is needed
3. **Mutable values or data structures** - by default, class properties are mutable or in-built data structures, e.g. the ones in `System.Collections.Generic` namespace for C#, are all mutable. In contrast, Clojure has only immutable data-structures or even most of the F# collections are immutable
