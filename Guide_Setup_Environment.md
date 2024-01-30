### Quickstart Guide: Setting Up a Python Flask Development Environment

#### 1. Install Visual Studio Code (VS Code)
- **Download**: Go to the [VS Code website](https://code.visualstudio.com/) and download the installer for your operating system.
- **Install**: Run the installer and follow the on-screen instructions.
- **Verify**: Open VS Code to ensure it's installed correctly.

#### 2. Install Python
- **Download**: Visit the [Python website](https://www.python.org/downloads/) and download Python 3.12.
- **Install**: Run the installer. Ensure you check the option to "Add Python 3.12 to PATH" (environment variables).
- **Verify**: Open a command prompt or terminal and type `python --version` to check if Python is installed.

#### 3. Install Anaconda
- **Download**: Go to the [Anaconda website](https://www.anaconda.com/products/individual) and download Anaconda for Python 3.11.
- **Install**: Execute the installer and follow the instructions.
- **Create Virtual Environment**:
   - Open the Anaconda Prompt and type:
     ```bash
     conda create -n flask_env python=3.12
     ```
   - Activate the environment:
     ```bash
     conda activate flask_env
     ```

#### 4. Install Required Libraries
- **Pandas, Numpy, Flask, OpenAI, and ChromeDB**:
  - In the virtual environment, run:
    ```bash
    pip install pandas numpy flask openai chromadb jupyter ipykernel
    ```

#### 5. Install plugins in VS Code
- **Install Jupyter Plugin**:
  - Open VS Code.
  - Go to Extensions (sidebar) and search for "Jupyter".
  - Install the Jupyter extension.

- **Install Git Plugin**:
  - Go to Extensions and search for "Git".
  - Install the Git extension.

- **Install Python Plugin**:
  - Go to Extensions and search for "Python".
  - Install the Python extension.


#### 6. Verify Installation
- Create a simple Python file in VS Code and try creating a jupyter notebook (`test.ipynb`), using `flask_env` as a kernel, and importing Flask, Pandas, etc., to ensure everything is installed correctly.

#### 7. Starting Your First Flask Project
- **Create a New Folder** for your project and open it in VS Code.
- **Create a New Python File** (e.g., `app.py`) in the folder.
- **Write a Basic Flask App**:
  ```python
  from flask import Flask
  app = Flask(__name__)

  @app.route('/')
  def hello_world():
      return 'Hello, World!'

  if __name__ == '__main__':
      app.run(debug=True)
  ```
- **Run Your Flask App**:
  - Open a terminal in VS Code.
  - Ensure your virtual environment is active.
  - Run the command `python app.py`.
  - Open a web browser and go to `http://127.0.0.1:5000/` to see your Flask app.
