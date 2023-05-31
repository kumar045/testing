::page{title="Peer Review Assignment"}

<img src="/images/IDSN-logo.png" width="200" alt="cognitiveclass.ai logo"  />

##

Estimated time needed: **60** minutes

## Objectives

In this assignment you will:

-   Use the deep_translator python package for the translation.
-   Create a function that translates English to French.
-   Create a function that translates French to English.
-   Run coding standards check against the functions above.
-   Write unit tests to test the above functions.
-   Run unit tests and interpret the results.
-   Package the above functions and tests as a standard python package.

>**Important Notice** - Please keep in mind that sessions for this lab environment are not persisted. If you will not be completing the entire lab in one sitting, please save your code outisde of this environment, so you can resume your work without loss.

<details><summary><i>👉 Click here for instructions to save your code on github</i></summary>
Change to the project directory

```
cd /home/projects/xzceb-flask_eng_fr
```

Run these following commands replacing your github username and the email you use for loggin into github as appropriate.

```
git config --global user.email youremail@domain.com
git config --global user.name your_github_username

```

```
git add .
```

```
git commit -m"Temporary changes"
```

```
git push
```

</details>

## __Task1:__ Write a function that translates English text to French in translator.py

1. Open a terminal window by using the menu in the editor: Terminal > New Terminal.
<img src="images/new_terminal.png"  style="margin-top:10px; margin-bottom:10px"/>

2. Go to the project home directory.

    ```
    cd /home/project
    ```
    

3. Run the following command to Git clone the project directory from the clone URL you had copied in the prework lab.

    ```
    [ ! -d 'xzceb-flask_eng_fr' ] && git clone <paste_your_repo_name>
    ```
    

4. Change to the `final_project` folder.

    ```
    cd /home/project/xzceb-flask_eng_fr/final_project
    ```

5. Create folder named `machinetranslation` and change to that directory.

    ```
    mkdir machinetranslation
    cd machinetranslation
    ```

6. Run the following command to make sure that `python3` is using version 3.8.

```
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 10
```

7. Run the following command to check the python version.

```
python3 --version
```

>Note: It should be `Python 3.8.0`.

8. Install the packages that you will be using in this code, namely `deep_translator` and `Flask`.

    ```
    python3 -m pip install deep_translator
    python3 -m pip install Flask
    ```


9.  In the explorer, go to the `machinetranslation` directory and create a new file called `translator.py`. Enter the following line of code.

    ```
     from deep_translator import MyMemoryTranslator
    ```


>📷 Take a screenshot of your import statement and save it as a .jpg or .png with the filename `import_translator`.  You will be prompted to upload the screenshot in the Peer Assignement that follows.

10. Add function **englishToFrench** which takes in the `englishText` as a string argument, in `translator.py`. Use the instance of the MyMemory Translator you imported previously, to translate the text input in English to French and return the French text.

    ```python
    def englishToFrench(englishText):
        #write the code here
        return frenchText
    ```


📷 Take a screenshot of your functions and save it as a .jpg or .png with the filename `e2f_translator_function`.  You will be prompted to upload the screenshot in the Peer Assignement that follows.

11. Add function **frenchToEnglish** which takes in the `frenchText` as a string argument, in `translator.py`. Use the instance of the MyMemory Translator you imported previously, to translate the text input in French to English and return the English text.

    ```python
    def frenchToEnglish(frenchText):
        #write the code here
        return englishText
    ```


> 📷 Take a screenshot of your functions and save it as a .jpg or .png with the filename `f2e_translator_function`.  You will be prompted to upload the screenshot in the Peer Assignement that follows.

::page{title="__Task 2:__ Write the unit tests for English to French translator and French to English translator function  in tests.py"}

1. Create a new file called `tests.py` in the `machinetranslation` directory.
2. Write at least 2 tests in `tests.py` for each method
3. Test for the translation of the word 'Hello' and 'Bonjour'.
4. Test for the translation of the word 'Bonjour' and 'Hello'.
5. Take a screenshot of your unit tests and save it as a .jpg or .png with the filename `translation_unittests`.

::page{title="__Task 3:__ Check your code against python coding standards"}

1. At the terminal run the following command to install pylint.
    ```
    python3 -m pip install pylint
    ```

2. Run `pylint translator.py` to check the coding standard compliance in your code. Refer to this [exercise](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0222EN-SkillsNetwork/labs/module%206/Lab%20-%20Static%20Code%20Analysis/Static_Code_Analysis.md.html) you did earlier, if needed.
3. Make sure your rating is at least 7.
4. 📷 Take a screenshot of the output of the pylint analysis report showing your score and save it as a .jpg or .png with the filename `pylint_score`.

::page{title="__Task 4:__ Run tests"}



1. At the terminal run the command
    ```
    python3 tests.py
    ```
    

