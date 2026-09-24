# ProjectPromptingPrimer
We can get a very quick turnaround on our projects these days! But how organized does your repo get, and how difficult is it to stay on task, rather than getting bogged down in random bugs or your coding assistant changing directions midway through prompting? 

I've made a LOT of really interesting projects from fairly basic ideas because I used interesting prompting techniques & project organization! Remember, your coding agent or assistant is equally as capable of getting distracted as you are! Without a source of truth, it's pretty difficult to stay organized with your project. Here are a couple important files, and the relevant prompts to maintain them. 

-----------------------------
- todo.md
-  Relatively self explanatory. This is your project's to-do list. It should keep track of what's working, whats broken, and why it isnt working. If you ever need to present your project to others, you can easily explain the state of your project with a file like this.
-  [?] Why is this better than using a coding agent to explore the context of your entire repo?
-  [a;] A coding agent exploring the context of your entire repo will weigh all the files in your repo similarly.
-  If you pick up a project again after a couple months, it might be able to look thru your git commits and figure out what was working, but it definitely wont remember the context of what wasn't working and why
-  It is much easier to maintain this markdown file after each git commit message than maintain long documentation for each method! 
-  Reconstructing the context each time can cost up to \(O(kn)\).
-  Writing a short update when each change happens costs \(O(n)\) total. Reading a bounded current-state summary on each return costs \(O(k)\), giving \(O(n+k)\).
------------------------------
- SHOW_BIBLE.md
-  This is the file that explains how to keep building the project without accidentally turning it into a different project. `todo.md` tells you where you left off; the show bible tells you how everything is supposed to fit together.
-  Include the basics: what the project does, how to run it, where the important code lives, and which parts should stay consistent as you add features.
-  [?] Isn't that just a README?
-  [a;] A README helps someone get started. This file is for the person (or coding agent) who comes back three months later and thinks, “Where should this feature go, and why did I build the rest of it this way?”
-  The name comes from TV writing. A show bible helps different writers keep the characters and world consistent across episodes. Here, it helps you and your coding assistant make new features that still belong in the same project.
-  Try to write down actual decisions, not vague goals. “Keep it simple” sounds nice, but “Put new settings in `src/config/` and give each one a default” is much more useful.
-  Update it when you change something fundamental about how the project works. You don't need to touch it for every little bug fix.
------------------------------
- RubricATM.md
-  ATM stands for “at the moment.” This file describes what the best version of your project would look like, then takes an honest look at what you’ve built so far.
-  [?] Why would I grade my own project?
-  [a;] Because after a while, it’s easy to lose track of the big picture. You might spend an afternoon fixing tiny visual details and forget that someone still can’t get through the main feature without hitting an error.
-  I’d give points for things that matter to *this* project, like whether the main idea works, how it handles things going wrong, and whether another person could figure out how to run it. For each score, write down what you actually checked and what’s still missing.
-  Update the grade after a meaningful round of work. Keep the latest one at the bottom of the file, and let Git history hold onto the older versions. You don’t need a new rubric for every commit.
-  The most useful part is the end: pick the three changes that would improve the project the most right now. That gives you somewhere to start next time you open the repo.
------------------------------
## The project loop

**`SHOW_BIBLE.md` → `RubricATM.md` → `todo.md` → build → `todo.md` → `RubricATM.md` → repeat**

1. **Read `SHOW_BIBLE.md`.** Understand what the project is and which rules should stay consistent.
2. **Read `RubricATM.md`.** Compare the current repo with the version you’re aiming for. Find the biggest gap.
3. **Update `todo.md`.** Turn that gap into a specific task.
4. **Build and verify.** Make the change and check that it works.
5. **Update `todo.md` again.** Record what worked, what broke, and what’s left.
6. **Update `RubricATM.md`.** After a meaningful iteration, reassess the project and choose the next gap.

Update `SHOW_BIBLE.md` when you change how the project is supposed to work. Otherwise, use it as the reference at the start of each loop.


