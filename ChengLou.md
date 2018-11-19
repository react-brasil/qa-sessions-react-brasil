By: @AndreiCalazans
Do you think reasonML has potential to be more than just a compiled to JavaScript language? Can it become itself a language compiled directly to machine code or any other low level language?

```
We already compile to machine code! :smiley: That's how Reason started. But since compiling to JS gets us a bigger crowd, here we are. I won't get into details, but if you look at e.g. https://github.com/bsansouci/bucklescript, you can basically make your pure Reason project to compile to assembly without many changes
GitHub
bsansouci/bucklescript
A backend for the OCaml compiler which emits JavaScript. - bsansouci/bucklescript
```

By: @grsabreu
Why should JS devs get into ReasonML if we have relatively easier options like TypeScript and Flow? What points Reason can offer that neither TS and Flow can't?

```
Until you try a "sound" type system, you wouldn't realize that most other type systems fall into an uncanny valley of static typing. By "sound", we usually mean "it'll be 100% correct", _not_ a heuristics, but a guarantee. This is subtle, but drastically changes how you think and use the types. If you hover over a type in Reason and it says "number", it'll _definitely_ be a number, not "maybe a number, maybe undefined, etc". That's one thing. The other thing is, we've got one of the fastest build pipeline in the world. One of our codebases has 1k files and it compiles in under 2s, fresh build. Type inference is still immediate. No such thing as save -> wait minutes -> check for errors
```

By: @sibelius
Your talk "Spectrum of Abstraction" opened my mind about all the trade offs libraries/packages and frameworks have to decide when choosing an abstraction.
What powerful abstractions have you seen that changed your mind? (edited)

```
Some of the recent improvements in machine learning really made me stop and wonder what I'm doing as engineer, lol. On top of my mind, there's also https://www.youtube.com/watch?v=xnez6tloNSQ recently and https://www.youtube.com/watch?v=iWa4t9oa5zw&feature=youtu.be&t=1972. And as always, I recommend you to check everything by http://worrydream.com (edited)
```

By: @Rafael Ramblas
Why the functional approach to React? How this idea came to be and why OCaml was chosen to be the code base for the first Proof of Concept?

```
It was SML at first, then OCaml. OCaml's type system had a few extra things Jordan was looking for. He chose SML because it was a faster language for him to prototype in. Honestly, once you dig to the end of it, you realize React isn't _that_ functional or that OOP. It's somewhere in-between, and that's fine. I think we should start with "does this help me build my product better" rather than the sometime wrong proxy metric of "is this the most functional-oriented thing I can use".
```

By: @guilhermedecampo
What was the hardest problem you had to deal with lately?

```
That hits close to home... not one problem but a few dozen. I worry about the future of computing, etc. But more on that another time I guess
```

By: @PlayMa256
Why OCaml was only known and used in the academic environment?
Are there any particular reasons for it to not had became a "mainstream" language?

```
Well, every language starts obscure, right? Arguably OCaml is taking longer than most. Simply speaking, the timing wasn't right until recently. There wasn't even a package management story until a few years ago, etc. And front-end folks were unfamiliar with types back then too. And then no such thing as BuckleScript existed. It took a while for the window of opportunities to align
```

By: @andrei_calazans
As for mid-2018 is it safe to start a to production project with ReasonML, will my company still face some difficulties with its adoption? (edited)

```
The learning curve's still there; but if you've got a Reason person who knows the in and out of things, there's not much that's not achievable. BuckleScript's interop system is featureful, to say the least, so you usually know that you can bind to everything you need. Definitely do the JS track; the native track is still experimental (edited)
```

By: @grsabreu
Are there any plans to provide an official Relay-like GraphQL client for Reason as an approach to get more people using it?

