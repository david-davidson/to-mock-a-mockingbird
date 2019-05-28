Raymond Smullyan's _To Mock a Mockingbird_ explores various problems in combinatory logic through the extended metaphor of a forest full of birds. Each bird represents a combinator function: a simple, generic, often higher-order function that operates on no variables other than its arguments. (The Mockingbird, for example, takes one argument and returns the result of invoking it with itself: `const Mockingbird = x => x(x)`).

This repo captures notes and solutions from working through Smullyan's puzzles. (So far, I've only been able to figure out #7 without checking the answers, which can be quite dense—these notes are for explaining the answers to myself.)

* [1: The Signifance of the Mockingbird](problem-1/README.md)
* [2: Egocentric?](problem-2/README.md)
* [3: Story of the Agreeable Bird](problem-3/README.md)
* [4: A Question on Agreeable Birds](problem-4/README.md)
* [5: An Exercise in Composition](problem-5/README.md)
* [6: Compatible Birds](problem-6/README.md)
* [7: Happy Birds](problem-7/README.md)
* [8: Normal Birds](problem-8/README.md)
