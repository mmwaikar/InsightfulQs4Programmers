# Scala

**Scala is an enigma** - it has so many *good* and *bad* things at the same time. I knew and liked Clojure before I had to use Scala at work, and all I had heard about Scala was that it is a big, complicated language with a lot of concepts so I was reluctant to learn it, but I was wrong. I also thought that I knew FP (Functional Programming) but I couldn't have been more wrong.

## The good parts

The thing is that typed FP has so many concepts which are not present in dynamic FP languages like Clojure (or Lisp). You'll only know or learn about Monads, Applicatives or Effects if you use a typed FP language. So the saying that *Scala is poor man's Haskell* or that *Scala drags you half-way to Haskell* is absolutely true. Chances are very low that you'll get to use Haskell at work but are much higher that you may get to use Scala at work (like I did). The very fact that Scala is a *language on the JVM*, gives it the **reach** that makes it a practical language.

Scala has a surprising number of excellent libraries if one has to practice **pure FP**. Some of these are:

- [Cats](https://typelevel.org/cats/) - a library which provides abstractions for FP
- [fs2](https://fs2.io/#/) - Functional, effectful, concurrent streams for Scala
- [http4s](https://http4s.org/) - Typeful, functional, streaming HTTP for Scala
- [Cats Effect](https://typelevel.org/cats-effect/), [ZIO](https://zio.dev/), [Eff](https://atnos-org.github.io/eff/) - Effect libraries

> ⚠️ The only downside of going with pure FP is that **it's hard** and takes time to master, and on top of that, your entire team has to be well versed with all these pure FP concepts, so it's a long, uphill battle before you could be productive. One highly recommended resource for flattening the learning curve are various [Rock The JVM](https://rockthejvm.com/) courses for learning advanced FP concepts.

> ℹ️ F# creator Don Syme explicitly didn't want this advanced FP or Category Theory concepts in F# and feels that it should be possible for common programmers to be productive with an FP language without having to deal with these difficult concepts.

> ℹ️ [OCaml](https://ocaml.org/) now officially has an effects framework called [eio](https://github.com/ocaml-multicore/eio).

## The bad parts

*So what's the problem?* Well, here comes the **enigma** part - the one big mistake that Scala did, elevates it to being a **case-study** - *the sin of breaking backward compatibility*. **Not just once, but multiple times:** 

- Scala 2.18 code did not used to compile for 2.19 (if I remember correctly, the version numbers might be a little off though)
- What to say of Scala 2 vs. 3? (Same as Python 2 vs. 3 for those who don't know)

You won't appreciate C# or Java **never** breaking backward compatibility, until you have to deal with it yourself. When the realization dawned on me that I'll have to invest time to *again learn a new syntax* for Scala 3, I was really pissed off, and disgusted. I mean, for no fault of mine, and for no **substantial** gains, I have to invest time and energy again, and *imagine it for a team now*. **The greater the team, the greater the loss in productivity and resources.**

Some other deal breakers:

- Lack of async/await
     - Let me be very frank - if a languages does not have async/await support than anytime you have to deal with asynchronous functions (which is in a lot of places), and specially when you to combine a lot of those functions in a business logic, your code is bound to get very complex, and you'll spend **exponentially more time** than if you were to use those very same functions and weave them together in a business logic if they were totally synchronous. It is not for nothing than languages apart from F# & C#, like Dart, Python, JS, Rust - all have async/await - **a game changer for which F# and Microsoft get very little credit**)
- **Akka** the open-source poster child of Scala, was turned into a for-profit version
- [Lagom](https://www.lagomframework.com/) which was the only micro-services framework, was abandoned
- Similarly, [Play](https://www.playframework.com/) was also left to open-source maintainers (which is not bad per-se)
- Lack of full-stack support
    - Sure, there is [Scala.js](https://www.scala-js.org/) but sadly it did not take off and at least, my first experience of using any JS library in Scala.js was not friendly (and time consuming). **This point needs a little elaboration** - *you may say that it is a wrong yardstick to measure a so-called backend language*, but again, *there are some things that experience teaches you and if you want to learn from my experience / mistake* 😉, it is this - **pick a language that lets you write all kinds of applications** (user interfaces - platform specific / independent / browser-based, backend, APIs, scripts, AI / ML and what not). If you are thinking are there any such languages, then the answer is a **big YES** - [Rust](./Rust.md), Kotlin and C# (to name a few)

## The situation today

Companies that are still using Scala:

1. are either using Akka (because of their prior commitment or whatever reason)
2. or, have migrated their Akka code-bases to [Pekko](https://pekko.apache.org/) the open source port of Akka
3. or, are using libraries from the pure FP camp (mentioned above)

**So in hindsight**, the companies (or individuals / teams) who were in the pure FP camp, were probably the ones who experienced the least amount of churn. I feel really sorry for everyone else who is not a part of (these 2) the Akka / Pekko or pure FP camps.

# Conclusion

If you plan to adopt Scala (in 2025), please do so only if you can adopt the pure FP ecosystem, which I've already mentioned, will take substantial time & effort, but can be highly rewarding at the same time.
