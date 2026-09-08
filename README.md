# LangChain   

<details> ​Welcome to this demonstration on setting up virtual environment and configuring API keys. ​In this walkthrough, we'll go step by step through creating a project folder, setting ​up a virtual environment, installing required packages using a requirements.txt file, configuring ​environment variables, and finally running a Python code that uses lang chain, Gemini ​and .env. ​By the end of this demo, you'll have a clean Python virtual environment, a working code, ​and a secure way to handle API keys without exposing them in your source code. ​Let's begin. ​Let's begin inside Visual Studio Code. ​I've already created a folder on my machine called Environment Setup, and now I'm going ​to open it as a project. ​From the top menu, I choose File, then Open Folder, browse to the Environment Setup folder ​and open it. 
​It's important that we open the entire folder, not just a single Python file. ​It can detect virtual environments, apply the correct Python settings, and manage extensions ​and imports properly. ​Think of the folder as the home base that VS Code uses to understand your project. ​With the folder open, we're ready to create our first code file. ​In the Explorer panel on the left, I click New File and name it Test File. ​This file is going to be our test script. ​We'll use it later to confirm that our virtual environment is active, our libraries are installed ​correctly, and our environment variables, like the Gemini AP key, are being loaded properly. 
​For now, I'm going to leave this file empty. ​Before we write any code, we need to make sure our terminal environment is configured ​correctly inside VS Code. ​One of the most important steps in this demo is choosing the right terminal. ​VS Code often defaults to PowerShell, and PowerShell can block virtual environment activation ​because of execution policies. ​To avoid that problem, we explicitly switch to Command Prompt. ​At the top, I open the Terminal menu and choose New Terminal. ​Once the terminal appears, I click the little drop-down arrow next to the plus icon and ​select Command Prompt. 
​Now, at the bottom of the window, you should see something like Path of the file. ​That tells us we're in the Environment Setup folder and using Command Prompt, which is ​exactly what we want for this setup. ​With our terminal ready, we can create the virtual environment. ​In the Command Prompt terminal, I type python-mv nvnv1 and press Enter. ​This command creates a new folder called env1 inside the Environment Setup directory. ​That folder is a self-contained Python environment. ​It has its own Python interpreter, its own pip, and its own site packages directory for ​installed libraries. 
​The big advantage here is isolation. ​Whatever you install in env1 stays inside this project and doesn't interfere with other ​projects or your global Python installation. ​This is especially important when you work with fast-moving AI libraries like LangChain, ​where different projects might depend on different versions. ​Now that the environment exists, we need to tell VS Code to use it. ​To do that, we select the Python interpreter that lives inside env1. ​I press Ctrl plus Shift plus P to open the command palette and start typing Python. ​Select Interpreter. 
​When that option appears, I select it. ​VS Code now shows me a list of available Python interpreters. ​Among them, I look for the one that points to our new environment. ​I click that. ​From this moment on, when VS Code runs Python code, formats it, or installs tools using ​its integration, it will use the interpreter from env1. ​This keeps everything consistent. ​We've told VS Code which interpreter to use, but we also need to activate the environment ​in the terminal itself. 
​Back at the bottom terminal, which is still in the environment setup folder, I run env1 ​slash scripts slash activate after pressing enter. ​The prompt changes to include the name of the environment at the beginning. ​You'll see something like... ​That little env1 prefix is your visual indicator that the virtual environment is active. ​From now on, every time we run Python or pip in this terminal, those commands will operate ​inside env1, not on the system-wide Python installation. ​This is exactly what we want. ​Next, we'll declare the libraries we need using a requirements.txt file. 
​In the project root, right next to test file and the env1 folder, I create a new file called ​requirements.txt. ​Inside that file, I type the names of the packages we'll be using. ​These three packages are the core of our demo. ​LangChain gives us the workflow engine and abstractions for building chains. ​LangChain, Google Gen AI, provides integration with Google's Gemini models. ​And Python.env lets us load secrets, like API keys, from a .env file without hard-coding ​them in our source code. ​Listing them in requirements.txt means anyone who wants to reproduce this project can do ​so with a single command. 
​With the requirements file ready and our env1 environment active, we can now install our ​dependencies. ​In the same terminal, I simply run pip install-r requirements.txt pip reads the file, downloads ​each library, and installs everything directly into our virtual environment. ​Once this completes without errors, our setup is ready. ​Now we switch back to test file and paste in the test code. ​The purpose of this script is straightforward. ​It verifies that our environment variables, dependencies, and Gemini integration are all ​working properly. ​The code begins by calling load.env, which loads values from our .env file. 
​Let's run it. ​Back in the env1 terminal, I run python test.py. ​It prints the banner message and waits for your question. ​For example, if I ask, how should I design a microservice architecture for an e-commerce ​platform? ​The pipeline sends this to Gemini and returns response outlining services, API, and communication ​patterns. ​Seeing this output confirms that the environment is active, the interpreter in VS Code is using ​the correct Python source, the library is installed correctly, the .env file loaded ​successfully, and Gemini is responding through lang chain. ​That's all about this demonstration. 
​Thank you, and see you in the next video. </details>

# 02 Preparing a Modern AI Development Environment
https://www.coursera.org/learn/building-your-first-ai-agent-with-langchain/lecture/jdBIZ/preparing-a-modern-ai-development-environment
step in Python and environment configuration helps isolate project dependencies to avoid conflicts?


Setting up virtual environments for the project. 
<img width="806" height="358" alt="image" src="https://github.com/user-attachments/assets/fbfebd7b-88d7-4761-88e2-798d4caf5cfa" />

<img width="909" height="381" alt="image" src="https://github.com/user-attachments/assets/7822ac7a-41a7-4f70-94b3-d81c2c1f39c8" />

 ## Demonstration: Gemini API Key Setup with AI Studio
 <img width="920" height="412" alt="image" src="https://github.com/user-attachments/assets/826d04b9-5a64-4e16-a97c-2d5e31a4b5c6" />

 # Demonstration: Setting up Virtual Environment and Configuring API Keys

 ## creat folder 📂 for project files
 <img width="899" height="401" alt="image" src="https://github.com/user-attachments/assets/b7440423-2637-4425-a4b0-74e5a8aa7ef7" />

 test.py  in # drive c 

 ## we have activate the cmd   by default it use power shell    
 1>   click ...  on left side of "Run"   open New Terminal

 <img width="892" height="406" alt="image" src="https://github.com/user-attachments/assets/b2fa67de-6e73-4010-941d-5a6af62f8f06" />
## pratical
``` python -m venv env1
```

<img width="1862" height="673" alt="image" src="https://github.com/user-attachments/assets/0a854f83-17ae-48d6-bff2-b33c29567406" />

## Question
<img width="1310" height="420" alt="image" src="https://github.com/user-attachments/assets/51c1c6dc-d33a-4f90-bf15-e5956c4cbbef" />

press  CTRL + SHIFT + P    TO OPENT THE Python  interpreter   >> scroll down to select   >  than select that env1 

<img width="1513" height="725" alt="image" src="https://github.com/user-attachments/assets/80e20505-f230-4a2f-b953-cc146104d1b9" />

## activate the env1   
>>>  Source 
<img width="1531" height="851" alt="image" src="https://github.com/user-attachments/assets/d8a202fa-8c4f-4e0e-85d9-a88635f7f228" />
>>>  Paractial
<img width="650" height="385" alt="image" src="https://github.com/user-attachments/assets/3b49322e-9735-4a23-8b62-2f692ad33508" />


>>>  Creat and Install  the Requirements Variables
 <img width="1536" height="851" alt="image" src="https://github.com/user-attachments/assets/2c08609f-aaa4-49c4-80e4-409d76252863" />

 ## command  
  langchain
  langchain-google-genai
  python-dotenv

  pip  install -r  requirements.txt

  ```
from dotenv import load_dotenv
from langchain_google_genai import ChatGoogleGenerativeAI
from langchain_core.prompts import ChatPromptTemplate
import os
I
def build_char()
#Load environment variables from.env
load_dotenv()
#Gemini API key is read from GOOGLE_API_KEY env var
api_key os.getenv("GOOGLE_API_KEY")
if not api_key:
raise ValueError("GOOGLE_API_KEY not found in environment/.env")
11m ChatGoogleGenerativeAI(
)
model-"gemini-2.5-flash",
temperature-0.4,
google_api_key-api_key, optional if it's already in env, but explicit is clear
prompt Chat PromptTemplate.from_messages(
[
(
"system",
(
"You are a senior software architect helping developers make
"good technical decisions. Be concise, practical, and specific.
"Focus on architecture, tools, trade-offs, and best practices."
),
"human",
(
"Developer question:\n"
"{question}\n\n"
"Answer for an experienced tech audience.
"Use short paragraphs and bullets when helpful."
),    ```









 




