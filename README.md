# Stock Data Extraction with Airflow

## Description

This is my first project on Apache Airflow. It creates an automated workflow to extract daily historical stock data from publicly traded companies. Data is collected for Apple (AAPL), Microsoft (MSFT), Google (GOOG), and Tesla (TSLA) and saved in CSV format. This project shows the practical application of Airflow in managing and automating data extraction processes.

## How It Works

The script defines a DAG (Directed Acyclic Graph) in Airflow to schedule and execute a data extraction task for each specified stock. The yfinance library is used to extract the data.

## Requirements

Python 3.x
Apache Airflow
yfinance
pendulum
pathlib

## Setup

Install all required libraries.
Set up Apache Airflow on your system.
Place the script in the Airflow DAGs directory.

## Execution

The DAG will automatically be executed by Airflow according to the defined schedule (0 0 * * 2-6), meaning every weekday from Tuesday to Saturday.
