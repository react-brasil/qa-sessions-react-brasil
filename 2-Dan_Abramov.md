Vinicius Rangel
Dan, there are bigger plans to redux this year?

Dan
Not sure what you mean :slightly_smiling_face: But I have no plans regarding Redux personally. I'm not actively involved with maintaining it.

-------------------

thiago.leite
Andrew Clark said on his Twitter that class components will be considered as legacy APIs in the future, while function components will remain. We must take this statement in consideration in the projects that are under development/will be developed? And what is the best way to write a component?

Dan
He also said on Twitter that we have dozens of thousands of class components and they aren't going anywhere :slightly_smiling_face: When/if we have a more convenient and less verbose way to declare components than classes, we'll definitely announce it, but I don't see how it could affect existing projects.

-------------------

pvieira91
1) Tests | We went from 0 to 100 in what regards unit testing. It’s pretty common nowadays to find companies that have very high thresholds on unit testings. Do you think that it’s valuable to impose a high unit test coverage even for presentational components?

2) Styling | What is your opinion of css-in-js? Do you prefer it over standard stylesheets (scss, css-modules, post-css etc) or it’s more interesting to use a css-in-js lib? If so, which one? (styled-components)?

Dan
>1)
Personally I don't find unit testing components very valuable. Especially if they just contain markup — you're basically testing that React works, and we have tests in React itself for that. I think some combination of integration tests for higher-level UI scenarios (click a button, something shows up) and unit tests for _logic_ (e.g. complex calculations) is helpful. I'm more skeptical of asserting on component output although I understand others might not agree.

>2)
I don't care about this much. If I were writing something today for myself I'd probably use vanilla CSS. Maybe glamor if there were a lot of dynamic styles.

-------------------

sibelius
> how will async react help in handling requests waterfall?
> how will async react improve react native?
> what is take on flow/typescript and reason?
> what next after relay modern?


Dan
>how will async react help in handling requests waterfall?
Not sure what exactly is being asked. But my guess is this is about the case where you have a parent and child component that each request some data, but it could've been requested in parallel.
With “suspense” APIs (part of async React), we think it’s much simpler to “move” async dependencies up and down the tree without re-wiring the props or changing the app architecture. This is because all components are backed by the same cache. So I think async React would help avoid waterfalls by making it easier to optimistically _preload_ resources that you think components below will need. Similar to `<link rel="preload">` in HTML.

>how will async react improve react native?
There's work in progress on revamping React Native architecture to better take advantage of async rendering and solving some existing pain points regarding interop with sync code. I’m not the best person to talk about that though.

>what is take on flow/typescript and reason?
I’m personally comfortable with JS + some sprinkles of Flow where I’m not confident what’s going on with types. Not a fan of having to annotate everything. I haven’t tried Reason yet so I don’t know if I’ll like it.

>what next after relay modern?
I don’t know, is there something missing in it? My understanding is that the Relay team is happy with performance wins from Modern. We might need to change the React bindings to it to better take advantage of the upcoming React async features, but I don’t know more.

-------------------

gabrielrubens
We all know that unit testing is important, but it’s hard to make sure that all cases are being covered in a test suite
Is there any technique you guys use to make sure all test cases/possibilities are being covered besides only trusting in human review?

Dan
If this is about components, I’ll reiterate we don’t do that much unit testing of components at Facebook.
If this is about React itself, we’re using fuzzy testing in some cases where there are too many possibilities. A fuzz test is like a test that generates some inputs randomly many times, and then asserts some conditions that we expect to always be true. If there’s a regression, we add it to a list of inputs that must always be tested. So that helps refine a fuzz test over time.

-------------------

Marco Nicolodi
How do you balance fast delivery with code quality?

Dan
We sacrifice either one or the other depending on what’s more important? :slightly_smiling_face:

-------------------

haz
How did you start working on Facebook? Was invited? How was the process?

Dan
I’ve chatted to recruiters a long time ago but they didn’t have any UK positions at the time, and I couldn’t get a US visa (and didn’t want one that much anyway). After about a year I bumped into Jing Chen at React Europe (I think she was on the Relay team at the time, although I’m not sure). She asked if I was interested in interviewing, and mentioned the London office. I said that I am, so she arranged for other speakers to interview me on the next day (so I skipped most of the conference), but it was a regular FB interview process (several interviews).

-------------------

sibelius
> what do you think about recompose?

Dan
Too much indirection.

-------------------

r.santos
If someone is starting Studying React today do you think it still a good idea study redux as well?

Dan
I always suggested learning React first before you look at Redux.
After you've learned React, I think learning Redux makes sense even if you don't plan to use it. 90% of "learning Redux" isn't about Redux itself. It's about learning to use functional composition and immutability. That would come in handy regardless of whether you plan to use Redux APIs or rediscover the same patterns yourself when you use context API or something similar.

-------------------

jpbretanha
Should we start moving from using HoC’s and start to use render props?

Dan
I don't know, what looks clearer to you?

-------------------

sibelius
> is React going to add a compilation step soon?

Dan
There is already a JSX compilation step but you're probably referring to whole program optimization. There are some experiments we're working on but I wouldn't say there're anywhere near "soon".

-------------------

sibelius
> how does Facebook handles flow-typed internally?

Dan
I don't know.

-------------------

weslopes
What about the microservices in front-end with react? It’s a good idea?

Dan
I don't know anything about microservices.

-------------------

sibelius
> will Facebook switch to fullstack Javascript? are you guys using nodejs in backend?

Dan
No, FB uses a highly optimized runtime and language (HHVM, Hack) and there are no plans to swap it with Node.

-------------------

jcm
> what do you think of function as child components ?

Dan
They're cool when the API is clear?

-------------------

Marco Nicolodi
What are the most important things to check during code reviews?

Dan
Semicolons.

Okay, I'm kidding.

If you don't have any type checker, I think it's most important to look out for potential crashes (`null` / `undefined`) as those are painful to diagnose and fix. Other than that, I don't know—depends on the kind of mistakes you usually notice and want to reduce?

-------------------

lucasbento
How do you feel about ReasonML?

Dan
Copy pasting from above:
I haven’t tried Reason yet so I don’t know if I’ll like it.

-------------------

Lucas Sartori
Hello Dan, I’m a great fan, really appreciate you taking your time to answer some questions here!
So, I’m a junior developer that has been working with React and Javascript in general for less than a year. I’d like to ask you about your first steps into the programming world, what motivated you the most to keep going before you had any palpable success and what would you recommend a junior developer in dedicating himself in 2018?

Dan
I started with Visual Basic so that's kind of a long time ago. Throwing things on a form and seeing it "come alive" when I press "run" was pretty magical. I don't think there was anything else that motivated really, I just liked making things.
I recommend building lots of small things

-------------------

rudiney
Not much a tech question but, how is the mood inside Facebook about this Cambridge Analytica data breach scandal? Can we expect big changes on the FB developers polices or any chance the open source tools licenses being reveiewed?

Dan
The APIs that allowed this "breach" were closed down four years ago. I think at the time the policy was really naïve but there were also a lot of people who argued data should be "more open" and FB is evil for "locking it down". So it's interesting how the perspective changes over a few years.
I think it's clear to everybody at the company now that the old vision was too idealistic, but even though they closed it down four years ago, the old mistakes keep chasing them :slightly_smiling_face: . I know there's a lot of people working hard on fixing problems like fake news, election integrity, abuse etc, so I think the company will survive through this and become wiser.
I don't see how this relates to open source tools. Regarding developer APIs, yes, there's been some further lockdown on data apps could get, you can read about those changes at https://newsroom.fb.com.

-------------------

guilhermepontes
What is your typical day like?

Dan
Woke up, fell out of bed
Dragged a comb across my head
Found my way downstairs and drank a cup
And looking up I noticed I was late
Found my coat and grabbed my hat
Made the bus in seconds flat
Made my way upstairs and had a smoke
And everybody spoke and I went into a dream

-------------------

lucasbento
How’s the environment in Facebook HQ? How does it compare to a startup (in terms of bureaucracy, speed, etc)?

Dan
I don't really see any bureaucracy at all except cases where something has legal implications. Individual people and teams have a lot of agency.

-------------------

r.santos
Do you think that the new versions of React - 16.3.0 and beyond - are going in a direction that will improve state management power to the point where Redux might become useless?

Dan
I think I sort of answered that. The point of Redux isn't "Redux-the-library", it's the pattern of separating update logic from descriptions of "what happened". Whether you use Redux-the-library or not, this pattern might be handy for some cases. I wrote an article a long time ago that both describes these cases and describes "Redux without Redux" at the end: https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367
I will also quote my earlier reply:

