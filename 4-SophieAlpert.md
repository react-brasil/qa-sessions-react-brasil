By: @hnordt
In your opinion, what’s the best thing about React? There is anything you would like to change?

```
I don't know if there is a single best thing about React, I think the most important things that React gives are the component model (so that you can have different parts of your code cleanly isolated) and the declarative render methods (so that you don't need to write out separate update logic for how things change), but these days most of the frontend frameworks give both of those. :slightly_smiling_face: I think the most unique things about React are the way that UIs can be treated the same as any other data in your app, and the way that we abstract away platform differences and support other platforms like React Native

there's a lot of stuff that I would like to change but we're working on a lot of it!
```

---

By: @hnordt
How did you learn about React? Did you co-authored it / you’ve been working on it since day 0?

```
I think I first learned about React from seeing the website on Hacker News on the day that it was open sourced, a little over 5 years ago. I'm not an original coauthor (I wasn't working at Facebook at the time) but I started contributing to React more and more over time and eventually I think I was the #1 committer even before I joined Facebook – at that point I figured that I should just go to Facebook to work on it full time, and that's what I did

fun fact: I deployed React to production in one of my projects less than 2 weeks after it was released – in hindsight I think maybe I was a little irresponsible :wink: but it worked out well and I think that makes me the first production user of React outside of FB
```


---

By: @lucianomlima
What are the difficulties in leading a Facebook development team?

```
at facebook we try to hire people who are good at their jobs and also independent, so my job as a manager is pretty easy :joy: I'd say there aren't many difficulties unique to Facebook except sometimes that at a large company there are a lot of different stakeholders and we feel like we have a big responsibility to do things well.
```


---

By: @Isac
What you think about ReasonML? Do you believe it will be the new language for web development?


```
I think Reason is very exciting in many ways (personally I love having a strong static type system and algebraic data types) and I don't think everyone likes JavaScript enough that it will remain dominant on the web forever, but the Reason ecosystem also has a long way to go and I think there are still some syntax quirks to the language that would be important for fix in order for it to appeal to most web developers
```

---

By: @gabriel.metalanguage
What books do you think most contributed to your life?

```
I remember reading a lot of web development books when I was young from the likes of Jeffrey Zeldman and Dan Cederholm explaining some of the ways to build websites with semantic HTML, etc; I think those brought me more immersed into web development originally but they were written before serious JS development on the web was common at all. These days I don't get to read as much as I'd like but when I do I've been dedicating more of my energy towards learning more about social justice and finding ways to make our world better.
```

---

By: @lucianomlima
Could you explain how Pull Requests code review works at Facebook?

```
on the React project, we use github pull request in our open source repo pretty similarly to how anyone else does – the only significant difference from most people's workflows is that we always let the author of a PR merge the commit (when it's someone on the team) so everyone has control over when their own code lands. at Facebook broadly, we have custom in-house code review tools (which began as a fork of Phabricator https://www.phacility.com/) that integrate with all of our internal systems like CI and task tracking; they're not too unusual but one nice feature that GitHub is missing is a way to do "stacked diffs" – posting two commits where one depends on the other but where the commits should be reviewed separately (perhaps even by different people)
```

---

By: @schuchowsky
Recently, Airbnb and Udacity shared their feedback after using React Native. In short, looks like it worked for them at the beginning, but now they are both moving to native IOS/Android development.
The question is: Is RN scaling well in Facebook? What are your thoughts on using RN on a complex project?

```
React Native isn’t the right choice for every project – I do think that the recent posts from Airbnb and Udacity share some insight into React Native’s advantages as well as some current limitations. we'll never get to a place where all apps are built in React Native, but we're constantly improving React Native so that it can work for more people – a few weeks ago I published an update on the React Native blog about the React Native roadmap and many of these planned improvements, so hopefully these improvements will solve many of the limitations these teams encountered!

at Facebook, we're continuing to use RN more than ever, including on FB Marketplace which is entirely RN, which might sound like a small feature but it has 800 million monthly users and about 100 different full-screen views as part of it – larger than almost all standalone apps!
```

---

By: @haz
How is Facebook’s position regarding employees doing personal side projects (open source or not)?

```
there's a review process to make sure that it doesn't conflict with what we're doing at FB (for example, you probably aren't allowed to contribute to a competing social network) but in general it's totally encouraged and I know a lot of people do it!
```

---

By: @haz
How was the process for you to join Facebook and how did you get your position?

