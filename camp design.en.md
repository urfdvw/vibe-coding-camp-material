# 🪄 Vibe Coding Magic Programming Lab Guide

**Device requirements:** A Chromebook, iPad, or regular computer (a keyboard is recommended).  
**Software requirements:** Only a modern browser is needed (Chrome or Safari recommended).  
**Before class:** Make sure each student is signed in to a GitHub account.

---

## 🟢 Session 1: Open the Cloud Magic Workshop

**Goal:** Create a repository (the “magic backpack”), open a cloud editor (the “magic workshop”), and use AI to write the first line of code.

### 🕒 00:00–05:00 Introduce the Concepts

* **Teacher script:** “Today we’re going to learn how to write code by talking! First, we need a ‘magic backpack’ for storing our code (GitHub). Then we’ll enter our ‘cloud workshop’ (Codespaces).”

### 🕒 05:00–15:00 Hands-on Setup: Create the Backpack and Open the Workshop

**👉 The teacher demonstrates on a shared screen while students follow along:**

1. Open a browser, visit `github.com`, and make sure you are signed in.
2. Click the green **[New]** button in the upper-right corner (or click the `+` in the upper-left corner and choose `New repository`).
3. In the **Repository name** box, enter a lowercase English name such as `my-first-magic` (any letters are fine).
4. Scroll down and **make sure [Add a README file] is checked**. This is very important because it allows the workshop to start correctly.
5. Click the green **[Create repository]** button at the bottom of the page.
6. On the new page, click the green **[<> Code]** button.
7. In the menu that opens, click the **[Codespaces]** tab.
8. Click the green **[Create codespace on main]** button.

* *Tip: The screen will turn dark while the environment loads. Tell the children, “Your magic workshop is being built for you in space. It will take about 30 seconds.”*

### 🕒 15:00–30:00 Summon the AI: Write Hello World

**👉 Work in the dark-themed Codespace interface:**

1. **Create a file:** Right-click in the blank area on the left (or click the file icon with a plus sign), choose **New File**, name it `index.html`, and press Enter.
2. **Call the helper:** Click the **Chat bubble icon (Chat)** in the far-left sidebar. This opens the AI helper, Agent.
3. **Say the magic spell:** In the Chat box, have the child type or dictate the following prompt (typos are okay):

> “Help me make a simple webpage. Write my name (for example, Alex) in huge, colorful letters and put a cat emoji next to it. Please put all the code in one file.”

4. Press Enter to send it. The AI will quickly generate some code.
5. **Cast the spell:** Hover over the upper-right corner of the AI’s code block. Click the **file icon with a right arrow (Apply in Editor)** or the **copy icon**. The code will be placed in the `index.html` file you just created.

### 🕒 30:00–40:00 See the Magic: Preview the Webpage

1. **Install the preview extension:** Click the **four-square icon (Extensions)** in the left sidebar, search for `Live Preview`, and click **[Install]**. This only needs to be done once.
2. Return to `index.html`, right-click inside the code, and choose **[Show Preview]**.
3. The webpage will immediately appear on the right, showing the child’s name and a cat!
4. From the top menu, choose **File -> Auto Save**. Turning on automatic saving now will prevent problems in later sessions.

---

## 🟡 Session 2: Little Inventors (No Computers)

**Goal:** Develop an app idea and organize its logic. This session mainly uses paper and pencils.

### 🕒 00:00–10:00 Set the Boundaries

* **Teacher script:** “You now have the power to direct a computer, but webpages have limits. We can’t make a complicated 3D racing game, but we can make: 1. a button that drops coins when clicked; 2. a digital pet you can feed; or 3. a random joke generator. What would you like to make?”

### 🕒 10:00–25:00 Complete the “Magic Blueprint”

**👉 Give each child a sheet of paper with these prompts (or use a notes app on a tablet):**

1. **My app is called:** ____________________
2. **What does the screen look like? (What color are the buttons? What pictures are there?):** ____________________
3. **Game rule (core logic): When I click [something], [what change] happens:** ____________________

### 🕒 25:00–40:00 One-on-One Teacher Approval (Flipped Classroom)

**👉 The teacher visits each child:**

1. Listen as the child explains the idea.
2. **Check the logic:** “When you choose rock, how does the computer choose its move? Is it random?”
3. **Simplify the requirements:** If the design is too complicated, guide the child by saying, “How about we build the first level today?”
4. Draw a big “✅” on the child’s paper to show that the design is approved.

