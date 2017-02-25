###### *[[Hacktivator]] > [Phase 1](https://github.com/hackreactor/peripheral-brain/wiki/Hacktivator#phase-1-review-the-building-blocks) > Review our mental models regarding interviewing*

How do you evaluate whether you did a good job in the interview? Answer these questions for yourself or a peer.

## Live interview checklist
1. [Yes/No] Did the candidate think ahead and make a reasonable plan of attack?
1. [Yes/No] Did the candidate clearly communicate all their technical ideas, starting with their plan?
1. [Yes/No] Did the candidate execute their plan step-by-step, in a disciplined and well-organized way?
1. [Yes/No] Did the candidate unblock themselves fluidly as parts of their plan hit roadblocks?
1. [Yes/No] Did the candidate get to a working solution by the deadline?
1. [Yes/No] Did the candidate improve and evolve the initial solution (if applicable)?
1. **[Yes/No] Overall: Is this candidate a Strong Yes for hire?**

* If not a Strong Yes, please be clear and specific about why not.
* No hedging. Anything less than enthusiastic Yes! translates automatically to a No.


## Exploring the assessment checklist items

### You think ahead
* You probe assumptions.
* You envision future state.
* You predict possible pitfalls.
* You come up with more than one reasonable/justifiable option.
* At the same time, you don’t over-think (analysis paralysis). You stay pragmatic.

### You're an excellent technical communicator
* You translate well from plain-English problem description to “computerese”
* You correctly use the usual dev-related buzzwords to concisely convey design and implementation ideas
* You draw succinct diagrams and tables (as needed) to convey design ideas

### You pattern-match against solid mental models
* You know what all the dev-related buzzwords that were introduced in the Instructional phase of Hack Reactor actually mean.
* You can use those buzzwords to succinctly explain things like:
	* how the Web works.
	* why you would or wouldn’t choose to use Node.js
	* how React, Angular, and Backbone are same or different, and why you might choose one or the other.
	* how to construct a professional-quality web app.
	* how to make a web app production-ready, and scale it as traffic increases.
	* etc (not a comprehensive list, just illustrating)

### You can unblock yourself
* You can come up with options, evaluate them quickly, and keep moving.
* You never spend more than a brief time in completely stuck mode without [trying something useful](How to unblock yourself).
* Ideally, no need to open-ended debug at all. Tests might fail but they immediately point to the problem.
* If you *must* do open-ended debugging then
	* Your debugging is done entirely via unit tests and code inspection.
	* No need for console.log statements, aside from REPL verification of syntactical details.

### You are pair-worthy
* You can think out loud without losing train of thought
* What you say feels like pairing, not parroting
* i.e., not the out-loud version of “useless/redundant comments”
* You accept and apply hints / constructive criticism

### You can iterate the solution 
* You handle different evolutionary pressures
	* tighter resource constraints / scaling pressure
	* different implementation style (recursive vs iterative)
	* evolving business rules
* Your code keeps working and stays reasonable as it evolves, doesn’t turn into a structural mess or debugging hell.