# Courier-Management-System

Courier Management System gives all information regarding the every Courier in the systems.
The system has two user role one is customer, who can track package using randomly generated number and another role is manager who can add packages and customer details.
All of them there is a primary role is admin who can add branches and location in the system.

## Setting up on Localhost

You may use any local web hosting server, but We recommend using [MAMP](https://www.mamp.info/en/windows/) as it allows you to set custom location, instead of every time putting & updating changes by going into `htdocs` folder.
Also, it doesn't disturb any existing installations!

Here, we will demonstrate using MAMP server.

### Setting up server

1. Install MAMP.
2. Clone this repository.
3. Open MAMP > Preferences > Web Server > Select.
   - Select the repo folder
   - ![Preferences Menu](https://i.imgur.com/cJhMiQG.png)
4. Click on `Ok` > `Start Server` and then click on `Open WebStart page`
5. In the webpage, Go to `Tools` > `phpMyAdmin`
6. A new page will open. 

### Setting up database

1. The new page will open `phpMyAdmin` . Here you need to create a database.
2. Click on `New` and set the name as - `courier_db`
3. After creating, open that database & go to `SQL` tab & copy-paste the commands from [here](./database/courier_db.sql) & execute them on the `SQL` tab by clicking on `Go` button.

### Setting up access rights

1. In the same database, go to `User accounts` tab & click on `Add user account`.
2. Setup accordingly - 
	- ![image-20201208165734232](https://i.imgur.com/zC9MIU1.png)
3. Scroll to bottom and click on `Go` at the right side to save changes.
4. After saving changes, go to `Database` section & click on `courier_db` then click on `Go` to save changes. ![image-20201208165959729](https://i.imgur.com/s1GNOkZ.png)

5. In the next page, tick the `Check all` & `Go` to save changes.

### Launching the Website

Type `localhost` in the URL bar and the website should be up & running!