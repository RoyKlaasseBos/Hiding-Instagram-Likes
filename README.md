# Hiding Likes on Instagram 
### Goodbye Likes, Hello Mental Health - How Hiding Like Counts Affects User Behavior and Self-Esteem

<p style="clear: both;">This repository contains supplemental material associated with my <a href="https://github.com/RoyKlaasseBos/Hiding-Instagram-Likes/blob/master/2020_08_19_Research_Master_Thesis_RJ_Klaasse_Bos.pdf">research master thesis</a>. Specifically, the online appendix describes the methods associated with the observational study and experiment. On a conceptual level we investigate the effect of hiding like counts on Instagram on users' posting frequency (H1), variety of visual-content (H2), like behavior (H3), and self-esteem (H4).</p>

<img src="https://raw.githubusercontent.com/RoyKlaasseBos/Hiding-Instagram-Likes/master/images/conceptual_model.jpg" alt="Conceptual model" width=750px />

## Web Appendix
The online appendix has been split up in two parts. The first part <a href="https://github.com/RoyKlaasseBos/Hiding-Instagram-Likes/blob/master/Web_Appendix_Data_Collection_Preparation.ipynb">Data Collection & Preparation</a> describes the seeding strategy (A), consumer account selection and screening (B), scraping process (C), computer vision API usage (D), image similarity computations (E), outlier screening (F), and propensity score matching (G). The second part <a href="https://github.com/RoyKlaasseBos/Hiding-Instagram-Likes/blob/master/Web_Appendix_Data_Analysis.ipynb">Data Analysis</a> then deploys various difference in difference models (H) on this data set and analyzes the results of the experiment (I).

## Data Description
We built on an observational data set scraped from Instagram (July 2020) and an experimental dataset obtained through a questionnaire on Prolific (N=600). Preprocessing of the raw data is documented in a step-by-step fashion in the appendix. Definitions and descriptions are outlined over <a href="https://github.com/RoyKlaasseBos/Hiding-Instagram-Likes/blob/master/Data_Set_Description.ipynb">here</a>. All data can be accessed through a relational database service. Attached online appendix refers to multiple environment variables in order to connect to the database (see instructions below). Credentials can be acquired by contacting one of the authors.

## Running Instructions
### Configure Environment Variables
Just like you sign in to Google Drive using your email and password credentials, we need to log in to our relational database using a database URL (`INSTAGRAM_DB_URL`) and database key/password (`INSTAGRAM_DB_KEY`) (available upon request). The idea is that we store these variables on our local machine without hardcoding them into our notebook. Below we briefly describe how to configure these environment variables. Alternatively, watch one of these tutorials ([Mac/Linux](https://www.youtube.com/watch?v=5iWhQWVXosU) & [Windows](https://www.youtube.com/watch?v=IolxqkL7cD8)). 

*Mac / Linux*
1. Go to the terminal and type `printenv` to list all environment variables stored on your machine. 
2. Assuming that `INSTAGRAM_DB_URL` and `INSTAGRAM_DB_KEY` are not listed there yet, we're going to define these two new variables. Open the terminal, go to your user directory (shortcut: `cd ~`), and type `nano .bash_profile` to open a text editor in the terminal. 
3. Within this window you can create new variables as follows: `export [VARIABLE_NAME]="the string value you want to store";` (e.g. `INSTAGRAM_DB_URL="http://anotherurl.com"`). Note that there is no space between the variable name and its value and that the string is enclosed in double quotes. Using this approach create a `INSTAGRAM_DB_URL` and `INSTAGRAM_DB_KEY` variable (you can list them below one another in the same file).
4. Exit the editor by pressing Ctrl + X, choose `Y` (to save changes), and finally press `Enter`. 
5. You can check whether everything worked out correctly by restarting your terminal and typing `printenv` (`INSTAGRAM_DB_URL` and `INSTAGRAM_DB_KEY` should be listered there now!). If the new envirionment variables didn't show up, you may need to use `nano .zshrc` instead of `nano .bash_profile` (see step 2).

*Windows*
1. Open up "Control Panel" > "System and Security" > "System".
2. In the left sidebar click on "Advanced system settings".
3. Click on "Environment Variables" in the bottom right.
4. Create a new "User Variable" (top list) and fill out the "Variable name" and "Variable value" (`INSTAGRAM_DB_URL` and `[DB_URL]`, respectively).
5. Repeat the same for the secret `INSTAGRAM_DB_KEY` and double click "OK" twice.

### Required Software Packages
* <a href="https://www.anaconda.com/products/individual">Anaconda & Jupyter Notebook</a>
* <a href="https://pypi.org/project/psycopg2/">psycopg2</a> (Python)
* <a href="https://pypi.org/project/rpy2/">rpy2</a> (Python)
* <a href="https://www.rdocumentation.org/packages/dplyr/versions/0.7.8">dplyr</a> (R)
* <a href="https://www.rdocumentation.org/packages/erer/versions/3.0">erer</a> (R)
* <a href="https://www.rdocumentation.org/packages/ez/versions/4.4-0">ez</a> (R)
* <a href="https://www.rdocumentation.org/packages/MASS/versions/7.3-52">MASS</a> (R)
* <a href="https://www.rdocumentation.org/packages/Matching/versions/4.9-7">Matching</a> (R)
* <a href="https://www.rdocumentation.org/packages/plm/versions/2.2-4">plm</a> (R)
* <a href="https://www.rdocumentation.org/packages/pscl/versions/1.5.5">pscl</a> (R)
* <a href="https://www.rdocumentation.org/packages/psych/versions/2.0.7">psych</a> (R)
* <a href="https://www.rdocumentation.org/packages/reshape/versions/0.8.8">reshape</a> (R)
* <a href="https://www.rdocumentation.org/packages/RPostgreSQL/versions/0.6-2">RPostgreSQL</a> (R)

## Acknowledgements
In the past half a year I was supervised by Hannes Datta (TiSEM) and Niels van de Ven (TiSEM), who I would like to thank for their comments on my thesis. Furthermore, I am grateful for Microsoft for providing Azure credits which we used to study image similarity.


*If you have any questions or suggestions, feel free to contact me: hoi@royklaassebos.nl*

<img src="https://raw.githubusercontent.com/RoyKlaasseBos/Hiding-Instagram-Likes/master/images/tiu_logo.png" alt="Logo Tilburg University" width=300px />
