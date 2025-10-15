Perfect 👌 Here’s your **well-formatted `README.md`** version of the “Basic Agent” lecture — clean, attractive, and easy for students to read on GitHub or during your video.
I’ve added clear headings, highlights, and markdown styling for a professional look.

---

```markdown
# 🧠 OpenAI Agents SDK — Lecture 1  
## 🎯 Topic: Basic Agent Setup and First Program

Welcome to **Lecture #1** of the *OpenAI Agents SDK Full Course* by **IB Coding School**!  
In this lecture, we’ll learn how to **create your first AI Agent** using the **OpenAI Agents SDK** — step by step in a simple and easy way.

---

## 📂 Step 1: Setting Up a New Project

### 🪶 1. Create a new folder
Create a new folder for your project.  
Example:
```

basic_agent_project

````
Then open it in **VS Code**.

---

### ⚙️ 2. Initialize the project with `uv`
Open the terminal in VS Code and type:
```bash
uv init
````

✅ **Explanation:**

* This command creates a new **Python project** using `uv`.
* It also sets up a **virtual environment** automatically.
* The environment helps you manage project dependencies safely and separately.

---

### 📦 3. Install the OpenAI Agents SDK

Now install the required package:

```bash
uv add openai-agents
```

✅ **Explanation:**

* This installs the **OpenAI Agents SDK** in your project.
* You can see it added under dependencies in your `pyproject.toml` file.

---

### 🧩 4. Check if your environment is active

Make sure VS Code is using the same environment created by `uv`.

Go to:

> **Command Palette → “Python: Select Interpreter” → choose your environment**

---

## 💻 Step 2: Writing Our First Agent

Now create a new file named **`main.py`** and paste the following code 👇

```python
from agents import Agent, Runner
from dotenv import load_dotenv

load_dotenv()

my_agent = Agent(
    name="Assistant",
    instructions="You are a helpful Assistant"
)

my_prompt = "What is capital of Pakistan?"

my_result = Runner.run_sync(
    starting_agent=my_agent, input=my_prompt
)

print(f"\n{my_result.final_output}")
```

---

## 🔍 Step 3: Code Explanation (Line by Line)

### 🧩 Import Required Classes

```python
from agents import Agent, Runner
```

* **Agent** → Creates your AI assistant (the “brain”).
* **Runner** → Executes or runs the agent (the “engine”).

---

### 🔐 Import dotenv

```python
from dotenv import load_dotenv
```

* Used to **load secret keys** (like the OpenAI API key) from a `.env` file.
* Keeps your API key **secure** and out of your code.

---

### 📜 Load Environment Variables

```python
load_dotenv()
```

* Loads all variables from `.env` file into Python.
* Makes your API key accessible to the SDK.

---

### 🧠 Create Your Agent

```python
my_agent = Agent(
    name="Assistant",
    instructions="You are a helpful Assistant"
)
```

* Creates a new agent named **“Assistant”**.
* `instructions` define the **personality and behavior** of your agent.

  * Example: “You are a math expert” will make it act like a math tutor.

---

### 💬 Give a Prompt

```python
my_prompt = "What is capital of Pakistan?"
```

* This is the **question or task** you want your agent to handle.

---

### ⚙️ Run the Agent

```python
my_result = Runner.run_sync(
    starting_agent=my_agent, input=my_prompt
)
```

* This **executes** the agent using the `Runner`.
* `starting_agent` tells it which agent to use.
* `input` provides the question.
* The result (answer + trace) is stored in `my_result`.

🧩 *Note:*
**run_sync** means it runs step-by-step (synchronously) and waits for the result.

---

### 🖨️ Display the Result

```python
print(f"\n{my_result.final_output}")
```

* Prints the final response from the agent.
* `\n` adds a new line for cleaner output.

✅ **Example Output:**

```
The capital of Pakistan is Islamabad.
```

---

## 🧾 Step 4: Summary

✔️ We created a **new project** using `uv`
✔️ Installed the **OpenAI Agents SDK**
✔️ Activated our **virtual environment**
✔️ Wrote and executed our **first agent code**
✔️ Displayed the **agent’s response** successfully

---

## 🎉 Congratulations!

You’ve just built your **first OpenAI Agent** using the **Agents SDK**!
This is the foundation for everything we’ll build in upcoming lectures.

---

## 🚀 Next Lecture Preview

In the next video, we’ll explore:

> 🧩 **How to add Tools** to your Agent —
> so it can perform real actions like **searching**, **calculating**, or even **talking to other agents!**

Stay tuned and don’t forget to ⭐ **star** this repository if you found it helpful.

---

### 📺 Course by: **IB Coding School**

> *Subscribe on YouTube for full OpenAI Agents SDK course tutorials!*

```

---

Would you like me to add a **banner section with badges (Python, OpenAI, UV, VS Code)** at the top — to make your README look even more professional and GitHub-ready?
```