---

## 🟠 Session 3: Summon the AI Helper (Build the Code)

**Goal:** Turn natural language into code and get the first version of the program running.

### 🕒 00:00–10:00 Prepare to Communicate

* **Teacher script:** “Take out the blueprint you made yesterday. Today we’re going to read it to our helper exactly as you wrote it.”

### 🕒 10:00–25:00 Enter the Blueprint

**👉 Open the computer or iPad:**

1. Visit `github.com/codespaces`, find the workshop created in the previous session, and open it.
2. Delete the old code from `index.html`.
3. Open Copilot Chat on the left and enter the ultimate magic spell:

> “I am a first-grade student. Please help me make a webpage game.  
> My game is called: [read the name from the blueprint].  
> The rules are: [read the rules from the blueprint].  
> **Please put all the HTML, CSS, and JavaScript in a single index.html file. Do not split it into separate files!** Make the buttons large and use bright colors!”

4. Send the prompt to Agent and wait for it to generate the code.
5. Click **Apply in Editor** (the arrow icon) in the upper-right corner of the code block to place the code in `index.html`.

### 🕒 25:00–40:00 First Preview and Troubleshooting

1. Right-click the code and choose **[Show Preview]**.
2. At this point, the game will probably already run. Let the children try it!
3. *If something goes wrong:* If the preview is blank, tell the child to say to Agent, “The screen is blank and nothing appears. Please check the code and rewrite it for me.”

---

## 🔴 Session 4: The Bug Detective Squad

**Goal:** Test the program, describe bugs in natural language, and add exciting extra features.

### 🕒 00:00–10:00 Explain the Detective Method

* **Teacher script:** “If the game does not behave correctly, we need to give our helper clues like detectives. Don’t just say, ‘It’s broken.’ Say, ‘When I press the red button, the score does not increase by one.’”

### 🕒 10:00–25:00 Find and Fix Bugs

**👉 Test while playing:**

1. Have the children click around enthusiastically in the preview window on the right.
2. After finding a problem, enter this in Copilot Chat:

> “There is a bug. When I [describe the action], [describe what goes wrong] happens. I want it to [describe the expected result].”

3. Agent will suggest a fix. The child clicks Apply, observes how the code changes, and checks whether the bug is fixed.

### 🕒 25:00–40:00 Cast a Makeover Spell

**👉 Once the game works, enjoy the creative side of Vibe Coding. Encourage children to ask Agent for anything they can imagine:**

* “Change the background into an animated starry sky!”
* “When I win, add a full-screen confetti animation!”
* “Change the score to a cartoon-style font!”
* *(Tip: Simply send each request to Agent as if chatting, then click Apply.)*

---

## 🟣 Session 5: Broadcast to the World

**Goal:** Save the project and publish it at a real internet address (URL) that can be shared with others.

### 🕒 00:00–20:00 Save and Publish (Important: Teacher Guidance Required)

**👉 Save the workshop’s code back into the backpack (Commit & Push):**

1. In the Codespace left sidebar, click the **third icon, which looks like a branch (Source Control)**.
2. Enter a short message in the message box, such as `Finished`.
3. Click the blue **[Commit]** button. If a confirmation dialog appears, click **[Yes]**.
4. Click the blue **[Sync Changes]** button. The code is now safely stored in the GitHub backpack.

**👉 Create a real web address (GitHub Pages):**

1. Open a new browser tab, visit `github.com`, and open the `my-first-magic` project page you created.
2. Click **[⚙️ Settings]** on the far right of the top menu.
3. Scroll down the left menu and click **[Pages]**.
4. Under **Build and deployment**, find the **Branch** section:
   * Open the `None` dropdown and select **`main`**.
   * Click the **[Save]** button next to it.
5. *Time to wait:* Tell the children it will take 1–2 minutes. They can click the `Actions` tab at the top and watch the yellow dot turn into a **green check mark ✅**, which means the site has been published successfully.

### 🕒 20:00–40:00 Sharing Party

1. Return to `Settings -> Pages`. A message will appear at the top: **Your site is live at `https://username.github.io/my-first-magic/`**, including a blue link.
2. This is the child’s own web address! Click it to open the project from anywhere on the internet.
3. **Try each other’s projects:** Children can send the link to their parents through a messaging app, or swap seats in the classroom and play the projects their classmates worked hard to create.
