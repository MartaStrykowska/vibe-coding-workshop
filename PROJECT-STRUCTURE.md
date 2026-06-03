# 📁 Project Structure — A Simple Example

Imagine you're building **helloworld.com** — a website with a homepage, a contact page, and a weather widget that pulls in live data. Here's how the project folder would be organised.

---

## 🗂️ Folder structure

```
helloworld/
│
├── app/                        # Every page of your website lives here
│   ├── page.tsx                # The homepage — helloworld.com
│   ├── contact/
│   │   └── page.tsx            # The contact page — helloworld.com/contact
│   └── api/
│       └── weather/
│           └── route.ts        # The weather API — helloworld.com/api/weather
│
├── components/                 # Reusable building blocks used across pages
│   ├── Navbar.tsx              # The navigation bar shown on every page
│   ├── Footer.tsx              # The footer shown on every page
│   └── WeatherWidget.tsx       # The weather widget (uses the API above)
│
├── public/                     # Images, logos, icons
│   ├── logo.svg                # Your logo
│   └── hero.png                # A hero image shown on the homepage
│
├── lib/                        # Code that connects to outside services
│   └── weather.ts              # The logic for fetching weather data
│
└── .env.local                  # Secret keys (e.g. your weather API key) — never shared
```

---

## 🧠 How to think about it

| Folder | What it's like in the real world |
|---|---|
| `app/` | The rooms of your house — each folder is a room (page) |
| `components/` | Furniture you move between rooms — build once, use everywhere |
| `public/` | Your photo album — images and files anyone can see |
| `lib/` | The pipes behind the walls — connects your app to the outside world |
| `.env.local` | A locked safe — holds your passwords and secret keys |
