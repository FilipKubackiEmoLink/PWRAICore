# 🚀 Project: AI Financial Analyst for Polish Companies 🇵🇱

Welcome, agents! Your mission, should you choose to accept it, is to build an awesome AI-powered tool from the ground up. We're going to take messy, real-world financial documents and turn them into pure, automated analytical gold.

This isn't just a coding exercise; it's a full-stack journey. We'll start with setting up a pro-level dev environment, wrestle with complex data, build a smart AI core, and finally, wrap it all up into a sleek, production-ready application. Let's build something cool! ✨

## 💾 Data Source 
I will add your emails and you will be able to download the data under this link:
https://drive.google.com/drive/folders/1OTZ184vuPtMygOEq6pEa09Y6CRm0ISOq?usp=sharing

---

## 🎯 Our Core Mission

1.  **💻 Build Like a Pro:** Set up and master a top-tier Python development workflow. No shortcuts!
2.  **📄 Tame the Data Chaos:** Create a rock-solid pipeline to rip tables out of messy PDFs and XHTML files.
3.  **✨ Structure & Supercharge:** Magically transform that raw data into clean, nested JSON and enrich it with crucial context.
4.  **🤖 Unleash the AI:** Use the power of LLMs to generate financial analysis that's actually smart and useful.
5.  **🚀 Go Live!:** Package our entire project into a real-world web application.

---

## Phase 0: The Sandbox - Explore & Experiment! Have fun, it matters!

Before we build the rocket ship, we need to play with the parts. This phase is all about getting your hands dirty, satisfying your curiosity, and understanding the battlefield. There are no wrong answers here—only discoveries. The goal is to explore the data, test out different tools, and start thinking about the challenges ahead.

**Your Playground Checklist:**

*   **🛠️ Tool Treasure Hunt:** The Python ecosystem is vast! Your first quest is to find the right tools for the job. Go explore libraries like `Beautiful Soup` and `lxml` for HTML/XHTML parsing. For the tricky PDFs, check out `pdfplumber`, `PyMuPDF`, or `camelot`. What are the pros and cons of each? How to handle documents' scans - check `dockling`?

*   **⚙️ From Slow to Pro:** Start by writing a simple script to loop through the files. Once that works, ask yourself: "How can I make this *faster*?" This is your invitation to explore the world of `multiprocessing` or `asyncio`. Can you make your computer do more than one thing at a time?

*   **⏳ Make it Feel Alive:** Nobody likes staring at a blinking cursor. Add some command-line magic with `tqdm` to create slick progress bars. It’s incredibly satisfying to watch your code churn through hundreds of files!

*   **🤖 Your AI Copilot:** You have a powerful personal tutor at your fingertips: AI assistants! Use them to brainstorm ideas, explain complex topics, or help you debug. But remember, they are the copilot, **you** are the pilot. Always trust your own intuition and understanding.

*   🚫 **The Golden Rule:** Never, *ever* blindly copy-paste code from an LLM. You will learn absolutely nothing. The real skill is understanding *why* the code works. Break it, fix it, and make it your own!

*   **🧠 Coder vs. Engineer:** Take a moment to think about this: What’s the real difference between *coding* and *software engineering*? One is about writing instructions; the other is about building reliable, scalable, and maintainable solutions. We're here to become engineers.

*   **🤝 Work Smart, Not Just Hard:** How will we organize our work? Let's chat about adopting a lightweight `SCRUM`-style workflow. Think short sprints, clear goals, and regular check-ins to keep everyone in sync and the project moving smoothly. Teamwork makes the dream work!
---

## Phase 1: The Foundation - Pro Setup 🛠️

First things first. A great project needs a great foundation. Before we even look at a single PDF, we're going to set up our environment like the pros do. This ensures our code is clean, reliable, and easy to work with.

**Your Checklist:**

*   **Dependency Guru (Rye):** We'll use `Rye` to handle all our Python packages and virtual environments. One `pyproject.toml` to rule them all!
*   **The Code Sheriff (Ruff):** `Ruff` will be our ultra-fast linter and formatter. It will keep our code looking sharp and consistent.
*   **Type Guardian (Mypy):** `Mypy` will be our static type checker to catch bugs before they even happen.
*   **The Gatekeeper (pre-commit):** We'll set up `pre-commit` hooks to automatically run all our checks. If the code ain't clean, it ain't getting committed!

