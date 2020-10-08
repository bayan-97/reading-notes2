# Solve Programming Problems

1. Read the problem completely twice

**This is the single most important step**.  You may even want to read the problem 3 or 4 times.

You want to make sure you completely understand the problem.  A good test of this is whether or not you can explain the problem to someone else.

If you are given any examples along with the problem, make sure you have worked through the examples and understand why the answers are correct for each one.


2. Solve the problem manually

It is very important to solve the problem manually first, so that you know what you are going to automate, otherwise you are just slinging code around.  Which while can be fun, will make you look like an idiot in a programming interview and will probably cause you to sweat profusely.

I recommend that you solve the problem with at least three different inputs to make sure you really understand your solution and that it will work for more than one case.

## example
If I give you a string “Zebra”, and ask you to reverse it, most people will do the following manual steps.

- Write “Zebra” down.
- Start a new word, and put “a” as the first letter.  (Why –> because it is the last letter, we want to start here)
- Put “r” down as the 2nd letter.  (Why –> because it is the next letter backwards from the last letter we copied)
- Put “b” down as the 3rd letter.  (Why –> same as above)

3. Optimize the manual solution

It’s well worth the effort to try and optimize the actual solution or simplify it when it is still in the most easily malleable state.

What you want to do here is figure out if there is another way you can solve the problem easier, or if there are some steps you can cut our or simplify.

We should be able to immediately recognize that we can use a loop here to reduce the manual steps.  Our duplicate why’s for most of our steps tell us that we are doing the same thing over and over for each step, just with different data.

1. Write “Zebra” down.
2. Start at the last letter in the word and create a new empty word.
3. Append the current letter to the new word
4. If there is a previous letter, make the previous letter the current letter and start back at 3.

4. Write pseudo-code or comments

Many times you can skip this step if you have a really good handle on the problem or your previous steps already created a detailed enough description of the solution that coding it is already a 1 to 1 translation.

If you are a beginner or struggle with these kinds of problems, I would go ahead and take the time to do this step anyway though.

5. Replace comments with real code

This step should be extremely easy at this point.  If you have done all the other steps, this step involves no problem solving at all.

All we do here is take each comment and convert it into a real line of code.


`String newWord =""`
`for(int index = oldWord.Length – 1; index <= 0; index—)`
   `newWord += oldWord[index];`
`return newWord;`


6. Optimize the real code


Sometimes this step isn’t necessary, but it’s worth taking a look at your code and figuring out if you can cut out a few lines or do something simpler.

This is also a good place to make sure all your variables are named with long meaningful names.  I cannot stress enough how important having good names for your variables and methods is for helping the person evaluating your code to understand what you were trying to do.  This is especially important when you make a mistake!

I won’t give an optimization for our trivial example of a string reversal, but a word of advice here is not to get too tricky.  Just try to mainly simplify your code and get rid of duplication.

## “Being busy is a form of mental laziness.” -Tim Ferriss

Extremely successful people don’t tolerate busywork or distraction. They have crystal clear vision on their goals, and do what they need to do to get there, every single day.

Deep work means absolutely not tolerating distractions and producing monumental quality and quantity in a very short time. This is how you can complete far more with focused efforts than unfocused efforts with far more time.


**“People think focus means saying yes to the thing you’ve got to focus on. But that’s not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I’m actually as proud of the things we haven’t done as the** **things I have done. Innovation is saying no to 1,000 things.”**
This process of weeding out the merely “good” for the truly great opportunities is easier when you value your time at $1,000/hour. Anything you can honestly justify doing for $1,000/hour is probably a good thing.


# How to think like a programmer 

The best way involves a) having a framework and b) practicing it.

“Almost all employers prioritize problem-solving skills first.
Problem-solving skills are almost unanimously the most important qualification that employers look for….more than programming languages proficiency, debugging, and system design.
Demonstrating computational thinking or the ability to break down large, complex problems is just as valuable (if not more so) than the baseline technical skills required for a job.” — Hacker Rank (2018 Developer Skills Report)


what should you do when you encounter a new problem?

1. Understand

This is why you should write down your problem, doodle a diagram, or tell someone else about it (or thing… some people use a rubber duck).

2.  Plan

In programming, this means don’t start hacking straight away. Give your brain time to analyze the problem and process the information.
3. Divide

Then, solve each sub-problem one by one. Begin with the simplest. Simplest means you know the answer (or are closer to that answer).

After that, simplest means this sub-problem being solved doesn’t depend on others being solved.

Once you solved every sub-problem, connect the dots.

4. Stuck?

three things to try when facing a whammy:


- Debug: Go step by step through your solution trying to find where you went wrong. Programmers call this debugging (in fact, this is all a debugger does).

- Reassess: Take a step back. Look at the problem from another perspective. Is there anything that can be abstracted to a more general approach?

- Research: Ahh, good ol’ Google. You read that right. No matter what problem you have, someone has probably solved it. Find that person/ solution. In fact, do this even if you solved the problem! (You can learn a lot from other people’s solutions).

# 5 Whys Getting to the Root of a Problem Quickly


## When to Use a 5 Whys Analysis
You can use 5 Whys for troubleshooting, quality improvement, and problem solving, but it is most effective when used to resolve simple or moderately difficult problems.

It may not be suitable if you need to tackle a complex or critical problem. This is because 5 Whys can lead you to pursue a single track, or a limited number of tracks, of inquiry when, in fact, there could be multiple causes.

1. Assemble a Team
Gather together people who are familiar with the specifics of the problem, and with the process that you're trying to fix. Include someone to act as a facilitator , who can keep the team focused on identifying effective counter-measures.

2. Define the Problem
If you can, observe the problem in action. Discuss it with your team and write a brief, clear problem statement that you all agree on. For example, "Team A isn't meeting its response time targets" or "Software release B resulted in too many rollback failures."

Then, write your statement on a whiteboard or sticky note, leaving enough space around it to add your answers to the repeated question, "Why?"

3. Ask the First "Why?"
Ask your team why the problem is occurring. (For example, "Why isn't Team A meeting its response time targets?")

Asking "Why?" sounds simple, but answering it requires serious thought. Search for answers that are grounded in fact: they must be accounts of things that have actually happened, not guesses at what might have happened.

This prevents 5 Whys from becoming just a process of deductive reasoning, which can generate a large number of possible causes and, sometimes, create more confusion as you chase down hypothetical problems.

4. Ask "Why?" Four More Times
For each of the answers that you generated in Step 3, ask four further "whys" in succession. Each time, frame the question in response to the answer you've just recorded.



5. Know When to Stop
You'll know that you've revealed the root cause of the problem when asking "why" produces no more useful responses, and you can go no further. An appropriate counter-measure or process change should then become evident. (As we said earlier, if you're not sure that you've uncovered the real root cause, consider using a more in-depth problem-solving technique like Cause and Effect Analysis , Root Cause Analysis , or FMEA .)

If you identified more than one reason in Step 3, repeat this process for each of the different branches of your analysis until you reach a root cause for each one.


[](https://www.mindtools.com/media/Diagrams/5_Whys_Figure_2_multiple_lanes.pdf)



6. Address the Root Cause(s)
Now that you've identified at least one root cause, you need to discuss and agree on the counter-measures that will prevent the problem from recurring.

7. Monitor Your Measures
Keep a close watch on how effectively your counter-measures eliminate or minimize the initial problem. You may need to amend them, or replace them entirely. If this happens, it's a good idea to repeat the 5 Whys process to ensure that you've identified the correct root cause.