# Custom ELT Project

This project showcases a custom Extract, Load, Transform (ELT) process using Docker and PostgreSQL. It simplifies data handling tasks for users.

## Repository Structure

1. **docker-compose.yaml**: This file contains the configuration for Docker Compose

2. **elt_script/Dockerfile**: This Dockerfile sets up a Python environment and installs the PostgreSQL client.

3. **elt_script/elt_script.py**: This Python script performs the ELT process. It waits for the source PostgreSQL database to become available, then dumps its data to a SQL file and loads this data into the destination PostgreSQL database.

4. **source_db_init/init.sql**: This SQL script initializes the source database with sample data, creating and populating tables.



## How it works

1. Ensure you have Docker and Docker Compose installed on your machine.
2. Navigate to the repository directory and run `docker-compose up`.
3. Once all containers are up and running, the ELT process will start automatically.
4. After the ELT process completes, you can access the source and destination PostgreSQL databases on ports 5433 and 5434, respectively.
