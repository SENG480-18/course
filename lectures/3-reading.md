---
Title: SENG480a/CSC485b/CSC578b---Lecture 3
Author: Neil Ernst
Date: Jan 21, 2019
---

# Reading and Understanding Code
One of your most frequent tasks as a programmer is not just *writing* code, which we focus on in university; but also *reading* code. 

Where are some places *reading* code will be important?

Code reviews for your team; [understanding library functions](https://hackernoon.com/im-harvesting-credit-card-numbers-and-passwords-from-your-site-here-s-how-9a8cb347c5b5); copying from StackOverflow; maintaining old legacy systems.


# Context and Preliminaries
The real preliminary of course is that you have a knowledge of basic software concepts, such as loops, methods, memory addresses, pointers, closures, lambdas, even monads or other esoterica. If you aren't trying to learn the language (and reading code is a great way to do that), then you are asking for trouble. For example, what does this mean?

## Examples
```
data {
  int<lower=0> N; 
  int<lower=1,upper=10> project[N];
  vector[N] x;
  vector[N] y;
} 
parameters {
  vector[10] a;
  real beta;
  real<lower=0,upper=100> sigma;
} 
transformed parameters {
  vector[N] y_hat;

  for (i in 1:N)
    y_hat[i] = beta * x[i] + a[project[i]];
}
model {
  y ~ normal(y_hat, sigma);
}"""
```

It helps to know about statistics and probabilistic programming before trying to sort it out (we are simulating a series of linear regressions using [PyStan](https://pystan.readthedocs.io/en/latest/)). 

What about 
```
X[⍋X+.≠' ';]
```

That's <a href="https://en.wikipedia.org/wiki/APL_(programming_language)">APL</a> for sorting a matrix. Apparently.

## Steps
There is no substitute for reading a lot of code. Books like 500 Lines can help, as can blog posts and mailing list posts (e.g., why was [Linus so pissed](http://lkml.iu.edu/hypermail/linux/kernel/1510.3/02866.html) about some pull request?) (Note that there are much better ways to handle this than being abusive to your co-workers.)

- get the source, or as much as you can
- replicate the build environment. Strictly speaking, you want something equivalent to a 'requirements.txt' with fully specified version numbers. If you are lucky, you get a Maven script to start from; if not, you get a 500 line Makefile to figure out. Watch those tabs!
- more likely, you will need to reconstruct the build environment from docs. 
- occasionally this means figuring out from the source which e.g. version of C++ was being used.
- develop a source of tools for code reading:
	+ favourite IDE
	+ grep, sed etc.
	+ reverse engineering tools: Rigi, Intellij, call graph constructors, Understand. In all likelihood you will use several tools in combination.
		* We saw an example of Understand on a Commander Keen game
	+ valgrind or other profilers
	+ git and version control analysis (diffs, blame, etc)
	+ step through with a debugger/print statements
	+ increase the debug level for logging messages

# One Approach
1. build the code executable 
2. run the tests
3. trace the thread of execution
4. note down what seem to be key classes.

> Djikstra: "The purpose of abstraction is not to be vague, but to create a new semantic level in which one can be absolutely precise"

## Find the Entry Point
- key events, main() method, initializations - often tests can be a good document for this.

There isn't always an obvious entry point, e.g. in control systems or other long-lived software (we really don't want to be in nuclear reactor shutdown mode too much!)

## Flowchart
Flowcharts are often seen as relics of the 80s:

[XKCD](https://xkcd.com/518/)

But in reality, they can be very effective at tracing execution flow, or (in a business context), business process logic. The other thing to keep in mind is that you might eventually want to translate your explorations into a communique for others; diagrams and notes can be important artifacts. In some ways you need a 'field book' like any decent archaeologist. Unless you are the relic-stealing, Nazi-fighting variety.

## Grep for keywords
Good keywords: `open, error, save, load` ... plus program specific ones (from the domain model). So perhaps another code reading approach is, figure out the domain model. Chances are a) they are using different words than the ones you might use (Client instead of Customer) or b) there are words you haven't seen before. Acronyms are a great example of this. Figuring out what AWT means (Abstract Windowing Toolkit) will greatly help code comprehension. What if we don't know what "asynchronous I/O" is about?

## View the hierarchy:
Ignore the lower level details, and focus on the method names and signatures, class names, and so on. A good IDE will help with this. In PyCharm, for example, you can pretty quickly navigate around the source. 

## Look at file structure
Someone put files in various folders for some reason. One of the challenges with code reading - and archaeology - is that you have to be careful assigning intent to actions. Think about excavating a Minoan village in Greece. You see some interesting pottery shards that seem to tie this village to Chinese traders (say). But is it really that narrative? Or is it equally likely that what you think is happening is in fact someone who dug a pit in the middle ages, and threw the pottery shards in much later?

## Rewrite the Code
As you move through it, write comments and fix variable names. Assumes existence of unit tests. Why?

# Other strategies?
We discussed some of our past approaches to code reading.

# Program Understanding Strategies
* Bottom Up
* Top Down
* Opportunistic or Knowledge based

These do what you would expect: begin by tracing the code at a low level; begin by looking at package and file organization; or begin by picking an interesting question (where does the credit card get sent?). Researchers have shown that we do all three when it comes to understanding programs.

# How Many People Did the Reading?
We broke into teams to read the code for a piece of the system, and had a group discussion about what we learned.

(then we walked through http://aosabook.org/en/500L/a-web-crawler-with-asyncio-coroutines.html)

Showed how to construct a mental model of what is happening. Go through, look for obvious code that can be ignored, highlight things I need to lookup (IOCP?). External calls to other files - how do these things link together?

If you haven't seen them before, you might notice new CS concepts: generators, closures, callbacks,etc

# References
* http://wiki.c2.com/?TipsForReadingCode
* Working Effectively With Legacy Code, Michael Feathers
* [How Do Program Understanding Tools Affect How Programmers Understand Programs?](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.400.223&rep=rep1&type=pdf) Storey, Wong, Mueller. ICPC 1997.