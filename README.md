# fde-project2-notebook-agentic-router
Implement agentic router with improved query routing and access control

1. Created a GitHub repo named fde-project2-notebook-agentic-router
2. Cloned this repo to a local folder
3. Committed the initial file for a baseline
4. Downloaded ipynb file from Hamza's repo to this folder
5. Renamed the file to Agentic_Router.ipynb
6. Run these commands to create a python virtual environment: 
    python3 -m venv .venv
    source .venv/bin/activate
    pip install ipykernel
    -prompt shows something like this which indicates it is running venv: 
    (.venv) yourname@Mac project %
7. Open the project folder in VS Code
8. Change from "Retricted Mode" to "Trusted Mode" in VS Code bottom left
9. Start updating ipynb 
10. Add .env to the project folder, not .venv
11. Add the following keys along with their values to .env
    OPENAI_API_KEY=
    SERP_API_KEY=
12. Create .gitignore file and add the following 
    .venv
    .env
13. Updated ipynb with addition pip installs for packages that are not on my laptop
14. loaded serp_api_key
15. Completed Step 1 and executed search based on SERP_API_KEY