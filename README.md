# Web-Based-Data-Collecting-App-Using-Flask-And-Postgresql


<h2><a id="frontend">1. Frontend</a></h2>



<h2><a id="backend">2. Backend</a></h2>


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