```
not currently, as messenger doesn't use Relay. If you're getting started with Reason, I highly recommend not trying all the pieces at the same time. You'll dissuade your coworkers and lose your chance of convincing them lol

By the way, follow the spectrum of abstraction! Start with the most concrete thing you can propose to coworkers, e.g. "I can write this particular piece of our product better". Don't start with the most abstract "lemme tell you all about the functional paradigm". Everyone who starts with the latter has failed so far. Think about why, in terms of abstractions vs concretization. It's just a bad way of selling your pitch to start at the most abstract proposition...

The most successful Reason conversions we've had are during Reason meetups where we gathered folks together to make e.g. a game or a small app. The moment you start preaching some monadic whatever, you've lost the interest of most newcomers/coworkers. (edited)
```


By: @Raphael Thomazella
How essential is math for a person to work at the industry nowadays? E.g. Can I get by with poor math skills?

```
Front-end dev basically requires no math at this point, which isn't a bad thing, since people of all walks of life can create now. But if you're doing this professionally, I do recommend you to at least look into the proper computer science stuff, e.g. classic data structures & runtime analysis. Again, think of the spectrum of abstractions: do you need math/CS right now to ship your web app? Likely not. Do you need it to jump into a related software domain you couldn't have otherwise? Probably.

There are definitely some more CS/Math-y domains such as crypto, machine learning, and anything low-level. I'd say don't be uncomfortable not knowing the theory, but make sure you do learn some so that you don't get stuck writing the same webapp in ten years.

Here's my recommendation to get started (I know this works because that's how I got started): read about some simple but non-trivial data structures like binary tree, and implement one yourself. Then do it for hash map, heap, trie. One day when folks are talking about things one abstraction level lower than what you're programming in, you'll suddenly start to realize things and connect concepts. It's an exciting feeling.

You're literally "powerful" once you learn proper CS. Folks usually counter that with the argument "yeah but it's not needed for what I'm doing right now", which is really talking beside the point if you think about it regarding abstraction spectrum. I think "it's not needed for what I'm doing" is actually a _great_ stance, as it prevents over-engineering, which is pretty much the root of all evil (the Reason community tries really hard not to reach for overly powerful and un-useful patterns like monads and other type-level tricks). But it has to be a learned, carefully understood stance, not an argument to defend your temporary ignorance. (edited)
```


By: @haz
What's the thing you like the most about working at Facebook?

```
You're the average of your coworkers, so it's nice to be around smart, passionate coworkers. Being around great folks is probably the best thing you can do for your career, so definitely do seek these folks out. You have internet, so you can reach out to a big pool of folks whenever you want now. Use it
```


By: @Raphael Thomazella
How was the process of making a programming language?

```
I wouldn't know, since we started with taking an existing one and tweak the edges as we saw fit. I'm very close to folks who created languages though; if it's to get work done, then forget about it right now, because you won't get any useful work done by starting with creating your own language lol. It's akin to "let's create a game engine before starting our game!". You never come back writing your product.
If it's just for fun: you'd still start with a concrete goal, but a goal that's concrete relative to creating said language, e.g. "I wanna see if I can implement a few type system feature" or "I wonder if I can make these optimizations or explore these new paradigms". Honestly, I'm always tracking new interesting languages, but it's not my main interest. My main interest is getting the job done :smiley:
```


By: @haz
How did you learn English and French? Do you have another language you would like to learn?

```
I'm Chinese and immigrated to Montreal, Canada. Montreal's official language is French. Every Chinese friend I have there are at least trilingual; it definitely sounds impressive to some folks!
My school also taught Latin, and I learned a bit of Spanish by myself. But use or it lose it. And I lost these two.
```


By: @sibelius
Will Reason have support to generators, async await, async generators and other async sugars syntaxes?

```
Generators will be hard; not thinking about it atm. Async/await, likely. This topic has been delayed for a long time now, because we just still don't think Promises is the way to go for us (perf, semantics, bike shedding, flexibility). We're thinking about it mostly for the interop purposes.
```

gabriel.metalanguage [3:51 PM]
Last question, would you consider coming to React Brasil Conf in 2019? All Brazilian React devs would love to see you giving a talk

Cheng Lou [3:51 PM]
I haven't decided yet, but thanks for the invitation! :smiley:
