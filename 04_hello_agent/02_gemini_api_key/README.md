
# 🧠 OpenAI Agents SDK

## 🎯  Basic Agent Setup with Google Gemini API Key



## Step 1: Add Your OpenAI API Key

Before running your agent, you need to provide your Google **Gemini API** key so the SDK can connect.

### 🧾 1. Create a .env file

Inside your project folder, create a new file named: **`.env`**

### 🔐 2. Add your API key

Open the .env file and add this line:
```bash
GEMINI_API_KEY=your_actual_api_key_here
```
Tips:
To Get API Key follow this Repo:
[03_get_api_keys](../../03_get_api_keys/)

### ⚠️ Important:

- Never share your API key publicly or upload .env to GitHub.
- Add .env to your .gitignore file to keep it private.


<br>

## 💻 Step 3: Writing Our First Agent

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

<br>

## 🔍 Step 4: Code Explanation (Line by Line)

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

* Loads all variables from `.env` file into your project.
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
* `instructions` define the **behavior** of your agent.

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

---

### 🖨️ Display the Result

```python
print(f"\n{my_result.final_output}")
```

* Prints the final response from the agent.



---

## 🧾 Step 5: Summary

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



### 📺 Course by: **IB Coding School**

> *Subscribe on YouTube for full OpenAI Agents SDK course tutorials!*

```

