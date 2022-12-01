# SEEL4213
# PROBLEM STATEMENT
# - No emergency call have been made when car, motocycle and lorry involve in accident because no one else saw the accident happen
# SYSTEM ARCHITECTURE
# - Sensor
# > IR sensor, Accelerometer, Gyro
# - Cloud Platform
# Create and Setup Django Rest Framework project 
# mkdir myproject
cd myproject
# Create a virtual environment to isolate our package dependencies locally
python3 -m venv env
source env/bin/activate
# Install Django and Django REST framework into the virtual environment
pip install django djangorestframework
# Install database specific libraries for the project, in this case PostgresSQL and Bigquery
pip install google-cloud-bigquery psycopg2
# Additional libraries to run the project and serve static files
pip install gunicorn whitenoise
# Set up a new project with a single application
django-admin startproject myproject .  
django-admin startapp crashdata_monitoring
# Create Google Cloud Project
# To install some cloud build tools
gcloud components install beta
# Authenticate with Google Cloud:
gcloud auth login
gcloud auth application-default login
# Create cloud project — choose your unique project name:
gcloud projects create [Crash_Detection]
# Set current project
gcloud config set project [Crash_Detection]
# Enable SQL admin on gcloud
gcloud services enable sqladmin
# SENSOR
# NodeMCU ESP32 using HTTP protocol
# > Build-in with wifi and bluetooth module make the device is very suitable to be use for IoT
# > Have a sufficient of I/O pin for this project