```
as I mentioned above, I was very involved in the React project even before I joined Facebook; I think I was the #1 committer to the repo, and I was attending many of the weekly team meetings – so from there, I already knew that I could probably come work here if I wanted to; at some point I decided that that would make sense so I messaged the manager at the time (who's also my current manager!) and told him that I would come interview :slightly_smiling_face:
```

---

By: @sibelius
What is missing in js type systems (TS or Flow)?

```
hmm, that's a good question. I think there are often complex APIs that might be hard to write a type signature for, but oftentimes that is a reason to simplify the API! Flow and TS have different strengths but I think Flow tends to have a stronger inference engine while TS has focused more on practical concerns like editor integration and npm tooling, so I think they can learn a lot from each other too
```

---

By: @brunolemos
Do you have any curious skill or hability that few people know about it?

```
I have perfect pitch, and my fingers are a little bit double-jointed. also I did a lot of math competitions when I was young so I know a lot of random math facts that tend to be useful :sweat_smile:
```

---

By: @andrei_calazans
As a manager/team leader, what’s the secret to keep a healthy environment?

```
I think the most important thing is for the team to trust and respect each other, and to have an environment where it's ok for people to make mistakes and not know things – that's how you grow!
```

---

By: @andrei_calazans
What skill do you think is always lacking in junior developers?

```
I think the biggest thing I wish more people did is try to not be afraid of other parts of code, even if your team didn't write it or if it's a third-party package – many people stop debugging once they reach the end of "their code" but often you can learn a lot and fix problems if you are comfortable looking one level deeper
```

---

By: @brunodahora
Will the new React features, like Async Rendering, be arriving to React-Native anytime soon? How is the status of it and how is this being treated inside the team?

```
yes! the architecture changes I mentioned in this post https://facebook.github.io/react-native/blog/2018/06/14/state-of-react-native-2018 are designed to integrate really well with async rendering so hopefully we will release them broadly for web and RN around the same time. we're currently doing our first production tests of async rendering so hopefully we'll see some good results soon :slightly_smiling_face:
```

---

By: @brunodahora
What is the trend inside the React team? What we, as React developers, should be looking at?

```
many of you have already seen this talk, but Dan Abramov's talk at JSConf Iceland in March talks about the future things we're thinking about right now: https://reactjs.org/blog/2018/03/01/sneak-peek-beyond-react-16.html (edited)

as React users, I think you can try to stay up to date with all of the new things but it's also not necessary so I wouldn't stress about trying to keep up with every single thing; the ideas that are really good will be here for a long time and you can always learn them later
```

---

By: @sibelius
How does engineering teams in FB interact with other (like react team, react native team, flow team, relay team)?

```
we sit very close to the other teams we work the most with, so it's easy to collaborate (and we also try to do fun activities together, like yesterday we had an offsite where we played "archery tag") but basically we try to develop our larger roadmaps together so that we can make sure we are building towards the same thing, and then we can always collaborate on smaller things when something comes up
```

---

By: @sibelius
What is missing in Relay/Apollo?

```
I haven't used them a lot myself, but I know that one big thing that stops people from using them is not having a graphql server, so I think it would be cool if there was some easy way to map graphql queries to normal API requests so that you can start using those libraries without a graphql server at all
```

---

By: @jcm
Does facebook uses chatbots? How automated is your normal workflow?

```
we don't use that many chatbots for work (partly for security reasons) but we have a lot of internal tools (probably hundreds) that are custom-built for our use cases that make us more productive. I think it's cool to work somewhere that is large enough to do this and somewhere that cares about making employees more productive. at some level, React is even an example of this: we built it as a tool to make ourselves faster at building high-quality UIs!
```

---

By: @sibelius
What IDE do you use? what is the missing feature of most IDEs today?

```
I used vim and macvim for a long time but got frustrated at configuring the file fuzzy finders (ctrlp, command-t, etc) to work well; recently I have been using vscode in vim mode although I get frustrated with it because some of the keyboard shortcuts are slightly different than vim and it confuses my muscle memory
```

---

By: @sibelius
What is missing in current open source bundlers (webpack, parcel, metro bundler)?

```
high performance and reliability are the biggest things I want in a bundler :slightly_smiling_face: I haven't recently felt frustrated at anything missing but I'm sure lots of other people have ideas for improvements that could be made
```

---

Thank you so much for your time @Sophie Alpert it was AMAZING, i’m pretty sure all Brazilian devs really loved it.

We have one last question:

By: @allBrazilianDevelopers <3(@Nic)
Any chance of you coming to Brazil for React Conf in October/2018?

```
unfortunately I don't think I will make it this year but maybe sometime in the future!
thank you for having me today, it's great to see everyone!
```

