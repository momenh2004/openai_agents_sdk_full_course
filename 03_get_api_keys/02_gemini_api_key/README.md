## 🔑 Getting a Google Gemini API Key

Google provides access to powerful AI models like **Gemini 1.5 Pro**, **Gemini 1.5 Flash**, and others via the **Google AI Studio API**.  
Follow the steps below to create and configure your own **Gemini API key**.

---

## 🪜 Step-by-Step Guide

### 🧭 1. Sign Up or Log In
- Go to the **Google AI Studio**: [https://aistudio.google.com](https://aistudio.google.com)  
- Sign in using your **Google Account**.  
- Accept the **terms and conditions** if prompted.

---

### ⚙️ 2. Navigate to API Keys
- After signing in, click your **profile icon (top-right corner)**.  
- Select **“View API keys”** from the dropdown menu.  
- Or go directly to 👉 [https://aistudio.google.com/app/apikey](https://aistudio.google.com/api-keys)



---

### 🧩 3. Create a New API Key
- Click the **➕ "Create API Key"** button.  
- Choose the project (or use the default one if not created yet).  
- Once generated, **copy your API key** and **store it securely** — you **won’t be able to view it again!**

> 📸 *Example Page:*  
> ![](images/gemini_create_key.png)

---

### 🧰 4. Use Your API Key
You can now use your Gemini API key in your Python or Node.js applications.

#### 🐍 Example (Python)
```python
import google.generativeai as genai

genai.configure(api_key="YOUR_API_KEY_HERE")

model = genai.GenerativeModel("gemini-1.5-flash")
response = model.generate_content("Hello, Gemini!")
print(response.text)
