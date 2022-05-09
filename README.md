# Web-Based-Data-Collecting-App-Using-Flask-And-Postgresql


<h2><a id="frontend">1. Frontend</a></h2>

1. We will implement two html pages - index.html and success.html
2. In Index.html, we will implement a form - to collect email id and user height
3. Once the input is successful and saved to postgresql database, we will move to show the success message on success.html



<h2><a id="backend">2. Backend</a></h2>

1. In the backend - we will use postgresql to store the data. 
2. We will also enforce that a person can't use the same email id multiple times.


<h2><a id="virtenv">3. Create Virtual Environment</a></h2>

1. Open new terminal and run the comman (python -m venv virtual). This will create a virtual python environment.
2. Install flask in the virtual env by (virtual\Scripts\pip install flask) or first activate the virtual environment python (virtual\Scripts\activate) and then run pip install flask.
3. Install psycopg2 using command (pip install psycopg2) in virtual environment.
4. Install Flask-SQLAlchemy (pip install Flask-SQLAlchemy)

<h2><a id="postgres">4. Postgresql Part</a></h2>

1. Open Pgadmin and create a Postgresql database for this application (name of table: height_collector)
2. Go to terminal, and activate virtual environment python (virtual\Scripts\activate)
3. Open pyhton terminal (python)
4. Run the command (from app import df) and then (db.create_all()). These two commands will create a table in Postgresql.

<h2><a id="deployweb">5. Deploy Website</a></h2>

1. Sign-up for Pythonanywhere (Beginner: Free acount)
2. Go to Console, and click on Bash Console. Using "pwd" you can see where you are.
3. Go to "web" section and create a new web app. Press next. Select Flask and python version. Press next. App is created.
4. Go to files. On the left side there will mysite option. Click there. Open the file "flask_app.py". Delete everything in that file and copy paste everything from script1.py in that file.
5. In mysite, create a new template folder. Upload templates files there.
6. Similarly create a static folder. Upload static files there.
7. Edit flask_app.py code (change app.run(debug=True) to app.run(debug=False))
8. Also upload send_email.py file in same directory as flask_app.py
9. Go to web section and click on Reload. It will provide a url. Click on the url and the website should be online.
10. In case the website is not online, look at error log.

To ensure the app works fine, we will need to create a postgresql data in Pythonanywhere server. 
1. Click on Databases.
2. Select MySQL database and create a password. Do remember the password (it will be required later). Click initialze. 
3. Create a new database "height_collector". Python will add username and $ sign before the given database name. 
4. Click on  start_console infront of created database. It will open a MySQL terminal.
5. "CREATE TABLE data (id SERIAL PRIMARY KEY, email VARCHAR(120), height INT);" run this sql query. This will create a table.
6. In flaks_app.py file change the settings to this new database. 'mysql+mysqlconnector://{username}:{password of mysql}@{Database host address}/{database name}' (line 7)


