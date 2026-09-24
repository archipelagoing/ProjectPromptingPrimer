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
