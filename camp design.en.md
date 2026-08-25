# Agent-Assisted Software Development Camp

**Device requirements**: A Chromebook, iPad, or ordinary computer (with a keyboard or voice input).

**Software requirements**: Only a modern browser is needed.

**Required before class**: A GitHub account; a Copilot subscription is recommended.

---

## Session 1: Open the Cloud IDE

**Goal**: Create a project repository, open the cloud editor, and use an Agent to write your first line of code.

### 00:00–05:00 Introducing the Concepts

- GitHub: the industry's largest platform for sharing (open source) and collaborating on (version control) software projects.
- Repo: the project folder.
- Codespace: the project editor (IDE).
- GitHub Pages: the project's website.

### 05:00–15:00 Hands-On Setup: Create the Project, Open the Editor

**The teacher leads on a shared screen while students follow along:**

1. Open a browser, go to `github.com`, and make sure you are signed in.
2. Click the **green [New] button** in the upper-right corner of the page (or click the `+` in the upper-left corner and choose `New repository`).
3. In the **Repository name** box, enter a lowercase English name, such as `my-first-magic` (any letters will do).
4. Scroll down and **be sure to check [Add a README file]** (very important — this lets our workshop start smoothly).
5. Click the **green [Create repository] button** at the bottom of the page.
6. On the new page, click the green **[<> Code]** button.
7. In the menu that pops up, click the **[Codespaces]** tab.
8. Click the green **[Create codespace on main]**.

* *Tell the students: the page will now turn black and start loading.*

### 15:00–30:00 Summon the Agent: Write Hello World

**Working inside the Codespace interface:**

1. Start a session. Say "Hi" in the chat window on the right.
   - A sign-in window will pop up; sign in with your GitHub account.
   - After signing in, the Agent will respond.
   - If you get the error "Language model unavailable," sign in and try again.

   ![Starting a session](image.png)

2. Start building the webpage. Tell the Agent: `Please write a GitHub Pages webpage that says "Hello World!"`
   - The content is up to you; it doesn't have to be exactly the same.
3. Check the webpage.
   - Type `python -m http.server` in the terminal to serve the page.
   - `Ctrl`/`Cmd` + click the link below, `http://0.0.0.0:8000/`.
   - A new tab will open with the content you asked for.
   - If you're not happy with it, you can chat with the Agent and ask it to make changes.
   - When you're happy with it, click [Keep].
   - Press `Ctrl + C` to stop the server.
4. Publish the webpage.
   - Tell the Agent: `Please push the current changes to GitHub`
     - Click [Allow] every time.
   - Go back to the GitHub repo page and click the Settings tab.
   - Choose Pages on the left.
   - Set Branch to main, then click [Save].

     ![alt text](image-1.png)

     - After that, you'll see the link to your webpage on the Pages screen.
     - Both the first publish and every later change take a few minutes before the newest version shows up.

### 30:00–40:00 Show Off the Results

You've published a webpage of your own! Send the link to your teacher and classmates so they can take a look.

- The teacher collects and backs up the students' webpage links.

### Tool Substitutions

A paid Agent is recommended, so as to avoid some pointless problems. Besides paying for GitHub, paid ChatGPT or Claude accounts also work; you'll need to install the corresponding extension and sign in inside it.

- ChatGPT users: install the Codex extension.
- Claude users: install the Claude extension.

You can also use the Live Server extension to serve the webpage instead of the python command, which is more convenient.

### Situations That May Come Up

Because Agent behavior is unpredictable, various situations will arise.

- It's best for teachers and teaching assistants to be familiar with the relevant GitHub concepts. Even if you don't teach them to the students, you can use them to help students debug.
  - main branch
  - commit
  - push
- Make sure the mode is Agent and not something else; this mode carries out tasks automatically as much as possible.
- In a simple camp like this, clicking Allow/Keep all the way through is normal, because everything runs in the cloud — even an error won't crash the computer.
  - That's not to say nothing can go wrong, but at this level of camp, if something breaks you can generally just start over.

---

## Session 2: Software Design (No Computers)

**Goal**: Work out the concept and the logic of the app. This session mainly uses paper and pencil.

Hand each child a sheet of paper with the following fill-in-the-blanks:

1. **My app is called**: ____________________
2. **What does it look like on screen? (What color are the buttons? What pictures are there?)**: ____________________
3. **Game rules (core logic): when I click [something], what [change] happens?**: ____________________

### 00:00–10:00 Explain the Boundaries

The teacher explains the limits of what the program can do.

- It's only a webpage.
- No complex graphics — a large 3D game, for example, isn't possible (the main bottleneck is really performance).
- No storing data online long-term — you can't build Facebook, for example.
- No multi-party communication — you can't build Discord, for example.

#### For Beginner Students

If students' basic understanding of computers is still fuzzy, or they're younger and can only take in so much, we don't introduce everything a webpage can do all at once. Also, to reduce the workload for teachers and TAs, we keep the topics within a certain range.

Recommended:

- Working with text and numbers.
  - A journal/planner, for example.
  - A calculator.
  - A clock or calendar.
- Working with geometric shapes.
  - Geometric-style games, for example:
    - Tetris.
    - Pac-Man.
    - Whac-A-Mole.
  - A spirograph simulator.
  - Physics simulations (simulating a balance scale, simulating gears).
