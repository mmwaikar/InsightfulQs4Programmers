# Niche Languages

The two niche languages which I absolutely love are Clojure & F#. These are on the opposite ends of a spectrum - one fully dynamic and the other fully type-safe (with possibly, one of the best type inference engines out there). If you forget this fact for a few minutes, then you'll realize that both share a lot of good principles:

- value equality
- immutable data structures
- REPL support, etc.

## So what's the problem?

The problem is that there are few companies using these languages in production, for different reasons.

Clojure is happy being a niche language and although there is a company behind it - Cognitect (which was acquired by [Nubank](https://en.wikipedia.org/wiki/Nubank)), it never got into the mainstream. A few reasons why Clojure didn't take off:

- people don't want to use a dynamic language (though they'll happily use JS for the front-end, because that's the default)
- some people don't like the Lisp syntax

In contrast, although Microsoft is behind F#, it cares little for F#'s success and is happy catering to it's main customer base, which are happily using C#. A few reasons why F# didn't take off:

- people don't want to invest time in learning a new language
- even if you'll be able to use it in many areas, you'll still have to fall back to C# for tasks like UIs, and maybe database access (in case you want to use ORMs), because of which people talk about OO-FP-OO (front-end - core business logic - data layer) sandwich

So the problem for an *average developer* is that there are few opportunities for them to get a job in any of these (or similar, niche) languages. Only the top few will get to use these languages as a part of their daily job, and the majority others will be regretting the fact that they are not able to land a job in these (much better than their famous counterparts) languages.

## So what's the solution?

Well, obviously, you'll have to place your bets on the language, which you think is very likely to become mainstream. And you know it's not an easy task to predict this. Scala was in this position, a few years ago, but it spectacularly blew away that opportunity. Kotlin is another such candidate, because already it has become the first language for Android development. Rust is also an excellent contender for breaking into the mainstream languages.

# Conclusion

Try to adopt a language which you can use for the broadest variety of tasks - starting from front-ends, server side (REST APIs, databases), scripting, infrastructure and what not. **No more of right tool for the right job BS.**

***Why can't there be a single, capable language for all these tasks in 2025?***