2. 📷 Take a screenshot of test results and save it as a .jpg or .png with the filename **unit_test_results**.

::page{title="__Task 5:__ Package the above functions and tests as a standard python package."}

1. Create `__init__.py` file in the directory `machinetranslation`.

2. Create a folder called `tests` under the newly created folder

3. Copy the unit `tests` into the tests folder

>📷 Take a screenshot of the folder structure of the package ( From the menu go to View -> Explorer to set the explorer view) and save it as a .jpg or .png with the filename `package_folder_structure`.

::page{title="__Task 6:__ Import the package into server.py and create flask end points"}

1. Import the package `machinetranslation` in server.py.

2. In the server.py, for end-point `/`, implement a method that renders the `index.html`.

3. In the space provided in server.py for end-point `/englishToFrench` implement a method that uses the appropriate translation function through the package you created in the previous part. The function should take the English text as input through the request parameter and return a string.

4. In the space provided in server.py for end-point `/frenchToEnglish` implement a method that uses the appropriate translation function through the package you created in the previous part. The function should take the French text as input through the request parameter and return a string.

5. Push the code to GitHub.
<details><summary><i>👉 Click here for instructions to push your code to github</i></summary>Change to the project directory

```
cd /home/projects/xzceb-flask_eng_fr
```

- Run these following commands replacing your github username and the email you use for loggin into github as appropriate.

```
git config --global user.email youremail@domain.com
git config --global user.name your_github_username

```

```
git add .
```

```
git commit -m"Final changes"
```

## Task - Generate Personal Access Token

- 	Verify your email address if it hasn’t been verified on Github.

-	In the upper-right corner of any page, click your profile photo, then click Settings.
	
	![](/images/Settings.png)


-	In the left sidebar, click Developer settings.
	
	![](/images/Developers%20setting.png)



-	In the left sidebar, click drop-down menu `Personal access tokens`.

![](/images/Personal%20token.png)
	
   
-	Click on `Token (classic)` and then click drop-down menu `Generate new token` and click `Generate new token (classic)`.
	
![](/images/Personal%20token2.png)
	
	

-	Give your token a descriptive name. To give your token an expiration, select the Expiration drop-down menu, then click a default or use the calendar picker. Select the scopes, or permissions, you'd like to grant this token. To use your token to access repositories from the command line, select repo.
	
	![](/images/repo.png)



-	Click `Generate token` and make a note of it.

![](/images/Generate%20token.png)
	
-  Make sure you copy the token and keep it safe. It is not visible to you again.

<img src="images/copy_token.png" style="margin-left:30px;margin-top:10px;margin-bottom:10px;width:75%;border: solid 1px grey"/>

>**Treat your tokens like passwords and keep them a secret.**

>Once you have a token, you can enter the Personal Access Token as password when performing Git operations.

>The git `push` command will enable you to sync all the changes made locally to the GitHub web repository.

- Run the following command with your actual HTTPS link:

    ```
    git push [HTTPS link]
    ```
    

    You will be prompted by git for your username and password.

- Type your GitHub username and for the password, enter the personal access token you generated in the previous task. When you are authenticated, all committed changes are synced with your GitHub repository.

You can now visit the GitHub repository page and check to ensure that the revised and newly added files are in place.

</details>

::page{title="__Task 7:__ Run the server"}

1. Change to the project directory and run the server from your terminal.

```
cd /home/project/xzceb-flask_eng_fr/final_project && python3 server.py
```

2. You will see that the server starts up in port 8080.

3. Click on the `Skills Network button` on the left, it will open the `Skills Network Toolbox`. Then click the `Other` then `Launch Application`. 
From there you should be able to enter the port.

<img src="images/Launch app.png" style="border: solid 1px grey"/>

Connect to port `8080`and click `Launch` button.

<img src="images/launch 1.png" style="border: solid 1px grey"/>

4. A new browser window opens up with the index page.
    - 📷 Take a screen shot of the translation from English to French
    - 📷 Take a screen shot of the translation from French to English

 <!--::page{title="__Task 8:__ (Optional) Deploy the application on IBM Cloud."}

>Note : This will only work if Cloud Foundry is available.

1. Change to the `final_project` directory.

    ```
    cd /home/projects/xzceb-flask_eng_fr/final_project
    ```
    

2. Login to the ibmcloud with your email and enter your password when prompted.

    ```
    ibmcloud login -u <your email>
    ```
    

3. Set the target region and owner. Run the followinf command after you  replace `REGION` with your region and the `OWNER` with your email id.

    ```
    ibmcloud target --cf-api https://api.REGION.cf.cloud.ibm.com -r REGION -o OWNER
    ```
    

4. Create an account space called `translator`.

    ```
    ibmcloud account space-create translator
    ```
    

5. Target the account space you just created.

    ```
    ibmcloud target -s translator
    ```
    

