🌦️ Astronomer Airflow Project — Weather Data Pipeline
========

Welcome to your Astronomer project! This project was generated using the astro dev init command via the Astronomer CLI. It has everything you need to develop, test, and run Apache Airflow pipelines locally.

📁 Project Structure
========

Your project includes the following files and folders:

1. dags/: 
Contains all Airflow DAGs (Directed Acyclic Graphs) for orchestrating workflows. By default, it includes:

2. weather_data_pipeline.py:
A custom ETL pipeline that fetches current weather data from a public Weather API (e.g., OpenWeatherMap or similar), processes the data, and optionally stores or logs it.
This DAG demonstrates the use of the TaskFlow API and can be extended for scheduled data ingestion or alerts.

3. Dockerfile: 
Defines the container environment using a versioned Astronomer Runtime image. Customize this to install additional system-level tools or libraries.

4. include/: 
Store any auxiliary files required by your DAGs or tasks. (Empty by default)

5. packages.txt: 
List OS-level packages to be installed in your Airflow environment. (Optional)

6. requirements.txt: 
Add Python dependencies your DAGs or tasks need (e.g., requests, pandas). (Optional)

7. plugins/: 
Extend Airflow’s capabilities by adding custom or community plugins. (Optional)

8. airflow_settings.yaml: 
A local-only settings file to preconfigure Airflow Connections, Variables, and Pools. It'd be helpful for version-controlling Airflow configurations during development.

🚀 Running Airflow Locally
========

1. To get started with Apache Airflow on your local machine, use the command: astro dev start
This command launches 4 Docker containers:
  Postgres: Metadata database
  Webserver: Airflow UI
  Scheduler: Executes scheduled tasks
  Triggerer: Handles deferred tasks (e.g., sensors)

2. Verify Containers are Running: docker ps
Look for containers named astro-... to confirm Airflow is up and running.

3. Access the Airflow UI. Open your browser and go to: http://localhost:8080
Login with:
    Username: admin
    Password: admin

4. Postgres Connection Info
Connect to the metadata database at:
  Host: localhost
  Port: 5432
  DB: Postgres
⚠️ If ports 8080 or 5432 are already in use, stop the conflicting containers or update your project’s port configuration.

☁️ Deploying to Astronomer Cloud
If you have an Astronomer Cloud account and a Deployment set up, you can easily push your code: astro deploy
For detailed deployment steps, check out the official Astronomer deployment guide.

