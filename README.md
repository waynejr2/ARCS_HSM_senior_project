# CSUN COMP 490 Senior Design Project - ARCS HSM proteus code verification and validation

## Wayne Rasmussen   10/19/2023 ##

## Doctor Dewey's Compiler Design series to watch ##
  - Compiler_Core_-_Part_1_-_Compiler_Internals  - Completed
  - Compiler_Core_-_Part_2_-_Tokenization  -- Completed
  - Compiler_Core_-_Part_3_-_Parsing  -- Completed
  - Compiler_Core_-_Part_4_-_Typechecking  -- Completed
  - Compiler_Core_-_Part_5_-_Code_Generation  -- Complete

## Doctor Dewey's Intro to HSM videos ##
  - These are the Thursday/Friday zoom meetings - up to date

## StateMachine.com media to consume -- completed ##

<https://docs.google.com/document/d/1yl9MzZ8Ib8TEpnE8Nj78Yp_ksdMXEGqrQBrlMA7svEA/edit> \
<https://www.state-machine.com/fsm#HSM> \
<https://www.state-machine.com/qpc/srs_sm.html> \
<https://www.state-machine.com/qpc/srs_ao.html>

## My Goal for things I need to get done before 10/26/2023 are: ##
  - getting the V1 compiler to run on my system
  - Compiler has been built.  gen-coverage.sh fails due to missing packages in os env
  - making a list of what I want to do in this project

## What I want to consider doing on this project.  List likely to be narrowed down ##
  - TDD with mutation testing on V1 Compiler
  - automatted HSM test code generator V1 Compiler and V2 if possible
  - fuzzing testing parts of the V1 compiler
  - verification/validation (likely way too big to do and perhaps not possible)

## Reading books and pdf -- work in progress ##
# How google Tests Software #
  - Good book - Talks about CI as being important. Perhaps on a VM (I will look into this).
  - Chapters 1, 2, 5 are most pertinent.
# FUZZING - Brute Force Vulnerability Discovery #
  - This is considered to be an advanced book on FUZZING
  - Very good introduction to the material
  - Part 1 Backgroun - chapters 1,2,3 are introduction to the subject.  MUST READ!!!
  - Part 2 Targets and Automation - Need to narrow down the chapters that we might want to consider
  - Part 3 Advanced Fuzzing Technology - Might not get to this at all but is solid looking.
# Certified Programming with Dependent Types #
  - Very advanced introduction to Coq Proof Assitant.  Might help, but might be more of a MS degree level.
# Specifying Systems #
  - ANother advanced book, some chapters might come in handy for multithreading or time sensitive code.
# Unit Test Frameworks #
  - Chapters 1, 2, 4, 6 might be useful.  The introduction and junit parts in those chapters.
# Software Abstractions #
  - need to revisit this at some time to see if there is something we can use.
  - Pages 250, 251 has a little bit of insight into State Machines that could be good to know.
# Proteus Language pdf #
  - Critial
  - Might need to write new documentation based on the class project
# Test Driven Development #
  - Have not look at yet.
# Testing Threading Thought Experiements.
passing 1 dollar around (AKA Money Maker):

N actors who pass the dollar around.  Can we end up with more than 1 dollar in the system

***************

sequence order test

Version 1)  N actors and 1 CENTRAL HUB actor.  
N actors signal HUB,  
HUB knows the first N signal Actors.  
Tests:  
	In the first N signals to HUB the sequence  
		Does the sequence have any repeated actors or is each listed once?  
	Is the sequence preserved over time?  
	Actor Counts, each Actor has a count of the number of times it has signaled,  
		over a long time, how close are these numbers.  


***************

Critical Toggle:  
Given N Actors in state [0|1]  
Rules based on their neighbors, determine if they flip state.  
	what happens?  
Note:  kind of like Conway's Game of Life.  

***************

Monkey Chatter:  
N Actors, chatting over time:  
can we create a test the over time could lead to:  
    Chatting stopped  
	Chatting remains the same  
	Chatting gone wild AKA Monkey Chatter  

***************

Stock Market:  AKA Trading Places stock market  
Can we flood the system with events?  
Is that a kind of malloc going on?  
N actors, When A Actor signals, it Signals all other actors.  
When an actor gets signalled, it signals all other actors.  
How large does the queue grow?  
Do we run out of space/crash the system.  
If we keep adding to the thread queue, when will we run out.  

***************

EVENT QUEUE size for threading.  

Can it really grow?  
***************
***************