6. Replace line 3 in the `manifest.yml` to give a name for your web application.

7. Deploy the application.

    ```
    ibmcloud app push
    ```
    

8. The route for your web application will be printed on the screen. Copy it to connect to it after the application successfully deploys.

    <img src="images/deploy_app.png" style="margin-top:10px;margin-bottom:10px"/>

    >Troubleshoot: You can check the logs by running, `ibmcloud cf logs <appname> --recent`

9. You can see your deployed application listed in the [Cloud Foundry](https://cloud.ibm.com/cloudfoundry/public). To make changes and push your app again, stop and delete the application from [Cloud Foundry](https://cloud.ibm.com/cloudfoundry/public) and then execute `ibmcloud app push`. -->



::page{title="__Task 8:__ Deploy the application on Code Engine."}

1. Change to the `final_project` directory.

    ```
    cd /home/project/xzceb-flask_eng_fr/final_project
    ```
  > ### Note: 
  > - Make sure `Task 7: Run the servers` runs successfully.
  > - In `requirements.txt` file, delete the package versions and it should look as shown below:
  ![](/images/Image.png)
  

2. Let’s create a Dockerfile in your project directory. Dockerfile is the blueprint for building a container image for our app. 
    
  ![](/images/Image%201.png)



3. Create `Dockerfile` and add the following lines to your file:

    ```
    FROM python:alpine3.7
    COPY . /app
    WORKDIR /app
    RUN pip install -r requirements.txt
    EXPOSE 8080
    ENTRYPOINT [ "python" ]
    CMD [ "server.py" ]
    ```

  On the first line we are importing the Docker image `python:alpine3.7` which comes with support for Python 3. This image allows us to create Flask web applications in Python that run in a single container. We are interested in the latest version of this image available, which supports Python 3.

  On the next 2 lines, we are opening port 8080 to usage in the docker container. This will allow us to access our application later once it’s deployed to the cloud.

  Finally, we copy the contents of the final_project directory we just created, into an app directory in the container image. Pretty easy, right!

  You should have a directory structure like this:
   
  ![](/images/Image%202.png)
 

4. On the menu in your lab environment, click `Skills network tools`; Click Cloud dropdown and choose `Code Engine`. The code engine set up panel comes up. Click `Create Project`.

 ![](/images/Image%203.png)

    

5. The code engine environment takes a while to prepare. You will see the progress status being indicated in the set up panel.


6. Once the code engine set up is complete, you can see that it is active. Click on `Code Engine CLI` to begin the pre-configured CLI in the terminal below.

   ![](/images/Image%204.png)

You will now use the CLI to deploy the application.

7. Change to the app directory where the Dockerfile was created.


    ```
    cd /home/project/xzceb-flask_eng_fr/final_project
    ```

8. Now run `docker build` in the app directory and tag the image. Note that in the below command we are naming the app `flask-docker-demo-translator`.

    ```
    docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/flask-docker-demo-translator
    
    ```
   ![](/images/Image%205.png)

9. Now push the image to the namespace so that you can run it.

    ```
    docker push us.icr.io/${SN_ICR_NAMESPACE}/flask-docker-demo-translator:latest
    ```
    ![](/images/Image%206.png)

10. Deploy the application.

    ```
    ibmcloud ce application create --name flask-docker-demo-translator --image us.icr.io/${SN_ICR_NAMESPACE}/flask-docker-demo-translator --registry-secret icr-secret

    ```
   ![](/images/Image%207.png)

> Please note this command will run only in a Code Engine CLI. If you didn’t follow the steps 4 to 7 to start the Code Engine CLI, you may get errors.

11. Press ctrl(Windows)/cmd(Mac) and the link that is created. Alternatively copy the link and paste it in a browser page and press enter. The `flask-docker-demo-translator` application page renders as given below.

![](/images/image%208.png)



::page{title="Congratulations!"}

You have completed the tasks for this project. In the peer assignement that follows, you will be required to upload the screenshots you saved in this lab.

## Authors

Lavanya

### Other Contributors

Ramesh Sannareddy

## Change Log

| Date (YYYY-MM-DD) | Version | Changed By        | Change Description                 |
| ----------------- | ------- | ----------------- | ---------------------------------- |
| 2021-05-14        | 1.0     | Lavanya | Created initial version of the lab |
| 2022-09-01 | 2.0 | Ratima | Updated screenshot and step of Lauch Application|
| 2022-09-23 | 2.1 | Ratima | Updated instruction|
| 2022-10-21 | 2.2 | Ratima | Updated Skill Network Logo screenshot|
| 2022-12-16 | 2.3 | Ratima | Updated instruction|
| 2023-03-21 | 2.4 | Ratima | Updated Task 8|
| 2023-06-01 | 2.5 | Shivam | Updated Translator|

 Copyright © 2020 IBM Corporation. All rights reserved.

