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
16. Completed Step 2 - Router Query function.
17. QUESTION 1: There is a cell with the command: 
                route_query("what is the revenue of uber in 2021?")
        Response: 
                {'action': '10K_DOCUMENT_QUERY',
                 'reason': "Asks for Uber's annual financial revenue",
                 'answer': "Uber's 2021 revenue was $17.5 billion"}
    I did not tie up the Qdrant data for 10K. How did the system respond with an answer?

    Since this command goes through OpenAI, did OpenAI fill the answer?
18. Step 3 - start
19. Added a git clone for the Qdrant repo since I did not run this in COLAB
20. Updated path to get qdrant data
21. Step 3 - completed. Loaded Qdrant data
22: Step 4 - start - build Retriever and RAG for vector databases
23. To fix compatibility issues of numpy versions with other libraries, I moved %pip install
    to the top of the Notebook
24. Completed Step 4
25. Completed Step 5
Note: Lesson learned: 
In Question 1, I asked whether OpenAI provided the "answer". Very likely it did.
The difference in that query vs the RAG query is that in RAG, the response also had a reference 
to the document from which it got the answer.
26. Start step 6 - setup users, roles and role permissions
27. Execute queries
28. Completed step 6
29. Assignment Part 1 - Sub-query Division - setup is done. 
30. Start Part 1 of implementation in 'def agentic_rag_multi'
31.     implemented 1: sub_queries
32.     implemented 2: agentic_rag on each sub_query
33. Re-wrote the logic - to be more defensive for JSON parsing
34. Instead of calling a pre-existing definition, the code explicitly queries for the route
35. added more validation and saved results to resultSet
36. Something is wrong. Restarting the kernel fixed it.