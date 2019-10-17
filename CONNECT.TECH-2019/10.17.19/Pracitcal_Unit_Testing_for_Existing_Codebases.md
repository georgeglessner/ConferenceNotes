# Practical Unit Testing for Existing Codebases
> K. Devin McIntyre

### Overview
- Blockers
	- Time
	- Practical Knowledge
	- Existing codebase
	- Team and management buy-in

### Time

Example unit-test-free process:
- First draft
- Trial and Error
- QA

Test-During:
- First draft
- trial and error
	- write unit tests during this phase 
- QA
	- finishes the automated system tests

Why use Test-During
- Productivity increases
- Gain experience
- Easier to change habits gradually
- Find bugs faster
- Don't need to keep automatically checking your work

Starting test-driven:
- decide whether you want to 
- gain experience with unit testing best practices
- understand how unit tests and code reflect each other
- mentally prepare for continuous refactoring, redesigning, and "failure"
- Try it with defects first

### Practical Knowledge
- Getting started
	- choosing test framework
		- what are other people using for apps similar? 

### testing UI code in Node
- Mimic the UI enviornment with JSDOM
- Support Node natively, then convert files during build process
- Use funcitonal / system tests of UI to complete your test coverage

### What to unit test
- "Contracts" of public functions
	- Beginning state / end state
- Logic branches

### What not to test
- every possible solution
- 3rd party tools
- theoretical ways things could be used but probably never will be

### State controle
- Do not let state bleed between individual tests
- Must restore previous state
- Avoid pollution of global objects
- memory leaks will break your tests
- may need to add "destroy" / "reset" funciton

### Stubs and Mocks
- Mock - a whole object to be another object
- Stub/spy - temporarily replacing an object's method

## Existing Codebase

### Setup File
1. Manually recreate the global state
2. Start writing tests for app code; the next step can wait
3. Refactor as much of your initial load/configuraion logic as possible in testable pieces, preferably in separate files

### Helper files
- used for difficult source code files
- move logic out of te difficult files into this new one
- write unit testa against the helper file
- only the one difficult file uses the heldper as a dependency
- intended as a **temporary** refactoring tool

### Cleanup code
- Functions like destroy/reset that clears state at the end of a unit test
- need to remove listeners, clear timeouts/intervals, set object pointers to undefined

### Refactoring a file for unit tests
- strictly maintain all public methods within the file
- only add or move code; do not remove or change anything (yet)
- focus on
	- control of state
	- splitting code into smaller, testable pieces

### Be Cautious
- Dont rush to delet anything
- avoid "improving" code until you have good coverage
- track the bugs you dins as real defects/issues

### Prioritaztion
- "canary"
	- if this test fails, you know you've broken your setup, failed to install something, etc
	- keep it around, you never know what could break your test environment
- easy file
	- pulling in one or two easy files lets you test whether you've set up the test env correctly for your app. 
- dependency tree roots
	- files that are most depended on should ideally gain test coverage first. 
	- look at your dependents to help think of test cases.
	- work your way gradually to files further along the tree, in order or "reach" or importance
- mission critical areas
- defect areas
	- add coverage for your worst defect areas
	- as you fix new defects, add unit tests for them
- error  handlers
	- those that are user-facing or otherwise important
	- those that communicate with third parties
	- not those that just log an error


Real code examples

_**The more tests you have, the more tests you have to maintain**_