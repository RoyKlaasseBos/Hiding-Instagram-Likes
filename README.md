# Hiding Likes on Instagram 
### Goodbye Likes, Hello Mental Health - How Hiding Like Counts Affects User Behavior and Self-Esteem

<p style="clear: both;">This repository contains supplemental material associated with my research master thesis. Specifically, the <a href="https://github.com/RoyKlaasseBos/Hiding-Instagram-Likes/blob/master/Web_Appendix_Hiding_Like_Counts_Instagram.ipynb">online appendix</a> describes the methods associated with the observational study and experiment. On a conceptual level we investigate the effect of hiding like counts on Instagram on users' posting frequency (H1), variety of visual-content (H2), like behavior (H3), and self-esteem (H4).</p>

<img src="https://raw.githubusercontent.com/RoyKlaasseBos/Hiding-Instagram-Likes/master/images/conceptual_model.jpg" alt="Conceptual model" width=750px />

## Data Description
This research project builds on an observational data set scraped from Instagram (July 2020) and an experimental dataset obtained through a questionnaire on Prolific (N=600). Preprocessing of the raw data is documented in a step-by-step fashion in the appendix. Definitions and descriptions are outlined over <a href="https://github.com/RoyKlaasseBos/Hiding-Instagram-Likes/blob/master/Data_Set_Description.ipynb">here</a>. All data can be accessed through a relational database service. Attached online appendix refers to multiple environment variables in order to connect to the database (see instructions below). Credentials can be acquired by contacting one of the authors.

## Configure Environment Variables
Just like you sign in to Google Drive using your email and password credentials, we need to log in to our relational database using a database URL (`INSTAGRAM_DB_URL`) and database key (`INSTAGRAM_DB_KEY`). The idea is that we store these variables on our local machine without hardcoding them into our notebook. Below we briefly describe how to configure these environment variables. Alternatively, watch one of these tutorials ([Mac/Linux](https://www.youtube.com/watch?v=5iWhQWVXosU) & [Windows](https://www.youtube.com/watch?v=IolxqkL7cD8)). 

*Mac / Linux*
1. Go to the terminal and type `printenv` to list all environment variables stored on your machine. 
2. Assuming that `INSTAGRAM_DB_URL` and `INSTAGRAM_DB_KEY` are not listed there yet, we going to define these two new variables. Type `nano .bash_profile` to open a text editor in the terminal. 
3. Within this window you can create new variables as follows: `export [VARIABLE_NAME]="the string value you want to store";` (e.g. `INSTAGRAM_DB_URL="http://anotherurl.com"`). Note that there is no space between the variable name and its value and that the string is enclosed in double quotes. Using this approach create a `INSTAGRAM_DB_URL` and `INSTAGRAM_DB_KEY` variable (you can list them below one another in the same file).
4. Exit the editor by pressing Ctrl + X, choose `Y` (to save changes), and finally press `Enter`.

*Windows*
1. Open up "Control Panel" > "System and Security" > "System".
2. In the left sidebar click on "Advanced system settings".
3. Click on "Environment Variables" in the bottom right.
4. Create a new "User Variable" (top list) and fill out the "Variable name" and "Variable value" (`INSTAGRAM_DB_URL` and [DB_URL], respectively).
5. Repeat the same for the secret `INSTAGRAM_DB_KEY` and double click "OK" twice.

*Note: you may need to restart your terminal and IDE in order for the changes to go into effect.*


## Acknowledgements
In the past half a year I was supervised by Hannes Datta (TiSEM) and Niels van de Ven (TiSEM), who I would like to thank for their comments on my thesis. Furthermore, I am grateful for Microsoft for providing Azure credits which we used to study image similarity.


*If you have any questions or suggestions, feel free to contact me: hoi@royklaassebos.nl*

<img src="https://raw.githubusercontent.com/RoyKlaasseBos/Hiding-Instagram-Likes/master/images/tiu_logo.png" alt="Logo Tilburg University" width=300px />
