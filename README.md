# Internship-test
## Internship test Connecthink - Carlos Leta Alfonso

In this github I have added all what I had to do for the Connecthink selection test.

For Part 1 of the jupyter notebook test I have uploaded the files:
- **test-scholar-data.ipynb**: jupyter notebook with all code and explanations.
- **Report_PandasProfiling.html**: report in html format with information from the dataset generated inside the jupyter notebook.

For Part 2 of the Interaction with Azure OpenAI and Dockerization test I have uploaded the **summarizer_app** folder, which includes the files for the text summarisation app, which are the following:
- **scripts.py**: python file with the functions implemented to connect to the Azure Open AI chat and make the summaries.
- **app.py**: python file to build the application with streamlit.
- **example_text.txt**, **example_text2.txt**, **example_text3.txt**: text files with content (more than 3 pages) to summarize.
- **Dockerfile**: file to build a docker image to dockerise the app.

To be able to run the app (with docker) the following steps must be taken:
- Download the github repository
- Enter through the terminal to the folder **summarizer_app**.
- Add an **.env** file (I have not added it for security reasons) in the folder **summarizer_app** with the variables **AZURE_OPENAI_ENDPOINT**, **AZURE_OPENAI_API_KEY** and **AZURE_OPENAI_DEPLOYMENT_NAME**, with their respective values.
- Build a docker image from the app's DockerFile with the following command: **'docker build -t image_app .'**   .
- Create and run a container from the created image with the following command: **'docker run -p 8501:8501 image_app'**   .
- Access the app by pasting the link **http://localhost:8501** in a web browser.

Once inside the app in the browser, it works as follows:
- There is a sidebar where we can add a text by clicking on **Browse files** and taking the text we want in the **summarizer_app** folder.
- Once loaded, click on **Add Data** to start summarising the text. If all goes well, you will see a message saying 'File uploaded, well chunked!'.
- Once the text has been summarised, you have the option to download the summary by clicking the **Download the summary** button.



