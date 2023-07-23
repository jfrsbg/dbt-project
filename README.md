# Repo description
The project is divided into sections as I'm making progress in the course. This repository simulates that you're an Analytics Engineer at Airbnb and you need to create some analysis in their data. 

## About data

The source data is from http://insideairbnb.com/ and it's already pre-prepared for the course's instructors. You can find the data I'm working with in pre-requistes/ folder.

## dbt connector
Using dbt-snowflake connector

# Getting started
- Create a snowflake account
- Execute the pre-requisites/snowflake_tables.sql inside you account
- create a ~/.dbt folder
    ```shell
    mkdir ~/.dbt
    ```
- create a working directory to you dbt project
    ```shell
    mkdir ~/Documents/dbt-project && cd ~/Documents/dbt-project
    ```
- install virtualenv via pip
    ```shell
    pip install virtualenv
    ```
- install python 3.11
    ```shell
    virtualenv venv --python=python3.11
    ```
- activate you virtuaenv
    ```shell
    . venv/bin/activate
    ```
- upgrade pip
    ```shell
    pip install --upgrade pip
    ```
- install dbt 1.5.0
    ```shell
    pip install dbt-snowflake==1.5.0
    ```
- initialize your project
    ```shell
    dbt init <your_folder>
    ```
- fill in the credentials that's being prompted to you based on pre-requisites/snowflake_tables.sql and based in the credentials you've provided when configuring your snowflake account.
    - schema: DEV
    - account: your snowflake account
    - database: AIRBNB
    - password: dbtPassword123
    - role: transform
    - user: dbt
    - warehouse: COMPUTE_WH


## Table of contents
- [x] models
- [x] materializations
- [x] seeds and sources
- [x] snapshots
- [x] tests
- [x] Macros, custom tests and packages
- [ ] Documentation
- [ ] Analysis, hooks and exposures

# dbt cheat sheet
- dbt snapshop
- dbt run
- dbt run --full-refresh --select fct_review: refresh the incremental table and select only the selected model
- dbt test
- dbt test --select dim_listings_cleansed: test only selected model
- dbt seed
- dbt deps: install dependencies
- dbt docs generate: generate docs
- dbt docs serve: serve docmentation page in your web browser

### Credits
** credits to Zoltan C. Toth for providing these learning tools for dbt.

To learn and understand every single concept in this repository, [check for the course](https://www.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt).