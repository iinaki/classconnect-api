# ClassConnect API

### Virtual Environment for python development

Using a virtual environment means:

1. **Isolated Dependencies** – Each project has its own Python interpreter and installed libraries. You can install specific versions of packages without affecting other projects or the system Python.
2. **Avoids System Conflicts** – You don’t modify system-wide Python, which can prevent errors like the one you encountered (externally-managed-environment).
3. **Portability & Reproducibility** – Your project’s dependencies are recorded in a requirements.txt file, making it easy for others to recreate your environment.
4. **Better Project Management** – You can create multiple virtual environments for different projects, each with its own dependencies.

#### How to use

1. In your project folder, run: `python3 -m venv venv`. This creates a folder named venv containing a self-contained Python environment.
2. Activate the Virtual Environment, in Linux/macOS: `source venv/bin/activate`. Once activated, your terminal will show (venv) before the prompt, indicating you’re inside the virtual environment.
3. Install Packages Inside the Virtual Environment, like `pip install fastapi[all] sqlalchemy psycopg2 alembic pydantic dotenv pytest httpx`. These packages will be available only inside this environment.
4. After installing all packages, freeze them into a requirements.txt file: `pip freeze > requirements.txt`. Others can recreate your environment using: `pip install -r requirements.txt`.
5. When you’re done, exit the virtual environment with: `deactivate`.