- Simple logic games.
  - Simon.
  - Guess the number.
  - Board and card games, but with your own rules.

#### For Advanced Students

A single webpage can actually do a great deal, and if the teachers and TAs are familiar with the relevant features and the students can handle it (high schoolers, for example), there's no reason not to include them.

The most useful part is this: when the teachers and TAs aren't familiar with a given feature either, you can simply ask the Agent first about what's possible and how to use it. Here are a few directions.

- If you need to get information from the outside world, ask the Agent: "Is there a free API for getting XXX?" If the Agent finds one, have it try fetching from it first; if the result looks good, use it in the webpage. Information like:
  - Weather.
  - Maps.
  - Random quotes.
- If you need to connect two players, use a PIN link — tell the Agent to use WebRTC PeerJS + a 6-digit PIN. Useful for head-to-head games.
- If you need to open local files, tell the Agent to use the File Access API — useful for building a text or image editor.
- If you're building a game, you can tell the Agent to use WebGL. It isn't required, but it can improve the game's graphics performance.
- If you need to save a small amount of data locally, such as settings, you can tell the Agent to store the data in Local Storage.
- A webpage can also use device hardware, such as the camera and microphone.
- If you want to use it on a phone, tell the Agent to optimize for mobile devices, including portrait display and touchscreens.

### 10:00–40:00 Students Design

Once students have finished their design, they raise a hand for a teacher or TA to review it.
Students whose designs have been approved present their designs to each other.

#### Review Criteria

- The logic needs to be complete — don't make the Agent guess what you meant.
  - Teachers and TAs mainly check the details of the design.
  - If a design is too ambitious but short on detail, guide the student toward a simple experimental version.
  - For advanced students, guide them to use `/grill-me` for an initial design check.
- There's a basic requirement for personalization.
  - Don't let students copy software that already exists; each student should produce something unique. Even the student with the fewest ideas is asked to make small adjustments to an existing form. At the very least there should be an aesthetic change. For example:
    - Logic tweak: chess with modified rules (the rules need to be described very carefully).
    - Aesthetic tweak: a journal/planner, but with a carefully considered layout (which can be photographed and uploaded to the Agent).

On the subject of complete logic, see [Beakman S2EP10](https://www.youtube.com/watch?v=TkSEcNv3FIU).

---

## Session 3: Implement the Code

**Goal**: Turn natural language into code and get the first version of the program running.

### 00:00–10:00 Upload the Design

The teacher walks students through it step by step:

- Just like in Session 1, open the chat with the Agent.
- Photograph the design sheet from earlier, upload it to the Agent, and say in chat: "Build a GitHub Pages web app according to these requirements. If anything is unclear, ask me before writing code."
  - Beginner students, whose designs are simple, can start writing code right away.
  - Slightly more advanced students should use plan mode so the Agent digests the design document before writing code.
- Check the output the same way as in Session 1.
- The output very likely won't match exactly what the student had in mind; when that happens, chat with the Agent again and tell it where things differ from what was expected.
- If bugs show up, you can also have the Agent fix them — a blank screen or a crash, for example.
  - Advanced students can be guided to send the errors from the F12 console to the Agent.
- Finally, don't forget to push; the procedure is the same as in Session 1.

### 10:00–40:00

From here on, you're in the loop of [give the Agent requirements → the Agent writes code → check the resulting webpage]. It's perfectly fine to step back and let students do it themselves.

When students finish, they can have a teacher or TA check their work.

- If the check turns up a bug, have the student fix it.
- If there's still plenty of time, the teacher can propose a new feature requirement or a suggested improvement.
  - The most common suggestion is to ask the student to add instructions:
    - "If someone opens your site for the first time, will they know how to play/use your app?"
  - Another suggestion is to make it look better:
    - For example, if the interface is blue, you might say, "I like pink — can you add an option that lets me set the interface color?"

---

## Session 4: User Feedback

### 00:00–10:00 Explanation

Hey, it's time to share.

The teacher compiles and publishes the links to all the students' apps and opens a feedback board.

Every student is asked to try out other people's apps and give feedback.

We want to give constructive feedback — the kind a developer can actually act on after reading it.

We use a fixed sentence pattern: "If XXX could YYY, it would meet my need to ZZZ." (This is mainly to keep feedback from causing friction between students.)

Students can also send their apps to parents, relatives, and neighbors to get feedback.

### 10:00–40:00 Share Party

Every app gets at least 1–2 comments.

Comments are anonymous; if a student has few comments, teachers and TAs should help by adding some.
Any inappropriate feedback should be hidden, to protect the students.

---

## Session 5: Iterate and Revise

### 00:00–10:00 Explanation

We've now collected a set of feedback, and it's all real user feedback.

We're now going to revise our apps based on that feedback and make them better.

### 10:00–40:00 Practice

Spend this time continuously revising the app.

Teachers and TAs go back to what they were doing in Session 3.

Students can also find new things to change by playing with their app themselves.

Even if students get absorbed in playing their own work or other people's, that's fine — the goal of this camp is for students to build a sense of accomplishment around delivery, and this is part of that.
