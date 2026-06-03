# 🧪 AI Build Labs — Vibe Coding Workshop

This repo contains the setup guide and prompt reference for the [AI Build Labs](https://launchpads.ai) vibe coding workshop. It covers everything you need to go from idea to deployed app using [Lovable](https://lovable.dev), [GitHub](https://github.com), and [Vercel](https://vercel.com) — and is designed to be a reference you can come back to whenever you start a new project.

> Questions? Reach out at [marta@launchpads.ai](mailto:marta@launchpads.ai)

---

## ⚡ Before the Workshop — Setup

You'll need three free accounts set up before we start. This takes about 10 minutes.

### 🐙 1. GitHub — use your work email

1. Go to [github.com](https://github.com) and create a free account — use your **company email**
2. Once logged in, click the **+** icon → **New repository**
3. Name it after your project (e.g. `hello-world`)
4. Set visibility to **Private**

Your repo URL will look like: `github.com/YourAccount/hello-world`

> Already have GitHub? Just sign in and create a new private repo.

### 💜 2. Lovable — use the invite link for extra credits

Sign up at: **[https://lovable.dev/invite/P4SRJ30](https://lovable.dev/invite/P4SRJ30)**

Use any email address you like. If you already have a Lovable account, just log in during the workshop.

### 🔺 3. Vercel — sign in with GitHub

Create a new account at [vercel.com](https://vercel.com) and click **Continue with GitHub**. The free Hobby plan is all you need.

### 💻 Optional — Claude Code (advanced users only)

If you want to work directly in the terminal using Claude Code, here’s how to get set up.

**Step 1 — Install Claude Code**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

When it’s done, you’ll see: `Claude Code successfully installed!`

**Step 2 — Start a session**

Pick one of the three options below depending on your situation:

_I have an existing project folder on my laptop:_
```bash
cd /path/to/your/project
claude
```
Replace `/path/to/your/project` with the actual path to your project folder.

_I only have a GitHub repo (no local folder yet):_
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
claude
```
Replace `yourusername` and `your-repo-name` with your actual GitHub username and repo name.

_I want to start from scratch:_
```bash
mkdir my-project-name
cd my-project-name
claude
```
Replace `my-project-name` with whatever you want to call your project.

---

## 🗺️ Step 1 — Start with Plan Mode

Before writing a single line of code, use Plan Mode to think through the build like a software engineer would. This keeps you in control of the structure and prevents messy, hard-to-fix code later.

---

### 💜 Lovable users

1. Open your Lovable project
2. Toggle **Plan Mode on** (top right of the chat panel)
3. Copy the prompt below, fill in your requirements, and send it

```
I want to build [describe your tool in 1–2 sentences].

Here are the features it needs:
- [Feature 1]
- [Feature 2]
- [Feature 3]
(add as many as you need)

Structure the plan like a software engineer would approach it:
1. Start with the data model — what data needs to be stored and how is it structured?
2. Break the build into clear, sequential phases — each phase should be small enough to build and test on its own
3. For each phase, describe: what is being built, what the expected outcome is, and what to test before moving on
4. Flag any dependencies between phases (e.g. authentication must come before user-specific data)
5. End with a summary of the full build sequence so I have a clear picture of the journey from start to finish
```

---

### 💻 Claude Code users

Type the following slash command to enter Plan Mode:
```
/plan
```
4. Then paste and fill in this prompt:

```
I want to build [describe your tool in 1–2 sentences].

Here are the features it needs:
- [Feature 1]
- [Feature 2]
- [Feature 3]
(add as many as you need)

Think and plan like a senior software engineer:
1. Start with the data model — what tables, fields, and relationships are needed?
2. Break the build into clear, sequential phases — each phase should be small enough to build and test independently
3. For each phase, include: what is being built, the expected outcome, a security check relevant to that phase, and a git commit at the end
4. Flag dependencies between phases (e.g. set up auth before building user-specific features)
5. End with a summary of the full sequence

When the plan is finalised, save it as a file called PLAN.md in the root of the project and add it to version control.
```

> Once the plan is saved, exit Plan Mode and start building phase by phase using the PLAN.md as your guide.

---

## 💬 Prompt Examples — Building Phase by Phase

Use these once your plan is in place. Copy, adapt, and send one at a time.

### 🚀 Start a new project from scratch
```
Build a [type of app] for [who uses it].
It should be able to [main thing it does].
Keep the design clean and modern. Use a simple colour palette.
```

### 🖼️ Build from a screenshot or mockup
```
Here's a screenshot of the design I want to build: [attach image]
Implement this as a web app. Make it responsive for mobile and desktop.
```

### ➕ Add a new page or feature
```
Add a /dashboard page that shows:
- A welcome message with the user's name
- A list of recent activity (mock data is fine for now)
- A sidebar with navigation links
Use the same layout and styling as the rest of the app.
```

### 🔁 Iterate on something that exists
```
The current [feature] works, but I want to improve it:
- [change 1]
- [change 2]
Keep everything else the same.
```

### 🐛 Fix something that's broken
```
This isn't working as expected: [describe the problem]
Here's what I see: [paste error or describe behaviour]
Please fix it without changing anything else.
```

### 🎨 Change the look and feel
```
Update the styling so it looks more [professional / playful / minimal / bold].
Keep the layout and functionality exactly the same — only change colours, fonts, and spacing.
```

### 🔍 Explain what was built
```
Explain what this code does in plain English.
I'm not a developer — use simple language and flag anything I should be aware of.
```

---

## 🔐 Security Prompt

Run this after completing any major phase to catch issues before they become problems.

```
Review what we've just built from a security perspective.

Check for the following:
- Are any API keys or secrets exposed in the frontend code?
- Is all user input validated before it reaches the database?
- Are the correct access rules in place — can users only see and edit their own data?
- Are there any routes or actions that should require login but currently don't?
- Is there anything else that looks risky or could be exploited?

For each issue you find, explain it in plain English and suggest how to fix it.
If everything looks good, confirm that and explain why.
```

---

## 💻 Useful Terminal Commands (Claude Code users)

These are the commands you'll reach for most often during a session.

| Command | What it does |
|---|---|
| `claude` | Start a Claude Code session in the current folder |
| `/plan` | Enter Plan Mode — think before you build |
| `/context` | Show what Claude currently knows about your project |
| `/memory` | View and edit Claude's memory (your CLAUDE.md) |
| `/clear` | Clear the current conversation and start fresh |
| `Ctrl + C` | Stop whatever Claude is doing |
| `exit` | End the session |

**Git commands you'll use alongside Claude:**

```bash
git status                   # See what files have changed
git add .                    # Stage all changes
git commit -m "your message" # Save a snapshot with a description
git push                     # Push changes to GitHub
git log --oneline            # See a history of your commits
```

---

## 🛠️ Troubleshooting Prompts

When things go wrong, these prompts help you get back on track without losing what you've built.

### Something broke after the last change
```
Something stopped working after the last change. Here's what I expected to happen:
[describe expected behaviour]

Here's what's actually happening:
[describe what you see, paste any error messages]

Please identify what went wrong and fix only that — don't change anything else.
```

### The app won't start or load
```
The app isn't loading. Here's the error I see:
[paste the error from the terminal or browser console]

What's causing this and how do I fix it?
```

### Claude did something I didn't want
```
The last change wasn't what I intended. Please undo everything from the last response
and bring the code back to how it was before. Then let's try again — I'll re-explain what I want.
```

### Something looks wrong but I don't know why
```
Something feels off but I can't pinpoint it. Can you review the current state of
[page or feature name] and flag anything that looks incorrect, incomplete, or inconsistent
with the rest of the app?
```

### I'm getting a database or API error
```
I'm seeing this error when trying to [action]:
[paste the error]

This is connected to [database / API name]. What's causing it and how do I fix it?
Don't change anything else in the project while fixing this.
```
