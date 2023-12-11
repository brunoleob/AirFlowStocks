# Stock Data Extraction with Airflow

## Description

This is my first project on Apache Airflow. It creates an automated workflow to extract daily historical stock data from publicly traded companies. Data is collected for Apple (AAPL), Microsoft (MSFT), Google (GOOG), and Tesla (TSLA) and saved in CSV format. This project shows the practical application of Airflow in managing and automating data extraction processes.

## Included Data Files
The sample data files have been added to the “stocks” directory.

## How It Works

The script defines a DAG (Directed Acyclic Graph) in Airflow to schedule and execute a data extraction task for each specified stock. The yfinance library is used to extract the data.

## Celery Executor and Redis Setup
The project utilizes the Celery executor for parallel task execution. A non-relational Redis database serves as the message broker for task queuing. This configuration enhances the scalability and performance of the data extraction process.

## Advantages of Celery
The use of Celery introduces parallelism, allowing multiple tasks to be executed simultaneously, and high availability, ensuring robust and reliable task execution.

## Worker Configuration
Workers have been configured to handle parallel processing of tasks, ensuring efficient and timely execution of the data extraction workflow.

## Execution Monitoring with Flower
The Flower tool has been integrated to provide a web-based monitoring interface for observing the progress and status of task executions. Flower enhances visibility into the Celery tasks and aids in debugging and performance optimization.

## Requirements

- Python 3.x
- Apache Airflow
- yfinance
- pendulum
- pathlib
- Redis

## Setup

1. Install all required libraries.
2. Set up Apache Airflow on your system.
3. Place the script in the Airflow DAGs directory.

## Execution

The DAG will automatically be executed by Airflow according to the defined schedule (0 0 * * 2-6), meaning every weekday from Tuesday to Saturday.
