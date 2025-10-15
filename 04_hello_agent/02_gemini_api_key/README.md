
# 🧠 OpenAI Agents SDK

## 🎯  Basic Agent Setup with Google Gemini API Key (Free)



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
[Get Gemini Key](../../03_get_api_keys/02_gemini_api_key/)

### ⚠️ Important:

- Never share your API key publicly or upload .env to GitHub.
- Add .env to your .gitignore file to keep it private.


<br>

## 💻 Step 3: Writing Our First Agent

Now create a new file named **`main.py`** and paste the following code 👇

```python
from agents import Agent, Runner, OpenAIChatCompletionsModel, set_tracing_disabled
from openai import AsyncOpenAI
from dotenv import load_dotenv
import os

load_dotenv()
set_tracing_disabled(disabled=True)

my_api_key = os.getenv("GEMINI_API_KEY")

my_clinet = AsyncOpenAI(api_key=my_api_key, base_url="https://generativelanguage.googleapis.com/v1beta/openai/")

my_model = OpenAIChatCompletionsModel(model="gemini-2.5-flash", openai_client=my_clinet)

my_agent = Agent(
    name="Assistant",
    instructions="You are a helpful Assistant",
    model=my_model
)

my_prompt = "What is capital of Pakistan?"

my_result = Runner.run_sync(
    starting_agent=my_agent, input=my_prompt
)


print(f"\n{my_result.final_output}")
```
---
<br>

## 🧩 Step-by-Step Code Explanation

### 1️⃣ Import Required Libraries

```python
from agents import Agent, Runner, OpenAIChatCompletionsModel, set_tracing_disabled
from openai import AsyncOpenAI
from dotenv import load_dotenv
import os
```

* **Agent** → Creates your AI assistant (the brain).
* **Runner** → Runs or executes the agent.
* **OpenAIChatCompletionsModel** → Allows you to use any OpenAI-compatible model (like Gemini).
* **set_tracing_disabled** → Turns off tracing (optional; makes execution faster).
* **AsyncOpenAI** → Helps connect with OpenAI or any compatible API (like Gemini).
* **load_dotenv** → Loads secret keys from `.env` file.
* **os** → Used to access environment variables in Python.

---


### 2️⃣ Load Environment Variables

```python
load_dotenv()
```

This loads the `.env` file where your API key is saved.

Example of `.env` file:

```
GEMINI_API_KEY=your_gemini_api_key_here
```

---

### 3️⃣ Disable Tracing (Optional)

```python
set_tracing_disabled(disabled=True)
```

This line **turns off tracing**, which is useful if you don’t want detailed logs or analytics.
You can skip this if you prefer default tracing behavior.

---

### 4️⃣ Get API Key from Environment

```python
my_api_key = os.getenv("GEMINI_API_KEY")
```

* Fetches the **Gemini API key** from your `.env` file securely.
* Keeps your key hidden from public code.

---

### 5️⃣ Create Gemini Client

```python
my_clinet = AsyncOpenAI(api_key=my_api_key, base_url="https://generativelanguage.googleapis.com/v1beta/openai/")
```

* Connects to **Gemini’s API endpoint**.
* Uses `AsyncOpenAI` because Gemini API is **OpenAI-compatible**.
* `base_url` changes the default OpenAI endpoint to Gemini’s URL.

---

### 6️⃣ Define the Model

```python
my_model = OpenAIChatCompletionsModel(model="gemini-2.5-flash", openai_client=my_clinet)
```

* Tells the SDK which **Gemini model** you want to use.
* Here we’re using **`gemini-2.5-flash`** — a fast and efficient model.
* `openai_client` links this model to the Gemini API connection.

---

### 7️⃣ Create the Agent

```python
my_agent = Agent(
    name="Assistant",
    instructions="You are a helpful Assistant",
    model=my_model
)
```

* Creates a **custom AI agent** using the Gemini model.
* The `instructions` define how the assistant should behave.

---

### 8️⃣ Add a Prompt

```python
my_prompt = "What is capital of Pakistan?"
```

* This is the question or command for your agent.

---

### 9️⃣ Run the Agent

```python
my_result = Runner.run_sync(
    starting_agent=my_agent, input=my_prompt
)
```

* Runs the agent and waits for its response.
* The output (answer) is stored in `my_result`.

---

### 🔟 Print the Final Output

```python
print(f"\n{my_result.final_output}")
```

* Displays the final response from the Gemini model.

✅ **Example Output:**

```
The capital of Pakistan is Islamabad.
```

---

## 🧾 Summary

✔️ Added Gemini API key in `.env` file

✔️ Connected Gemini API using `AsyncOpenAI`

✔️ Used `OpenAIChatCompletionsModel` for Gemini models

✔️ Created and ran an agent successfully

---


---

## 🎉 You Did It!

Now your **OpenAI Agents SDK** project is successfully connected to **Google Gemini models**.
This lets you build **AI Agents** powered by Gemini’s intelligence — fast, secure, and simple.

---

### 📺 Course by: **IB Coding School**

> *Subscribe on YouTube for more practical lectures on the OpenAI Agents SDK full course.*

```

---



