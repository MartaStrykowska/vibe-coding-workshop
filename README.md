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

### 🔺 Optional (this is for the advanced users only)

If you've never worked in Claude Code using the terminal, here's how to set it up: 

Type this command: (placeholder for a command) curl -fsSL https://claude.ai/install.sh | bash

When it’s done, you’ll see “Claude Code successfully installed!”. 

Do you have an existing project and want to continue working in it? Use command: 
cd /path/to/your/project
claude

Replace path/to/your/project with the path of where your project folder lives on your computer. If you only have Github available and no project folder on your laptop, you need to clone your Github repo to your laptop using this command (replace the name with your repo name): 
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
claude

Do you want to start from scratch? Type this commands in your Terminal all at once: 
mkdir my-project-name
cd my-project-name
claude

---

## 💬 Starting first with the Plan mode 

Copy, paste, and adapt these in Lovable or any AI coding tool.

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