>90% of "learning Redux" isn't about Redux itself. It's about learning to use functional composition and immutability. That would come in handy regardless of whether you plan to use Redux APIs or rediscover the same patterns yourself when you use context API or something similar.

-------------------

tiagosouto
what’s your opinion about RxJS?

Dan
I think it's cool for handling complex data flows. Not as much a fan of using it for UI composition.

-------------------

lucasbento
Right now you are working with open-source on your full-time job but how did you manage to work and maintain your personal projects on your free-time? Did you have a limit on how long time you would spend on it?

Dan
I didn't work on personal projects that I also wouldn't be using at my main job.

-------------------

sibelius
> How Facebook structure their frontend code? there is a bunch of microapps? if so how to you make them communicate each other?

Dan
No, it's a single monorepo. Any file can import any other file. (edited)

-------------------

@fdaciuk
Hi Dan! Are you using SSR with HHVM? If yes, which tools are you using for? (edited)

Dan
Not sure what you mean but we don't currently server-render React components. On the server, we use XHP for server rendering (which is not related to React).

-------------------

sibelius
is there any machine learning algorithms to improve frontend code? I heard code splitting is done like that, any other places to apply ML in fronted?

Dan
I don't know, but yea, we use it for code splitting.

-------------------

andrei_calazans
Do you think Mobx has grown to become a better state handler than Redux? whats your opinion on that?

Dan
Personally I’m not a fan of mutation. :slightly_smiling_face: It’s cool if it solves your problems but it makes some other things that are important to me harder.

-------------------

Diego Nascimento
What do you think about other forms of DOM manipulation, such as incremental-dom or glimmer?

Dan
I think the work glimmer is doing with AOT compilation is interesting. I don't know much about `incremental-dom` but I don't think DOM is the best fundamental abstraction to build a component system on. (That's my personal opinion)

-------------------

dnvtrn
What is the best solution to work with SSR and Create React App, avoiding the known problem about Google SEO web crawlers?

Dan
I don't know. You tell me. :slightly_smiling_face:

-------------------

sibelius
how async react will improve animations frameworks?

Dan
I don't think async React itself is going to help animation libraries. Although it should help block the thread less which should reduce jankiness of the animations when there are other updates happening.

-------------------

sibelius
> which other technical fields would you like to work? robots?

Dan
I don't think I have a lot of interest in other technical fields

-------------------

brunolemos
What is that you think may be big in a few years that only a few people is paying attention right now?

Dan
I'm hoping some ideas from async React will become more commonplace in other view libraries

-------------------

brunolemos
Thoughts on Flutter?

Dan
Separating state logic into reusable pieces seems nice. We're thinking about this.

-------------------

Aldo Jr.
Dan, what do you think about PWA?

Dan
I think the premise is good but service workers need better UX

-------------------

fdaciuk
When did you start learning functional programming? Could you recommend any language to get start with?

Dan
I think I started with an esoteric language nobody uses (http://nemerle.org/). Doesn't really matter, JS is fine

-------------------

leolopes
In the scope of react-native, what do you consider the must-have skills to be considered a good react-native programmer?

Dan
I don't know, make apps that look and behave well?

-------------------

guilherme_vasconcelos
What are the topics you suggest developers - involved with React and its ecosystem - to focus on studying in order to be prepared for the future or next years?

Dan
Immutability


sibelius
> which books changed your life?

Dan
https://www.amazon.com/Beginning-Infinity-Explanations-Transform-World/dp/0143121359


Jabur
Hey @Dan thank you so much for your time, i`m pretty sure everybody really loved your answers.

I only have one more question and one invite:

1 - Can you point to three other people to the next Q/A Session!

2 - And: Any chances to come to React Conf Brazil? :flag-br:

Dan
Re (2): not very likely because I don't do many talks so I don't even know when the next one is going to be
Re (1): in React ecosystem?
my teammate

https://mobile.twitter.com/ProvablyFlarnie

my manager

https://mobile.twitter.com/sophiebits

cool folks I've learned from

https://mobile.twitter.com/NikkitaFTW
https://mobile.twitter.com/rwieruch
https://mobile.twitter.com/siddharthkp
https://mobile.twitter.com/peggyrayzis
https://mobile.twitter.com/CompuIves
https://mobile.twitter.com/elibelly
