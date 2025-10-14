
##  **1. Introduction to `uv`**

### 🧠 What is `uv`?

**Simple Definition:**
`uv` is a **modern, fast tool** that helps Python developers manage:
* 🧩 **Projects** (folders and files)
* ⚙️ **Dependencies** (like libraries)
* 🌐 **Virtual environments** (Python environments)
* 🚀 **Packaging and running apps**



### 💡 Why we use `uv`?
Because it combines what `pip`, `venv`, and `poetry` do — **all in one tool**.
It is **super fast**, easy to use, and handles Python projects from setup to publishing.


<br>

## **B. Key Features of `uv`**
| Feature                       | Meaning (Simple Words)                                                     |
| ----------------------------- | -------------------------------------------------------------------------- |
| ⚡ **Speed**                   | `uv` is written in **Rust**, making it **much faster** than pip or poetry. |
| 📦 **Dependency Management**  | Installs and locks all required packages **in seconds**.                   |
| 🧰 **Virtual Environments**   | Automatically creates a **`.venv`** folder for each project.               |
| 📘 **pyproject.toml**         | Acts as the **main configuration file**, replacing `requirements.txt`.     |
| 🧠 **Python Version Pinning** | Ensures your project always uses the **same Python version**.              |
| 🚀 **Run Commands**           | Lets you **run scripts or apps directly** using `uv run`.                  |

<br>




## ⚙️ **C. UV Installation Guide**

Before using `uv`, you must have **Python** installed on your system.
Below are **step-by-step instructions** for installing Python on **Windows**, **macOS**, and **Linux**, followed by **UV installation**.


## 💻 **Python Installation (Step-by-Step for All OS)**


### 🪟 **Windows System**

#### ✅ Step 1: Download Python

🔗 Go to the official Python website:  
👉 [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/)

Click **"Download Python 3.x.x"** (latest version).


#### ✅ Step 2: Run the Installer

1. Double-click the downloaded `.exe` file.  
2. **Important:** Check the box ✅ **“Add Python to PATH”**  
3. Click **“Install Now”**


#### ✅ Step 3: Verify Installation

Open **Command Prompt** and type:

```bash
python --version
```

<br>

### 🍎 **macOS**

### ✅ Step 1: Use Homebrew (Recommended)

- First, install Homebrew (if not already installed):
```bash
- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```


Then install Python:
```bash
 brew install python
```

### ✅ Step 2: Verify Installation
```bash
python3 --version
```


### ✅ Expected Output Example:

Python 3.xx.x (latest version)

<br>

## 🐧 **Linux (Ubuntu / Debian-based)**
### ✅ Step 1: Update System
```bash
sudo apt update
```

### ✅ Step 2: Install Python
```bash
sudo apt install python3 python3-pip -y
```

### ✅ Step 3: Verify Installation
```bash
python3 --version
pip3 --version
```


### ✅ Expected Output Example:

Python 3.00.0 (latest version)
pip 24.00 (latest version)

<br>


## UV Package Manager Installation (All OS)


### 💻 **Windows**

* ✅ **Step 1:** Open PowerShell as Admin
* ✅ **Step 2:** Run Installation Script
  ```bash
  powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
  ```
  
* ✅ **Step 3:** Verify
  ```bash
  uv --version
  ```
  
<br>

### 🍎 **macOS**

* ✅ **Option 1:** Install via Homebrew
  ```bash
  brew install uv
  ```
  
* ✅ **Option 2:** Install via Script
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```
  
* ✅ **Step 3:** Verify
  ```bash
  uv --version
  ```
  

<br>

### 🐧 **Linux**

* ✅ **Step 1:** Install via Curl
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```
  
* ✅ **Optional:** If Needed, Add to PATH
  ```bash
  export PATH="$HOME/.local/bin:$PATH"
  ```
  
* ✅ **Step 2:** Verify
  ```bash
  uv --version
  ```
  
<br>




## **D. Steps to Create a Simple Application**

Let’s create a simple app called `my-simple-app`.



### 🧩 Step 1 — Create the Project

Run:

```bash
uv init my-simple-app
cd my-simple-app
```


**It creates:**


```
my-simple-app/
├── .gitignore
├── .python-version
├── main.py
├── pyproject.toml
└── README.md
```


🧠 Explanation:

* `.gitignore`: files to ignore in git
* `.python-version`: locks the Python version
* `main.py`: your main Python script
* `pyproject.toml`: your project’s configuration
* `README.md`: info about the project



### ⚙️ Step 2 — Create the Environment

Run:
```bash
uv sync
```


This command:

* Creates `.venv/` (virtual environment)
* Creates `uv.lock` (locks dependencies)

Now your project is fully ready to run in isolation.





### 🧑‍💻 Step 3 — Open in VS Code

Run:
```bash
code .
```


Then select:

> Command Palette → “Python: Select Interpreter” → choose `your environment`

Now VS Code knows which Python version to use.


### ✍️ Step 4 — Write Your Code

Open `main.py` and add:

```bash
def main():
    print("Hello from my-simple-app! — IB CODING SCHOOL")

if __name__ == "__main__":
    main()
```




### 🚀 Step 5 — Run the Application

Run directly using `uv`:

```bash
uv run python main.py
or
uv run main.py
```


**Output:**

Hello from my-simple-app! — IB CODING SCHOOL

<br>




## **E. Adding Packages**

Want to use an external library (like `openai-agents`)?
Just run:

```bash
uv add openai-agents
```


Now it’s automatically added to your `pyproject.toml`.



<br>

## **F. Quick Command Reference**



| Task               | Command                      |
| ------------------ | ----------------------------- |
| 🆕 Create new app  | `uv init my-simple-app`       |
| 🌱 Create environment | `uv sync`                  |
| ➕ Add dependency   | `uv add <package>`            |
| ▶️ Run file         | `uv run python main.py`       |



<br>


⭐ **Learn this complete course with video tutorials:**  
📺 [YouTube Channel — Illahi Bux](https://www.youtube.com/@illahibuxJ)


# The End