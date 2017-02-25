###### *[[Hacktivator]] > [Phase 1](https://github.com/hackreactor/peripheral-brain/wiki/Hacktivator#phase-1-review-the-building-blocks) > Review our mental models regarding interviewing*

## Basic recipe

1. Understand the problem.
2. Plan.
3. Outline a skeleton.
4. Implement and test piece-by-piece.
5. Iterate.

We've boiled down [great advice from Palantir and Triplebyte](#more-resources) (highly recommended reading) into this simple recipe. It needs to be simple, because under live interview pressure, it's hard to remember a lot of guidelines. If you always follow the same steps, the basic approach will become muscle memory and you can efficiently focus your limited time and energy on adapting specifically to that problem and that interviewer.

Let's look at these steps in more detail.

### Really understand the problem

Don't just dive into coding!

A misunderstanding early on can screw you over later. So ask at least 1 question. Use specific questions to verify your understanding of what the interviewer is looking for, or what the problem parameters really are. Probe for false assumptions and missing aspects. Draw or write out an example or two.

### Make a plan

Again, don't just dive into full-on coding! Think ahead. 

Decide on your core data structure(s). Decide on the core logic (perhaps it's a full-blown algorithm, perhaps it's just a strategy for organizing business logic) that will manipulate those data structures.

Ask more questions as you go.

### Make a skeleton

You guessed it -- don't just dive into coding a full implementation! Be organized.

Sketch out the flow of execution by stubbing out classes, functions, variables, filled-out data structures. Use comments or pseudo-code if you have to, but even better is to write syntactically correct JavaScript that doesn't need comments because the entities (functions, variables, etc) are so well-named that the flow just describes itself.

### Flesh out the skeleton with small, working pieces

*Now* you can dive into full implementation.

If you want to do full TDD, great. Write your test, make it go "green", and repeat. 

If you don't want to do full TDD, that's fine. But aim for the same end result -- fill in the implementation for one small piece, then immediately write a test to verify that it works. Repeat.

Proceeding this way, you will create crisply-defined Lego blocks that you snap together steadily and reliably into a solution.

DO NOT just write a whole bunch of stuff and then run it or walk through it and realize belatedly that it doesn't work, and slide into debugging hell.

Note that even if you are working on the whiteboard and not actually running the code in an interpreter, this approach still works. Instead of writing an actual unit test, just pause after having written each small piece, and explain briefly what a unit test would check for, then walk through the code yourself ("be the interpreter") and verify that it meets that stated expectation.

### Iterate the solution in the usual ways

After you have gotten to a working, "brute force" solution, you will often be asked to evolve your initial solution. Some typical evolutionary forces that the interviewer applies to the solution are:

* it must run faster
* it must use less memory
* it has to scale across more than one process / machine
* there are now more business rules, complicating the business logic
* it must handle different kinds of clients (e.g., not just command line, let's Web-enable it, or not just Web, let's support native mobile)
* it must be operationalized / production-ready
* it must switch paradigms (e.g., from imperative to recursive)

As you iterate the solution, follow this recipe again, lightly. Don't let it all become a mess in the solution-iteration phase. 

## More resources

These people have summarized things well. Very, very worth reading.

* [Palantir advice, part 1](https://www.palantir.com/2011/09/how-to-ace-an-algorithms-interview/)
* [Palantir advice, part 2](https://www.palantir.com/2011/10/the-coding-interview/)
* [Triplebyte advice](http://blog.triplebyte.com/how-to-pass-a-programming-interview)