**✅ Deliverable:** A perfectly configured repo where `rye lint` and `git commit` work flawlessly.

---

## Phase 2: The Data Heist - Extraction & Structuring 📊

Alright, time to get our hands dirty! This is where we tackle the main data challenge: pulling structured information from unstructured chaos.

**Your Data Drop:**
A ZIP file full of financial statements is waiting for you. Grab it, unzip it, and let the games begin!
➡️ [**LINK TO YOUR GOOGLE DRIVE / DATA SOURCE**]

*(**Pro-tip:** Unzip the data into a `data/` folder and add that folder to your `.gitignore`!)*

### Task 2.1: The Table Snatcher

Your first mission is to build a parser that can hunt down and extract tables from both PDF and XHTML files. These documents are wild and unpredictable, so your code needs to be tough and adaptable.

### Task 2.2: JSON Wizardry

Raw tables are... boring. Your job is to transform them into a beautifully structured, nested JSON format. Think about how financial statements are organized (sections, subsections, items) and design a schema that makes sense.

### Task 2.3: The Context Detective 🕵️

Often, a table of numbers has a tiny note somewhere saying "all figures in thousands of PLN". Your system needs to be smart enough to:
1.  Scan the document to find this crucial piece of text.
2.  Convert all the numbers to their *actual* value (e.g., `500` becomes `500,000`).

**✅ Deliverable:** A set of scripts that can chew through a folder of documents and spit out clean, normalized JSON files.

---

## Phase 3: The AI Brain - Intelligent Analysis 🤖🧠

Now for the really fun part. We have clean, structured data. It's time to plug it into an LLM and generate some serious insights.

**The Challenge:**
Your task is to build a module that uses an LLM to write a financial analysis report for a company. This report should be more than a simple summary; it should be insightful.

**Your AI needs two things:**
1.  All the historical data for one company.
2.  Data from other companies in the same industry for comparison.

**📈 The Final Report:**
The output should be a slick Markdown report that includes:
*   An "at-a-glance" summary.
*   Analysis of trends over time (are they growing or shrinking?).
*   Key financial ratios (what do the numbers *really* mean?).
*   A "Team A vs. Team B" style comparison against industry rivals.
*   Smart commentary on potential strengths and weaknesses.

**✅ Deliverable:** A Python module that takes a company name and generates an awesome, multi-page financial report.

---

## Phase 4: The Final Boss - Go Production! 🚀🐳

We've built the brain, now let's build the body. A standalone script is cool, but a real application is cooler. In this final phase, we'll wrap our entire project into a robust, scalable web service.

**The Tech Stack:**

*   **⚡ FastAPI:** We'll build a simple and lightning-fast API so that other services (or a future frontend!) can request an analysis.
*   **📦 Docker:** We'll containerize our entire application with Docker. This means it can run anywhere, anytime, without any "it works on my machine" drama.
*   **⏳ Celery:** Processing PDFs and running LLMs can be slow. We'll use Celery as a task queue to handle these heavy jobs in the background, so our API stays snappy.
*   **🤝 LLM Integration:** We'll make sure our LLM connection is robust, with proper error handling and configuration for a live environment.

**✅ Deliverable:** A fully "Dockerized" FastAPI application where you can request a financial analysis via an API endpoint and get the results.

---

## 👋 Meet the Crew & Ask for Help!

This is a team effort! If you get stuck, have a brilliant idea, or just want to chat about the project, reach out to your friendly neighborhood project leads.

*   **Kinga Kulewik** - `[kinga@email.com]` - The Boss 😎
*   **Filip Kubacki** - `filip.kubacki@emo-link.com` - Tech Lead / Mentor 🐮
*   **Uni Supervision** - `[uni.supervision@email.edu]` - The Big Brains 🧠

Don't hesitate to ask questions in our group chat or create an issue on GitHub. Let's learn and build together!