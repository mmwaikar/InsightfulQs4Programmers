# Rust

My journey with Rust is a typical hate (more of frustration, frankly) to acceptance & finally admiration story. I came to Rust after using Scala in production for almost 4 years and learning F# on my own. I've used GC languages (C#, F#, Java, Scala, Clojure) for my entire programming life and that's where the frustration with Rust stems from. Imagine the horror of seeing the `address of` operator (`&str`) after many years of conveniently forgetting to do anything with it 😉

## The pain points

- Ownership, moves & borrowing, oh my, and this is what will frustrate you at first and will take a long time to master
- Type inference which is not as capable as that of F#
    - Let's face it - F# or OCaml have the best type inference engines out there (you don't need to specify the types of function parameters or the return type). Even Scala is able to figure out the return type of the function based on the type of the last expression, so if you don't specify the return type, the compiler assumes the correct one. Not so with Rust - if you don't specify the return type, then the compiler assumes it to be a void 😞

## Things to love

- A language which may feel like a *niche* one for now, but has the **most chances of becoming mainstream** (with companies like Google, Microsoft, Amazon and many others using it for critical pieces of their software). I believe, it's good to have the [Rust Foundation](https://rustfoundation.org/) & [10 Years of Stable Rust: An Infrastructure Story](https://rustfoundation.org/media/10-years-of-stable-rust-an-infrastructure-story/) is an absolute must-read
- Tooling which works out of the box - `cargo` is just seamless
- No classes (OOP)
- Strong FP support (modules, Option, Result etc.)
- [WASM](https://www.rust-lang.org/what/wasm) support
- ...

## The absolute deal clincher / scale tilter

I haven't written UIs in a long time now - I enjoyed writing UIs in VB6 and then C# WinForms (imagine, these frameworks had pretty good tree-view / data-grid controls back then), before WPF / Silverlight sucked the joy out of it. I also liked AngularJS (the very first version) but then React happened, I got involved in the backend and there was a slow mayhem in the JS land.

So finally, after many years, I am having fun writing UIs in Rust 😍 and the primary enablers so far have been [Sycamore](https://sycamore.dev/), [Leptos](https://leptos.dev/) and [Dioxus](https://dioxuslabs.com/). I haven't had much success with [Relm4](https://relm4.org/) (so far) but that also looks like a nice framework (inspired by Elm and based on [gtk4-rs](https://gtk-rs.org/)). [Slint](https://slint.dev/) is another cool option.

# Conclusion

Companies so far, who have already adopted Rust, must have done so for the backend. Backend services, critical infrastructure, performance critical software and what not is already a solved puzzle for Rust. For companies, who are using TypeScript for the front-end, or any JS framework, Rust is becoming a viable option or will soon become one, once these frameworks have a stable release. And if you have Rust for one part of your stack, then who's stopping you from using it for the remaining part? 😝
