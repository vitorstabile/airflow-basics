<h1 align="center"> Airflow </h1>

# Content

1. [Chapter 1: Introduction to Apache Airflow](#chapter1)
    - [Chapter 1 - Part 1: What is Apache Airflow and why use it?](#chapter1part1)
      - [Chapter 1 - Part 1.1: What is Apache Airflow?](#chapter1part1.1)
      - [Chapter 1 - Part 1.2: Why Use Apache Airflow?](#chapter1part1.2)
      - [Chapter 1 - Part 1.3: Real-World Applications](#chapter1part1.3)
    - [Chapter 1 - Part 2: Understanding DAGs, Tasks, and Operators](#chapter1part2)
      - [Chapter 1 - Part 2.1: Directed Acyclic Graphs (DAGs)](#chapter1part2.1)
      - [Chapter 1 - Part 2.2: Tasks](#chapter1part2.2)
      - [Chapter 1 - Part 2.3: Operators](#chapter1part2.3)
      - [Chapter 1 - Part 2.4: Workflow](#chapter1part2.4)
    - [Chapter 1 - Part 3: Airflow Architecture: Scheduler, Webserver, and Metadata Database](#chapter1part3)
      - [Chapter 1 - Part 3.1: Core Components of Airflow](#chapter1part3.1)
      - [Chapter 1 - Part 3.2: Interaction Between Components](#chapter1part3.2)
      - [Chapter 1 - Part 3.3: Executors](#chapter1part3.3)
      - [Chapter 1 - Part 3.4: Architectures in Airflow](#chapter1part3.4)
    - [Chapter 1 - Part 4: Setting up a Local Airflow Environment (using Docker)](#chapter1part4)
      - [Chapter 1 - Part 4.1: Understanding Docker for Airflow](#chapter1part4.1)
      - [Chapter 1 - Part 4.2: Prerequisites](#chapter1part4.2)
      - [Chapter 1 - Part 4.3: Setting Up Airflow with Docker Compose](#chapter1part4.3)
      - [Chapter 1 - Part 4.4: Customizing Your Airflow Environment](#chapter1part4.4)
      - [Chapter 1 - Part 4.5: Troubleshooting Common Issues](#chapter1part4.5)
    - [Chapter 1 - Part 5: Introduction to the Airflow UI](#chapter1part5)
      - [Chapter 1 - Part 5.1: Accessing the Airflow UI](#chapter1part5.1)
      - [Chapter 1 - Part 5.2: Key Components of the Airflow UI](#chapter1part5.2)
      - [Chapter 1 - Part 5.3: Using the Airflow UI for Monitoring and Troubleshooting](#chapter1part5.3)
2. [Chapter 2: Building Your First DAG](#chapter2)
    - [Chapter 2 - Part 1: Defining a Simple DAG: A "Hello World" Example](#chapter2part1)
      - [Chapter 2 - Part 1.1: Understanding the Basic Structure of a DAG](#chapter2part1.1)
      - [Chapter 2 - Part 1.2: Practical Examples and Demonstrations](#chapter2part1.2)
    - [Chapter 2 - Part 2: Understanding Task Dependencies and Workflow Orchestration](#chapter2part2)
      - [Chapter 2 - Part 2.1: Defining Task Dependencies](#chapter2part2.1)
      - [Chapter 2 - Part 2.2: Workflow Orchestration](#chapter2part2.2)
      - [Chapter 2 - Part 2.3: Real-World Application](#chapter2part2.3)
    - [Chapter 2 - Part 3: Using BashOperator for Simple Commands](#chapter2part3)
      - [Chapter 2 - Part 3.1: Understanding the BashOperator](#chapter2part3.1)
      - [Chapter 2 - Part 3.2: Practical Examples and Demonstrations](#chapter2part3.2)
      - [Chapter 2 - Part 3.3: Best Practices](#chapter2part3.3)
    - [Chapter 2 - Part 4: Defining DAG Schedules and Catchup](#chapter2part4)
      - [Chapter 2 - Part 4.1: Understanding DAG Schedules](#chapter2part4.1)
      - [Chapter 2 - Part 4.2: Understanding Catchup](#chapter2part4.2)
      - [Chapter 2 - Part 4.3: Practical Examples and Demonstrations](#chapter2part4.3)
    - [Chapter 2 - Part 5: Running and Monitoring Your DAG in the Airflow UI](#chapter2part5)
      - [Chapter 2 - Part 5.1: Accessing the Airflow UI](#chapter2part5.1)
      - [Chapter 2 - Part 5.2: Understanding the DAGs View](#chapter2part5.2)
      - [Chapter 2 - Part 5.3: Exploring the DAG Details View](#chapter2part5.3)
      - [Chapter 2 - Part 5.4: Triggering DAG Runs](#chapter2part5.4)
      - [Chapter 2 - Part 5.5: Monitoring DAG Runs](#chapter2part5.5)
      - [Chapter 2 - Part 5.6: Common Use Cases for the Airflow UI](#chapter2part5.6)
3. [Chapter 3: Core Airflow Operator](#chapter3)
    - [Chapter 3 - Part 1: Introduction to Common Operators: PythonOperator, EmailOperator](#chapter3part1)
      - [Chapter 3 - Part 1.1: PythonOperator: Executing Python Code](#chapter3part1.1)
      - [Chapter 3 - Part 1.2: EmailOperator: Sending Email Notifications](#chapter3part1.2)
    - [Chapter 3 - Part 2: Working with Data Transfer Operators: S3Hook and S3FileTransferOperator](#chapter3part2)
      - [Chapter 3 - Part 2.1: Understanding S3Hook](#chapter3part2.1)
      - [Chapter 3 - Part 2.2: Understanding S3FileTransferOperator](#chapter3part2.2)
      - [Chapter 3 - Part 2.3: Real-World Application](#chapter3part2.3)
    - [Chapter 3 - Part 3: Using the PostgresOperator to Interact with Databases](#chapter3part3)
      - [Chapter 3 - Part 3.1: Understanding the PostgresOperator](#chapter3part3.1)
      - [Chapter 3 - Part 3.2: Advanced Usage and Best Practices](#chapter3part3.2)
    - [Chapter 3 - Part 4: Understanding Idempotency and Task Retries](#chapter3part4)
      - [Chapter 3 - Part 4.1: Understanding Idempotency](#chapter3part4.1)
      - [Chapter 3 - Part 4.2: Understanding Task Retries](#chapter3part4.2)
      - [Chapter 3 - Part 4.3: Real-World Application](#chapter3part4.3)
    - [Chapter 3 - Part 5: Best Practices for Operator Usage](#chapter3part5)
      - [Chapter 3 - Part 5.1: Understanding Operator Idempotency](#chapter3part5.1)
      - [Chapter 3 - Part 5.2: Configuring Task Retries](#chapter3part5.2)
      - [Chapter 3 - Part 5.3: Choosing the Right Operator](#chapter3part5.3)
4. [Chapter 4: Variables and Connections](#chapter4)
    - [Chapter 4 - Part 1: Introduction to Airflow Variables](#chapter4part1)
      - [Chapter 4 - Part 1.1: Understanding Airflow Variables](#chapter4part1.1)
      - [Chapter 4 - Part 1.2: Setting and Retrieving Variables](#chapter4part1.2)
      - [Chapter 4 - Part 1.3: Practical Examples](#chapter4part1.3)
    - [Chapter 4 - Part 2: Setting and Retrieving Variables in the UI and DAGs](#chapter4part2)
      - [Chapter 4 - Part 2.1: Understanding Airflow Variables](#chapter4part2.1)
      - [Chapter 4 - Part 2.2: Setting Variables in the Airflow UI](#chapter4part2.2)
      - [Chapter 4 - Part 2.3: Retrieving Variables in DAGs](#chapter4part2.3)
      - [Chapter 4 - Part 2.4: Best Practices for Using Variables](#chapter4part2.4)
    - [Chapter 4 - Part 3: Understanding Airflow Connections](#chapter4part3)
      - [Chapter 4 - Part 3.1: Understanding Airflow Connections](#chapter4part3.1)
      - [Chapter 4 - Part 3.2: Best Practices for Using Connections](#chapter4part3.2)
    - [Chapter 4 - Part 4: Configuring Connections for Databases, APIs, and Cloud Services](#chapter4part4)
      - [Chapter 4 - Part 4.1: Understanding Airflow Connections](#chapter4part4.1)
      - [Chapter 4 - Part 4.2: Configuring Connections](#chapter4part4.2)
      - [Chapter 4 - Part 4.3: Using Connections in DAGs](#chapter4part4.3)
      - [Chapter 4 - Part 4.4: Connection Examples for Different Services](#chapter4part4.4)
      - [Chapter 4 - Part 4.5: Practice Activities](#chapter4part4.5)
    - [Chapter 4 - Part 5: Using Variables and Connections for Secure Configuration Management](#chapter4part5)
      - [Chapter 4 - Part 5.1: Understanding the Need for Secure Configuration Management](#chapter4part5.1)
      - [Chapter 4 - Part 5.2: Airflow Variables: Dynamic Configuration Options](#chapter4part5.2)
      - [Chapter 4 - Part 5.3: Airflow Connections: Securely Storing Credentials](#chapter4part5.3)
      - [Chapter 4 - Part 5.4: Using Variables and Connections Together](#chapter4part5.4)
      - [Chapter 4 - Part 5.5: Practice Activities](#chapter4part5.5)
5. [Chapter 5: Advanced DAG Concepts](#chapter5)
    - [Chapter 5 - Part 1: SubDAGs and TaskGroups for Modular DAG Design](#chapter5part1)
      - [Chapter 5 - Part 1.1: Understanding SubDAGs](#chapter5part1.1)
      - [Chapter 5 - Part 1.2: Understanding TaskGroups](#chapter5part1.2)
      - [Chapter 5 - Part 1.3: SubDAGs vs. TaskGroups: A Comparison](#chapter5part1.3)
      - [Chapter 5 - Part 1.4: Practical Examples and Demonstrations](#chapter5part1.4)
    - [Chapter 5 - Part 2: Using BranchPythonOperator for Conditional Logic](#chapter5part2)
      - [Chapter 5 - Part 2.1: Understanding the BranchPythonOperator](#chapter5part2.1)
    - [Chapter 5 - Part 3: Dynamic DAG Generation with Python](#chapter5part3)
      - [Chapter 5 - Part 3.1: Understanding Dynamic DAG Generation](#chapter5part3.1)
      - [Chapter 5 - Part 3.2: Implementing Dynamic DAG Generation](#chapter5part3.2)
    - [Chapter 5 - Part 4: Understanding XComs for Inter-Task Communication](#chapter5part4)
      - [Chapter 5 - Part 4.1: Understanding XComs](#chapter5part4.1)
    - [Chapter 5 - Part 5: Implementing Error Handling and Alerting](#chapter5part5)
      - [Chapter 5 - Part 5.1: Understanding Error Handling in Airflow](#chapter5part5.1)
6. [Chapter 6: Airflow Sensors](#chapter6)
    - [Chapter 6 - Part 1: Introduction to Airflow Sensors](#chapter6part1)
      - [Chapter 6 - Part 1.1: Understanding Airflow Sensors](#chapter6part1.1)
      - [Chapter 6 - Part 1.2: Types of Airflow Sensors](#chapter6part1.2)
      - [Chapter 6 - Part 1.3: Sensor Parameters](#chapter6part1.3)
      - [Chapter 6 - Part 1.4: Practical Examples](#chapter6part1.4)
      - [Chapter 6 - Part 1.5: Best Practices for Using Sensors](#chapter6part1.5)
    - [Chapter 6 - Part 2: Using FileSensor to wait for file arrival](#chapter6part2)
      - [Chapter 6 - Part 2.1: Understanding the FileSensor](#chapter6part2.1)
    - [Chapter 6 - Part 3: Using HttpSensor to check for API availability](#chapter6part3)
      - [Chapter 6 - Part 3.1: Understanding the HttpSensor](#chapter6part3.1)
      - [Chapter 6 - Part 3.2: Best Practices for Using HttpSensor](#chapter6part3.2)
    - [Chapter 6 - Part 4: Creating Custom Sensors](#chapter6part4)
      - [Chapter 6 - Part 4.1: Understanding Custom Sensors](#chapter6part4.1)
      - [Chapter 6 - Part 4.2: Advanced Custom Sensors](#chapter6part4.2)
      - [Chapter 6 - Part 4.3: Best Practices for Custom Sensors](#chapter6part4.3)
      - [Chapter 6 - Part 4.4: Real-World Application](#chapter6part4.4)
    - [Chapter 6 - Part 5: Best practices for using Sensors](#chapter6part5)
      - [Chapter 6 - Part 5.1: Sensor Timeouts and Failure Modes](#chapter6part5.1)
      - [Chapter 6 - Part 5.2: Sensor Modes: Poke vs. Deferrable](#chapter6part5.2)
      - [Chapter 6 - Part 5.3: Optimizing Sensor Performance](#chapter6part5.3)
      - [Chapter 6 - Part 5.4: Best Practices for Sensor Design](#chapter6part5.4)
7. [Chapter 7: Deploying Airflow to Production](#chapter7)
    - [Chapter 7 - Part 1: Choosing a Deployment Strategy: Kubernetes, Docker Compose, Managed Services](#chapter7part1)
      - [Chapter 7 - Part 1.1: Deployment Strategies for Apache Airflow](#chapter7part1.1)
      - [Chapter 7 - Part 1.2: Choosing the Right Strategy](#chapter7part1.2)
      - [Chapter 7 - Part 1.3: Practice Activities](#chapter7part1.3)
    - [Chapter 7 - Part 2: Configuring Airflow for Production: Database, Executor, Logging](#chapter7part2)
      - [Chapter 7 - Part 2.1: Database Configuration](#chapter7part2.1)
      - [Chapter 7 - Part 2.2: Executor Configuration](#chapter7part2.2)
      - [Chapter 7 - Part 2.3: Logging Configuration](#chapter7part2.3)
    - [Chapter 7 - Part 3: Implementing Monitoring and Alerting](#chapter7part3)
      - [Chapter 7 - Part 3.1: Key Monitoring Metrics](#chapter7part3.1)
      - [Chapter 7 - Part 3.2: Tools for Monitoring Airflow](#chapter7part3.2)
      - [Chapter 7 - Part 3.3: Implementing Alerting](#chapter7part3.3)
      - [Chapter 7 - Part 3.4: Best Practices for Monitoring and Alerting](#chapter7part3.4)
    - [Chapter 7 - Part 4: Understanding Airflow Security Best Practices](#chapter7part4)
      - [Chapter 7 - Part 4.1: Authentication and Authorization](#chapter7part4.1)
      - [Chapter 7 - Part 4.2: Encryption](#chapter7part4.2)
      - [Chapter 7 - Part 4.3: Network Security](#chapter7part4.3)
      - [Chapter 7 - Part 4.4: Other Security Considerations](#chapter7part4.4)
    - [Chapter 7 - Part 5: Scaling Airflow for High Availability](#chapter7part5)
      - [Chapter 7 - Part 5.1: Understanding High Availability and Scalability in Airflow](#chapter7part5.1)
      - [Chapter 7 - Part 5.2: Architectures for Scaling Airflow](#chapter7part5.2)
      - [Chapter 7 - Part 5.3: Configuring Airflow for High Availability](#chapter7part5.3)
      - [Chapter 7 - Part 5.4: Implementing Monitoring and Alerting](#chapter7part5.4)
      - [Chapter 7 - Part 5.5: Airflow Security Best Practices](#chapter7part5.5)
  
## <a name="chapter1"></a>Chapter 1: Introduction to Apache Airflow

#### <a name="chapter1part1"></a>Chapter 1 - Part 1: What is Apache Airflow and why use it?

Apache Airflow has become a cornerstone in modern data engineering, enabling teams to orchestrate complex workflows with reliability and scalability. Understanding what Airflow is and why it's used is crucial for anyone looking to build and manage data pipelines effectively. This lesson will provide a comprehensive introduction to Airflow, covering its core functionalities, benefits, and use cases, setting the stage for more advanced topics in subsequent modules.

#### <a name="chapter1part1.1"></a>Chapter 1 - Part 1.1: What is Apache Airflow?

Apache Airflow is an open-source workflow management platform for data engineering pipelines. It allows you to programmatically author, schedule, and monitor workflows. In simpler terms, Airflow helps you define a series of tasks and their dependencies, ensuring they are executed in the correct order and at the right time.

**Key Concepts**

- **Workflows (DAGs)**: Airflow represents workflows as Directed Acyclic Graphs (DAGs). A DAG is a collection of tasks organized to reflect their dependencies. "Directed" means the tasks have a specific order, "Acyclic" means there are no loops (a task cannot depend on itself, directly or indirectly), and "Graph" represents the connections between tasks.
- **Tasks**: A task represents a single unit of work within a DAG. It could be anything from running a Python script to executing a SQL query or transferring data between systems.
- **Operators**: Operators are pre-built task templates that encapsulate common actions. Airflow provides a variety of operators for interacting with different systems and services, such as BashOperator for executing shell commands, PythonOperator for running Python functions, and operators for interacting with cloud platforms like AWS, Google Cloud, and Azure.
- **Scheduling**: Airflow allows you to schedule DAGs to run at specific intervals (e.g., daily, hourly) or based on external triggers.
- **Monitoring**: Airflow provides a web-based UI for monitoring the status of DAGs and tasks, viewing logs, and troubleshooting issues.

**Example: A Simple Data Pipeline**

Imagine a scenario where you need to:

- Extract data from a database.
- Transform the data (e.g., clean, aggregate).
- Load the transformed data into a data warehouse.

Using Airflow, you can define a DAG with three tasks:

- ```extract_data```: Executes a SQL query to extract data from the database.
- ```transform_data```: Runs a Python script to transform the extracted data.
- ```load_data```: Loads the transformed data into the data warehouse.

You would also define the dependencies between these tasks, ensuring that transform_data runs only after extract_data completes successfully, and load_data runs only after transform_data completes successfully. Airflow would then schedule and execute this DAG according to your defined schedule, monitoring the status of each task and alerting you to any failures.

#### <a name="chapter1part1.2"></a>Chapter 1 - Part 1.2: Why Use Apache Airflow?

Airflow addresses several key challenges in building and managing data pipelines:

**1. Workflow Orchestration**

Airflow provides a centralized platform for orchestrating complex workflows, ensuring that tasks are executed in the correct order and at the right time. This eliminates the need for manual scheduling and coordination, reducing the risk of errors and improving efficiency.

Example: Consider a marketing analytics pipeline that requires data from multiple sources (e.g., website analytics, CRM, social media) to be combined and processed before generating reports. Airflow can orchestrate this entire process, ensuring that data is extracted from each source, transformed, and loaded into a central data warehouse in a timely and reliable manner.

**2. Scalability and Reliability**

Airflow is designed to handle large-scale workflows with thousands of tasks. It can be deployed on a variety of infrastructure, including cloud platforms like AWS, Google Cloud, and Azure, allowing you to scale your workflows as needed. Airflow also provides built-in fault tolerance, ensuring that workflows continue to run even if individual tasks fail.

Example: An e-commerce company might use Airflow to process millions of transactions daily, generating personalized recommendations for customers. Airflow's scalability ensures that the pipeline can handle the increasing volume of data as the company grows.

**3. Monitoring and Alerting**

Airflow provides a web-based UI for monitoring the status of DAGs and tasks, viewing logs, and troubleshooting issues. It also supports alerting, allowing you to receive notifications when tasks fail or when other issues occur. This enables you to quickly identify and resolve problems, minimizing downtime and ensuring data quality.

Example: A financial services company might use Airflow to monitor its fraud detection pipeline, receiving alerts when suspicious transactions are detected. This allows them to quickly investigate and prevent fraudulent activity.

**4. Code as Configuration**

Airflow allows you to define workflows as code, using Python. This provides several benefits:

- **Version Control**: Workflows can be stored in version control systems like Git, allowing you to track changes and collaborate with other developers.
- **Testability**: Workflows can be tested using standard Python testing frameworks, ensuring that they are reliable and accurate.
- **Reusability**: Workflows can be easily reused and adapted for different purposes.

Example: A data science team might use Airflow to define a machine learning pipeline as code, allowing them to easily version control, test, and reuse the pipeline for different models and datasets.

**5. Extensibility**

Airflow is highly extensible, allowing you to create custom operators and hooks for interacting with different systems and services. This makes it easy to integrate Airflow with your existing infrastructure and tools.

Example: A research institution might develop custom Airflow operators for interacting with specialized scientific instruments or data repositories.

#### <a name="chapter1part1.3"></a>Chapter 1 - Part 1.3: Real-World Applications

Here are some real-world examples of how Airflow is used:

- **Data Warehousing**: Orchestrating the extraction, transformation, and loading (ETL) of data into a data warehouse.
- **Machine Learning**: Building and deploying machine learning models, including data preprocessing, model training, and model evaluation.
- **Business Intelligence**: Generating reports and dashboards for business users.
- **Financial Services**: Automating financial processes, such as fraud detection and risk management.
- **E-commerce**: Personalizing customer experiences and optimizing marketing campaigns.

**Hypothetical Scenario**

Imagine a small startup that provides a subscription-based service. They need to analyze user behavior to improve their product and marketing efforts. They have data scattered across various sources:

- User activity logs stored in cloud storage (e.g., AWS S3).
- Subscription data in a relational database (e.g., PostgreSQL).
- Marketing campaign data from a third-party API.

Without Airflow, they might rely on manual scripts or ad-hoc processes to collect and analyze this data. This is prone to errors, difficult to scale, and lacks proper monitoring.

With Airflow, they can define a DAG that automates the entire process:

- **Extract**: Extract data from S3, PostgreSQL, and the marketing API using appropriate Airflow operators (e.g., S3Hook, PostgresOperator, SimpleHttpOperator - which we will cover in later modules).
- **Transform**: Clean and transform the data using Python scripts executed with the PythonOperator. This might involve tasks like data validation, aggregation, and feature engineering.
- **Load**: Load the transformed data into a data warehouse (e.g., Snowflake, BigQuery) using a dedicated operator.
- **Analyze**: Trigger a data analysis script or notebook to generate insights and reports.

This Airflow DAG ensures that the data is processed consistently, reliably, and on a schedule. The startup can monitor the pipeline's progress, receive alerts for any failures, and easily scale the pipeline as their data volume grows.

#### <a name="chapter1part2"></a>Chapter 1 - Part 2: Understanding DAGs, Tasks, and Operators

Understanding DAGs, Tasks, and Operators is fundamental to grasping how Apache Airflow works. These three components are the building blocks of any workflow you'll create in Airflow. A DAG defines the overall structure, Tasks represent individual units of work, and Operators determine what that work actually is. Without a solid understanding of these concepts, building and managing complex data pipelines with Airflow becomes significantly more challenging. This lesson will provide a comprehensive overview of DAGs, Tasks, and Operators, equipping you with the knowledge to design and implement effective workflows.

#### <a name="chapter1part2.1"></a>Chapter 1 - Part 2.1: Directed Acyclic Graphs (DAGs)

A DAG, or Directed Acyclic Graph, is the core concept in Airflow. It represents a workflow, a collection of tasks you want to run, organized in a way that reflects their dependencies.

**DAG (Directed Acyclic Grapsh)**

- The Dag means directed acyclic graph, and a Dag is a collection of all the tasks you want to run, organized in a way that reflects their relationships and dependencies.
- It helps you to define the structure of your entire workflow, showing which tasks needs to happen before others.
- A Dag in airflow lists all the tasks to complete your data workflow in the right sequence.

<br>

<div align="center"><img src="img/dagexample-w527-h344.png" width=527 height=344><br><sub>Example of a DAG - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>

You have four tasks T1, T2, T3, and T4. T4 depends on T1, T2, and T3.
So you have those directed dependencies, and you know that in order to execute T4, because, T1, T2 and T3 need to run first.

**You don't have any cycle in your graph in your Dag**

<br>

<div align="center"><img src="img/notdagexample-w527-h459.png" width=527 height=459><br><sub>Example of NOT a DAG - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>

Because you have a loop. You can see that T4 depends on t1, t2, t3, but T1 also depends on T4. So you have a loop like an infinite loop. And this is not an acyclic graph.

**What "Directed Acyclic Graph" Means**

- **Directed**: The graph has direction. This means the connections between tasks have a specific order. Task A might depend on Task B, indicating that Task B must complete successfully before Task A can start. This directionality defines the flow of execution.
- **Acyclic**: The graph cannot have cycles. This means you can't have a situation where Task A depends on Task B, Task B depends on Task C, and Task C depends on Task A. Such a cycle would create an infinite loop, making it impossible to determine the execution order.
- **Graph**: In this context, a graph is a collection of nodes (Tasks) and edges (dependencies) that define the relationships between those nodes.

**DAG Definition in Airflow**

In Airflow, a DAG is defined using Python code. This code specifies the tasks to be executed and their dependencies. The Airflow scheduler reads this code and uses it to orchestrate the execution of the workflow.

**Example of a Simple DAG**

Here's a basic example of a DAG definition:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='simple_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example']
) as dag:
    # Define a task that executes a Bash command
    task1 = BashOperator(
        task_id='print_date',
        bash_command='date'
    )

    # Define another task
    task2 = BashOperator(
        task_id='sleep',
        bash_command='sleep 5'
    )

    # Define task dependencies
    task1 >> task2 # task1 will run before task2
```

In this example:

- We import the necessary modules from Airflow.
- We create a DAG object, providing a dag_id, start_date, schedule_interval, catchup and tags.
  - ```dag_id``` is a unique identifier for the DAG.
  - ```start_date``` specifies the date from which the DAG should start running.
  - ```schedule_interval``` defines how often the DAG should be triggered (e.g., daily, weekly). None means the DAG will only be triggered manually.
  - ```catchup``` is a boolean that determines whether Airflow should run the DAG for all missed intervals between the start_date and the current date.
  - ```tags``` are labels that can be used to categorize and filter DAGs in the Airflow UI.
- We define two tasks, task1 and task2, using the BashOperator. Each task is given a task_id and a bash_command to execute.
- We define the dependency between the tasks using the >> operator. This indicates that task1 must complete successfully before task2 can start.

**DAG Attributes**

DAGs have several important attributes that control their behavior:

- ```dag_id```: A unique identifier for the DAG. This is used to identify the DAG in the Airflow UI and when triggering DAG runs.
- ```start_date```: The date from which the DAG should start running. Airflow uses this to determine which DAG runs to schedule.
- ```schedule_interval```: Defines how often the DAG should be triggered. This can be a cron expression (e.g., '0 0 * * *' for daily at midnight), a timedelta object (e.g., timedelta(days=1) for daily), or a preset schedule (e.g., '@daily' for daily).
- ```catchup```: A boolean that determines whether Airflow should run the DAG for all missed intervals between the start_date and the current date. Setting this to False is generally recommended for production DAGs to avoid overwhelming the system with backdated runs.
- ```tags```: A list of tags that can be used to categorize and filter DAGs in the Airflow UI.
- ```default_args```: A dictionary of default arguments that will be passed to all tasks in the DAG. This can be used to set default values for parameters like retries, retry_delay, and owner.

**Real-World Examples of DAGs**

- **Data Ingestion Pipeline**: A DAG could be used to ingest data from various sources (e.g., APIs, databases, files), transform it, and load it into a data warehouse. Each task in the DAG could represent a specific step in the ingestion process, such as extracting data from an API, cleaning the data, and loading it into a database.
- **Machine Learning Model Training**: A DAG could be used to automate the process of training and deploying a machine learning model. Tasks could include fetching training data, preprocessing the data, training the model, evaluating the model, and deploying the model to a production environment.
- **Hypothetical Scenario**: E-commerce Order Processing: Imagine an e-commerce platform. A DAG could automate the order processing workflow. Tasks might include:
  - Receiving order information from the website.
  - Checking inventory levels.
  - Processing payment.
  - Sending order confirmation email to the customer.
  - Updating the shipping system.

#### <a name="chapter1part2.2"></a>Chapter 1 - Part 2.2: Tasks

- A task is a specific instance of an operator. When an operator is assigned to a Dag, it becomes a task.
- Tasks are the actual units of work that get executed when your Dag runs.

Tasks represent individual units of work within a DAG. Each task performs a specific operation, such as executing a script, running a database query, or transferring data.

**Task Definition**

In Airflow, tasks are defined using Operators. An Operator is a template for a specific type of task. When you instantiate an Operator, you create a task.

**Task Attributes**

Tasks have several important attributes:

- ```task_id```: A unique identifier for the task within the DAG. This is used to identify the task in the Airflow UI and when defining task dependencies.
- ```dag```: The DAG to which the task belongs. This is automatically set when you define a task within a DAG context (using the with DAG(...) as dag: syntax).
- ```owner```: The owner of the task. This is typically the user or team responsible for maintaining the task.
- ```retries```: The number of times the task should be retried if it fails.
- ```retry_delay```: The amount of time to wait between retries.
- ```start_date```: The date from which the task should start running.
- ```end_date```: The date when the task should stop running.
- ```depends_on_past```: If set to True, keeps a task from getting triggered if the previous schedule's task did not succeed.
- ```wait_for_downstream```: If set to True, an instance's previous tasks have to be done for their upstream tasks to get triggered.
- ```priority_weight```: Allows relative priorities for tasks amongst all DAGs.
- ```weight_rule```: Weight Rules for assessing task successes.

**Task Dependencies**

Task dependencies define the order in which tasks should be executed. You can define dependencies using the >> (downstream) and << (upstream) operators.

- ```task1 >> task2```: This means that task1 must complete successfully before task2 can start.
- ```task2 << task1```: This is equivalent to task1 >> task2.
- ```[task1, task2] >> task3```: This means that both task1 and task2 must complete successfully before task3 can start.
- ```task1 >> [task2, task3]```: This means that task1 must complete successfully before both task2 and task3 can start.

**Task States**

Tasks can be in one of several states:

- ```queued```: The task is waiting to be executed.
- ```running```: The task is currently being executed.
- ```success```: The task completed successfully.
- ```failed```: The task failed to complete.
- ```skipped```: The task was skipped because a dependency failed or because the task was explicitly skipped.
- ```up_for_retry```: The task failed but will be retried.
- ```up_for_reschedule```: The task is waiting for a sensor to complete.

**Real-World Examples of Tasks**

- **Data Transformation**: A task could be used to transform data from one format to another (e.g., CSV to JSON).
- **Database Query**: A task could be used to execute a SQL query against a database.
- **API Call**: A task could be used to make a call to an external API.
- **Hypothetical Scenario**: Social Media Analytics: Imagine a company analyzing social media trends. Tasks could include:
  - Fetching data from Twitter API.
  - Cleaning and pre-processing the text data.
  - Performing sentiment analysis.
  - Storing the results in a database.

#### <a name="chapter1part2.3"></a>Chapter 1 - Part 2.3: Operators

- An operator defines a single, ideally idempotent task in your Dag (Idempotent means that you can run this task, this operator as many times as you want for the same input.)
- Operators allow you to break down your workflow into discrete, manageable pieces of work.
- Airflow has thousands of operators.
  - The PythonOperator to execute a Python script or function.
  - The BashOperator to execute a bash script, or command
  - The SQLExecuteQueryOperator to execute a SQL query to a database
  - The FileSensor to wait for a file
 
**Tasks vs. operators**

Operators provide the implementation of a piece of work. Airflow has a class called BaseOperator and many subclasses inheriting from the BaseOperator, such as PythonOperator, EmailOperator, and OracleOperator. Tasks in Airflow manage the execution of an operator;
they can be thought of as a small wrapper or manager around an operator that ensures the operator executes correctly. The user can focus on the work to be done by using operators, while Airflow ensures correct execution of the work via tasks.

- Operators define what a task does, while tasks are the actual instances of these actions that get executed within a DAG.
- Operators are reusable templates, whereas tasks are tied to a specific workflow and its execution.

- **Operator**: PythonOperator defines the action of running a Python function.
- **Task**: When you assign the PythonOperator to a DAG, it becomes a task, like process_data_task, and represents the specific step of running that Python function in the workflow.

Operators are the building blocks of tasks in Airflow. They are pre-built templates that encapsulate common operations, such as executing a Bash command, running a Python function, or transferring data between systems.

**Types of Operators**

Airflow provides a wide range of operators for different purposes. Some of the most commonly used operators include:

- ```BashOperator```: Executes a Bash command.
- ```PythonOperator```: Executes a Python function.
- ```EmailOperator```: Sends an email.
- ```SimpleHttpOperator```: Makes an HTTP request.
- ```PostgresOperator```: Executes a SQL command in a Postgres database.
- ```MySqlOperator```: Executes a SQL command in a MySQL database.
- ```S3FileTransferOperator```: Transfers files between local storage and Amazon S3.
- ```SFTPOperator```: Transfers files to and from SFTP servers.
- ```Sensor```: A special type of operator that waits for a certain condition to be met before proceeding.

**Using Operators**

To use an operator, you need to instantiate it and provide the required parameters. The parameters vary depending on the operator.

**Example of Using the BashOperator**

```py
from airflow.operators.bash import BashOperator

task = BashOperator(
    task_id='my_bash_task',
    bash_command='echo "Hello, World!"'
)
```

In this example, we create a BashOperator task that executes the command echo "Hello, World!". The task_id is set to my_bash_task.

**Example of Using the PythonOperator**

```py
from airflow.operators.python import PythonOperator

def my_python_function():
    print("Hello from Python!")

task = PythonOperator(
    task_id='my_python_task',
    python_callable=my_python_function
)
```

In this example, we create a PythonOperator task that executes the function my_python_function. The task_id is set to my_python_task, and the python_callable parameter is set to the function to be executed.

**Real-World Examples of Operators**

- **Data Extraction**: Using SimpleHttpOperator to extract data from a REST API.
- **Database Operations**: Using PostgresOperator to create tables, insert data, or run complex queries.
- **File Transfers**: Using S3FileTransferOperator to move data between your local file system and AWS S3.
- **Hypothetical Scenario**: Online Advertising Campaign: Imagine automating an online advertising campaign. Operators could be used for:
  - ```SimpleHttpOperator```: Fetching campaign performance data from ad platforms (Google Ads, Facebook Ads).
  - ```PythonOperator```: Processing the data and generating reports.
  - ```EmailOperator```: Sending the reports to stakeholders.
 
#### <a name="chapter1part2.4"></a>Chapter 1 - Part 2.4: Workflow

- A workflow is the entire process defined by your Dag, including all tasks and their dependencies.
- It represents your entire data pipeline showing how all the pieces fit together to achieve your goal

<br>

<div align="center"><img src="img/workflow-w812-h762.png" width=812 height=762><br><sub>Example of a Workflow - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>

When the BashOperator runs, for example, in 1 of janary of 2024, it becomes a Task Instance (TI)

#### <a name="chapter1part3"></a>Chapter 1 - Part 3: Airflow Architecture: Scheduler, Webserver, and Metadata Database

Apache Airflow's architecture is fundamental to understanding how it orchestrates complex workflows. At its core, Airflow relies on three key components: the Scheduler, the Webserver, and the Metadata Database. These components work together to define, schedule, execute, and monitor workflows, making Airflow a powerful tool for data engineering and automation. Understanding how these components interact is crucial for effectively using and managing Airflow in any environment, from local development to large-scale production deployments.

#### <a name="chapter1part3.1"></a>Chapter 1 - Part 3.1: Core Components of Airflow

The Airflow architecture is built around three primary components: the Scheduler, the Webserver, and the Metadata Database. Each component plays a distinct role in the overall functioning of the platform.

**The Web Server**

- The web server provides the user interface (UI) for Airflow, which you access through a web browser to manage, monitor, and interact with your workflows.
  - What it does:
    - Displays DAGs (Directed Acyclic Graphs) and their status.
    - Shows task logs and execution history.
    - Allows manual triggering of tasks and monitoring of task states (success, failure, etc.).
  - Why it's useful: The web UI provides a real-time overview of all running and scheduled workflows, making it easy to troubleshoot, monitor, and maintain workflows.
  - Example:
    - A data engineer uses the Airflow web UI to see which DAGs are running, identify failed tasks, and view detailed logs to understand why a task failed.
 
**The Scheduler**

- The scheduler is the component responsible for determining when tasks should be executed based on their schedule intervals and dependencies.
  - What it does:
    - Constantly checks DAGs and schedules tasks according to the defined intervals (e.g., every hour, daily).
    - Ensures tasks are run in the correct order, respecting task dependencies.
    - Handles retries for failed tasks based on retry policies.
  - Why it's useful: The scheduler ensures that workflows are triggered at the right time and that tasks execute in the right sequence, managing task dependencies automatically.
  - Example:
    - A DAG is scheduled to run every day at midnight. The scheduler ensures the first task (e.g., extracting data) runs at the scheduled time, and subsequent tasks (e.g., data transformation) run after the extraction is complete.
 
**The Meta Database**

- The meta database stores all metadata related to Airflow, such as DAG definitions, task statuses, and execution logs.
  - What it does:
    - Tracks task instances and their current status (e.g., running, succeeded, failed).
    - Stores logs, schedule intervals, retries, and any metadata associated with workflows.
  - Why it's useful: The database acts as Airflow's memory, keeping track of the state of all workflows and allowing Airflow to resume tasks even after failures or restarts.
  - Example:
    - If a task fails, Airflow can retry it because the meta database records task statuses and retry counts. A data analyst can query the database to see the history of task executions.
 
**The Triggerer**

- The triggerer manages deferrable tasks, which are tasks that need to wait for an external event to occur before they can continue (e.g., waiting for a file to be uploaded).
  - What it does:
    - Allows Airflow to manage tasks that are in a "waiting" state without consuming unnecessary resources.
    - Efficiently handles tasks waiting for external conditions (such as an external file or database query result).
  - Why it's useful: The triggerer ensures that Airflow can handle tasks that need to wait for external triggers without using up worker resources.
  - Example:
    - A task waits for a file to arrive in an Amazon S3 bucket. Instead of holding a worker, the triggerer waits for the event (the file upload) and then triggers the next task once the event occurs.
 
**The Executor**

- The executor is responsible for deciding how and where tasks are executed. It manages whether tasks are run sequentially or in parallel, and how they are distributed across systems.
  - What it does:
    - Executes tasks based on available resources and task scheduling.
    - Depending on the executor used (e.g., SequentialExecutor, LocalExecutor, CeleryExecutor), tasks can be run locally, in parallel, or across distributed systems.
  - Why it's useful: Executors allow Airflow to scale, determining the strategy for executing tasks. Executors also decide how to handle parallelism or distribute work across a cluster of worker machines.
  - Example:
    - If you’re using the CeleryExecutor, tasks can be distributed across multiple worker nodes in a cluster, allowing for parallel task execution in a scalable manner.

**The Queue**

- The queue is where tasks wait before they are executed by a worker.
  - What it does:
    - Holds tasks that are ready to be executed but are waiting for resources (like workers) to become available.
    - Manages task prioritization and execution order, especially in cases where there are more tasks than available workers.
  - Why it's useful: Queues help manage task execution in environments where resources are shared or limited, ensuring that tasks are run in the correct order.
  - Example:
    - A DAG has multiple tasks, but only a few workers are available. Tasks are placed in a queue, and once a worker becomes available, the next task in line is executed.
 
**The Worker**

- The worker is the process that actually performs the tasks defined in the DAG.
  - What it does:
    - Executes the actual task logic (e.g., running a Python function, executing a shell command, or interacting with an external API).
    - Retrieves tasks from the queue and performs the required work, reporting the results back to Airflow (success, failure, etc.).
  - Why it's useful: Workers are responsible for the actual execution of tasks. Without workers, tasks would not get executed, and DAGs would remain incomplete.
  - Example:
    - A worker processes a task that involves downloading a file from an external API and saving it to a local directory. Once the worker completes the task, it reports success, and the scheduler can trigger the next dependent task.

#### <a name="chapter1part3.2"></a>Chapter 1 - Part 3.2: Interaction Between Components

**Defining pipelines flexibly in (Python) code**

In Airflow, you define your DAGs using Python code in DAG files, which are essentially Python scripts that describe the structure of the corresponding DAG. As such, each DAG file typically describes the set of tasks for a given DAG and the dependencies between the tasks, which are then parsed by Airflow to identify the DAG structure. Other than this, DAG files typically contain some additional metadata about the DAG telling Airflow how and when it should be executed, and so on. We’ll dive into this scheduling more in the next section.

**Scheduling and executing pipelines**

Once you’ve defined the structure of your pipeline(s) as DAG(s), Airflow allows you to define a schedule interval for each DAG, which determines exactly when your pipeline is run by Airflow. This way, you can tell Airflow to execute your DAG every hour, every day, every week, and so on, or even use more complicated schedule intervals based on Cron-like expressions.

At a high level, Airflow is organized into three main components:

- The Airflow scheduler—Parses DAGs, checks their schedule interval, and (if the DAGs’ schedule has passed) starts scheduling the DAGs’ tasks for execution by passing them to the Airflow workers.
- The Airflow workers—Pick up tasks that are scheduled for execution and execute them. As such, the workers are responsible for actually “doing the work.”
- The Airflow webserver—Visualizes the DAGs parsed by the scheduler and provides the main interface for users to monitor DAG runs and their results.

At a high level, the scheduler runs through the following steps

- Once users have written their workflows as DAGs, the files containing these DAGs are read by the scheduler to extract the corresponding tasks, dependencies, and schedule interval of each DAG.
- For each DAG, the scheduler then checks whether the schedule interval for the DAG has passed since the last time it was read. If so, the tasks in the DAG are scheduled for execution.
- For each scheduled task, the scheduler then checks whether the dependencies (= upstream tasks) of the task have been completed. If so, the task is added to the execution queue.
- The scheduler waits for several moments before starting a new loop by jumping back to step 1.

<br>

<div align="center"><img src="img/airflowoverviewprocess-w1121-h657.png" width=1121 height=657><br><sub>Airflow overview Process - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>

- **DAG Definition**: DAGs are defined in Python files and placed in the DAGs folder.
- **Scheduler Parsing**: The Scheduler periodically parses these DAG files to identify DAGs and tasks.
- **Metadata Storage**: The DAG definitions are stored in the Metadata Database.
- **DAG Run Triggering**: Based on the schedule_interval, the Scheduler triggers DAG runs.
- **Task Execution**: The Scheduler submits tasks to the Executor for execution.
- **Status Updates**: The Executor updates the status of tasks in the Metadata Database.
- **Webserver Monitoring**: The Webserver retrieves DAG and task status from the Metadata Database and displays it in the UI.
- **User Interaction**: Users can interact with Airflow through the Webserver to monitor DAG runs, view logs, and manage connections and variables.


#### <a name="chapter1part3.3"></a>Chapter 1 - Part 3.3: Executors

While not one of the three core components, the Executor is a crucial part of the Airflow architecture. The Executor is responsible for actually running the tasks that the Scheduler assigns to it. Different types of Executors exist, each suited for different environments and workloads. We will cover Executors in more detail in a later module, but it's important to understand their basic role in the overall architecture.

#### <a name="chapter1part3.4"></a>Chapter 1 - Part 3.4: Architectures in Airflow

Airflow can run in both single-node and multi-node setups, with each setup having distinct architectural differences. Here's a breakdown of each architecture:

**Single-Node Airflow Architecture**

- In a single-node setup, all Airflow components (Webserver, Scheduler, Metadata Database, and Worker) run on a single machine.
- This is typically used for small-scale deployments, testing, or development environments.
- Core Components:
  - Webserver:
    - The web-based user interface (UI) where you can monitor DAGs, view logs, and manage tasks.
    - In a single-node setup, it runs on the same machine as the other components.
  - Scheduler:
    - Responsible for scheduling DAG runs and ensuring tasks are executed based on their defined schedule intervals.
    - In a single-node architecture, the scheduler runs on the same machine as the webserver and workers.
  - Metadata Database:
    - Stores metadata about DAGs, tasks, and their execution history. Airflow uses databases like MySQL or PostgreSQL.
    - The metadata database is hosted locally on the same machine in this setup.
  - Worker:
    - Executes the actual tasks of the DAG. The tasks are processed in parallel using the machine's available resources.
    - In a single-node setup, there is only one worker, which runs on the same machine as all other components.

- Positve:
  - Simpler to manage: All components are on one machine, making it easier to deploy, set up, and troubleshoot.
  - Good for development: Perfect for development or small-scale workflows, where scaling or distributed execution isn’t required.
- Limitations:
  - Limited scalability: A single machine can only handle so many tasks simultaneously due to hardware constraints.
  - Single point of failure: If the machine goes down, all Airflow services stop.
 
**Multi-Node Airflow Architecture**

- In a multi-node setup, Airflow components are distributed across different machines. This allows Airflow to handle larger workloads by running multiple workers across multiple machines.
- This is typically used in production environments where high availability, fault tolerance, and scalability are critical.
- Core Components:
  - Webserver (Single Instance):
    - The user interface remains centralized and usually runs on a dedicated machine, allowing users to monitor workflows.
    - The Webserver is stateless, so it can run independently without being involved in task execution.
  - Scheduler (Single Instance or Highly Available Mode):
    - The Scheduler is responsible for queuing tasks. In a multi-node setup, it runs separately from workers.
    - In larger setups, you might also set up a highly available mode with multiple schedulers running in active/passive mode to prevent any single point of failure.
  - Metadata Database (Single Instance):
    - The centralized database that tracks the state of the tasks and DAGs.
    - This is usually hosted on a dedicated machine and can be scaled separately using database replication techniques.
  - Worker (Multiple Instances):
    - Workers are distributed across different machines (nodes), allowing them to execute tasks in parallel, thereby increasing the processing capacity.
    - Workers pull tasks from the task queue and execute them. This multi-node worker setup allows you to scale the number of workers based on the workload.
    - You can use distributed systems like Celery or Kubernetes to manage these workers.
  - Message Broker (e.g., RabbitMQ, Redis):
    - In a multi-node setup, tasks are queued in a message broker (like RabbitMQ or Redis) to distribute the load among the workers.
    - The message broker ensures communication between the Scheduler and the distributed Workers.

- Positive:
  - Scalability: You can add more worker nodes to handle an increasing workload without overwhelming a single machine.
  - Fault Tolerance: If one worker node fails, other worker nodes can continue processing tasks, increasing system reliability.
  - Performance: By distributing tasks across multiple machines, you can process workflows faster, improving throughput.
- Limitations:
  - Complexity: Multi-node setups require more configuration and maintenance. Setting up and monitoring multiple nodes and components adds overhead.
  - Resource Intensive: You’ll need to allocate more resources (multiple machines or cloud instances) to manage the infrastructure.
 
  **Use Case Scenarios**

- Single-node: Suitable for small development environments where workflows and tasks are minimal and don't require much scalability.
- Multi-node: Ideal for production environments with large-scale data pipelines, high availability needs, and distributed task execution requirements.

#### <a name="chapter1part4"></a>Chapter 1 - Part 4: Setting up a Local Airflow Environment (using Docker)

Setting up a local Airflow environment is crucial for learning, experimenting, and developing DAGs without affecting production systems. Docker provides an isolated and reproducible environment, ensuring consistency across different machines. This lesson will guide you through setting up Airflow using Docker, covering the necessary steps and configurations to get you started. By the end of this lesson, you'll have a fully functional Airflow instance running locally, ready for you to build and test your workflows.

#### <a name="chapter1part4.1"></a>Chapter 1 - Part 4.1: Understanding Docker for Airflow

Docker is a platform that uses containerization to package an application and all its dependencies together into a standardized unit for software development. An Airflow Docker setup encapsulates the Airflow scheduler, web server, worker processes, and metadata database within containers. This approach offers several advantages:

- **Isolation**: Each Airflow component runs in its own container, preventing conflicts with other software on your system.
- **Reproducibility**: The Docker image ensures that the Airflow environment is consistent across different machines, regardless of the underlying operating system.
- **Simplified Setup**: Docker streamlines the installation process, eliminating the need to manually install and configure Airflow's dependencies.
- **Scalability**: Docker Compose allows you to easily scale individual Airflow components as needed.

**Docker Concepts: Images and Containers**

It's important to understand the distinction between Docker images and containers:

- **Docker Image**: A read-only template that contains instructions for creating a container. Think of it as a blueprint for your Airflow environment.
- **Docker Container**: A runnable instance of an image. It's the actual running Airflow environment.

**Why Docker Compose?**

Docker Compose is a tool for defining and running multi-container Docker applications. In the context of Airflow, Docker Compose simplifies the process of managing the various Airflow components (scheduler, webserver, database) as a single unit. It uses a YAML file (docker-compose.yaml) to define the services, networks, and volumes required for the application.

#### <a name="chapter1part4.2"></a>Chapter 1 - Part 4.2: Prerequisites

**Development Environment Setup on Windows**

1 Install Python on Windows

  - Download the latest version of Python from the official Python website.
  - During installation
    - Check the box "Add Python to PATH".
    - Select the option to install for all users and install Python.
    - Verify Python installation by opening Command Prompt and typing
    - ```python --version```
  - Install pip (Python’s package installer)
    - If pip isn't installed automatically, you can manually install it
    - ```python -m ensurepip --upgrade```

2 Install Virtual Environment (venv)

  - Create a virtual environment to isolate your Python dependencies
    - Open Command Prompt or PowerShell
    - Navigate to your project directory
    - ```cd path\to\your\project```
    - Create a virtual environment using venv
    - ```python -m venv venv```
    - Activate the virtual environment
    - ```.\venv\Scripts\activate```

3 Install Python Packages

  - Once the virtual environment is activated, you can install necessary packages using pip
    - If you have a requirements.txt file, you can install all required packages
    - ```pip install -r requirements.txt```
    - Otherwise, install packages manually (e.g., Airflow)
    - ```pip install apache-airflow```

4 Install Docker

  - Download and install Docker Desktop for Windows from the official Docker website
  - After installation, verify Docker is running by typing in Command Prompt or PowerShell
  - ```docker --version```
  - To use Docker Compose, ensure it is installed by default with Docker Desktop
  - ```docker-compose --version```


**Development Environment Setup on Linux**

1 Install Python on Linux

  - Update the system.
  - ```sudo apt update && sudo apt upgrade```
  - Install Python (if not already installed)
  - ```sudo apt install python3 python3-pip python3-venv```
  - Verify installation
  - ```python3 --version```
  - ```pip3 --version```

2 Install Virtual Environment (venv)

  - Create a virtual environment to isolate your Python dependencies
    - Navigate to your project directory
    - ```cd ~/path/to/your/project```
    - Create a virtual environment using venv
    - ```python3 -m venv venv```
    - Activate the virtual environment
    - ```source venv/bin/activate```

3 Install Python Packages

  - Once the virtual environment is activated, you can install necessary packages using pip
    - If you have a requirements.txt file, you can install all required packages
    - ```pip install -r requirements.txt```
    - Otherwise, install packages manually (e.g., Airflow)
    - ```pip install apache-airflow```

4 Install Docker

  - Update system and install Docker
  - ```sudo apt update```
  - ```sudo apt install docker.io```
  - Start and enable Docker
  - ```sudo systemctl start docker```
  - ```sudo systemctl enable docker```
  - Verify Docker installation
  - ```docker --version```
  - Install Docker Compose
  - ```sudo curl -L "https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose```
  - ```sudo chmod +x /usr/local/bin/docker-compose```
  - ```docker-compose --version```

#### <a name="chapter1part4.3"></a>Chapter 1 - Part 4.3: Setting Up Airflow with Docker Compose

The most common and recommended way to set up Airflow locally is by using the official Airflow Docker image and Docker Compose.

**Creating the docker-compose.yaml File**

Create a new directory for your Airflow project and create a docker-compose.yaml file within it. This file will define the services needed for Airflow.

```yaml
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#

# Basic Airflow cluster configuration for CeleryExecutor with Redis and PostgreSQL.
#
# WARNING: This configuration is for local development. Do not use it in a production deployment.
#
# This configuration supports basic configuration using environment variables or an .env file
# The following variables are supported:
#
# AIRFLOW_IMAGE_NAME           - Docker image name used to run Airflow.
#                                Default: apache/airflow:2.5.1
# AIRFLOW_UID                  - User ID in Airflow containers
#                                Default: 50000
# AIRFLOW_PROJ_DIR             - Base path to which all the files will be volumed.
#                                Default: .
# Those configurations are useful mostly in case of standalone testing/running Airflow in test/try-out mode
#
# _AIRFLOW_WWW_USER_USERNAME   - Username for the administrator account (if requested).
#                                Default: airflow
# _AIRFLOW_WWW_USER_PASSWORD   - Password for the administrator account (if requested).
#                                Default: airflow
# _PIP_ADDITIONAL_REQUIREMENTS - Additional PIP requirements to add when starting all containers.
#                                Default: ''
#
# Feel free to modify this file to suit your needs.
---
version: '3'
x-airflow-common:
  &airflow-common
  # In order to add custom dependencies or upgrade provider packages you can use your extended image.
  # Comment the image line, place your Dockerfile in the directory where you placed the docker-compose.yaml
  # and uncomment the "build" line below, Then run `docker-compose build` to build the images.
  image: ${AIRFLOW_IMAGE_NAME:-apache/airflow:2.5.1}
  # build: .
  environment:
    &airflow-common-env
    AIRFLOW__CORE__EXECUTOR: CeleryExecutor
    AIRFLOW__DATABASE__SQL_ALCHEMY_CONN: postgresql+psycopg2://airflow:airflow@postgres/airflow
    # For backward compatibility, with Airflow <2.3
    AIRFLOW__CORE__SQL_ALCHEMY_CONN: postgresql+psycopg2://airflow:airflow@postgres/airflow
    AIRFLOW__CELERY__RESULT_BACKEND: db+postgresql://airflow:airflow@postgres/airflow
    AIRFLOW__CELERY__BROKER_URL: redis://:@redis:6379/0
    AIRFLOW__CORE__FERNET_KEY: ''
    AIRFLOW__CORE__DAGS_ARE_PAUSED_AT_CREATION: 'true'
    AIRFLOW__CORE__LOAD_EXAMPLES: 'true'
    AIRFLOW__API__AUTH_BACKENDS: 'airflow.api.auth.backend.basic_auth,airflow.api.auth.backend.session'
    _PIP_ADDITIONAL_REQUIREMENTS: ${_PIP_ADDITIONAL_REQUIREMENTS:-}
  volumes:
    - ${AIRFLOW_PROJ_DIR:-.}/dags:/opt/airflow/dags
    - ${AIRFLOW_PROJ_DIR:-.}/logs:/opt/airflow/logs
    - ${AIRFLOW_PROJ_DIR:-.}/plugins:/opt/airflow/plugins
  user: "${AIRFLOW_UID:-50000}:0"
  depends_on:
    &airflow-common-depends-on
    redis:
      condition: service_healthy
    postgres:
      condition: service_healthy

services:
  postgres:
    image: postgres:13
    environment:
      POSTGRES_USER: airflow
      POSTGRES_PASSWORD: airflow
      POSTGRES_DB: airflow
    volumes:
      - postgres-db-volume:/var/lib/postgresql/data
    healthcheck:
      test: ["CMD", "pg_isready", "-U", "airflow"]
      interval: 5s
      retries: 5
    restart: always

  redis:
    image: redis:latest
    expose:
      - 6379
    healthcheck:
      test: ["CMD", "redis-cli", "ping"]
      interval: 5s
      timeout: 30s
      retries: 50
    restart: always

  airflow-webserver:
    <<: *airflow-common
    command: webserver
    ports:
      - 8080:8080
    healthcheck:
      test: ["CMD", "curl", "--fail", "http://localhost:8080/health"]
      interval: 10s
      timeout: 10s
      retries: 5
    restart: always
    depends_on:
      <<: *airflow-common-depends-on
      airflow-init:
        condition: service_completed_successfully

  airflow-scheduler:
    <<: *airflow-common
    command: scheduler
    healthcheck:
      test: ["CMD-SHELL", 'airflow jobs check --job-type SchedulerJob --hostname "$${HOSTNAME}"']
      interval: 10s
      timeout: 10s
      retries: 5
    restart: always
    depends_on:
      <<: *airflow-common-depends-on
      airflow-init:
        condition: service_completed_successfully

  airflow-worker:
    <<: *airflow-common
    command: celery worker
    healthcheck:
      test:
        - "CMD-SHELL"
        - 'celery --app airflow.executors.celery_executor.app inspect ping -d "celery@$${HOSTNAME}"'
      interval: 10s
      timeout: 10s
      retries: 5
    environment:
      <<: *airflow-common-env
      # Required to handle warm shutdown of the celery workers properly
      # See https://airflow.apache.org/docs/docker-stack/entrypoint.html#signal-propagation
      DUMB_INIT_SETSID: "0"
    restart: always
    depends_on:
      <<: *airflow-common-depends-on
      airflow-init:
        condition: service_completed_successfully

  airflow-triggerer:
    <<: *airflow-common
    command: triggerer
    healthcheck:
      test: ["CMD-SHELL", 'airflow jobs check --job-type TriggererJob --hostname "$${HOSTNAME}"']
      interval: 10s
      timeout: 10s
      retries: 5
    restart: always
    depends_on:
      <<: *airflow-common-depends-on
      airflow-init:
        condition: service_completed_successfully

  airflow-init:
    <<: *airflow-common
    entrypoint: /bin/bash
    # yamllint disable rule:line-length
    command:
      - -c
      - |
        function ver() {
          printf "%04d%04d%04d%04d" $${1//./ }
        }
        airflow_version=$$(AIRFLOW__LOGGING__LOGGING_LEVEL=INFO && gosu airflow airflow version)
        airflow_version_comparable=$$(ver $${airflow_version})
        min_airflow_version=2.2.0
        min_airflow_version_comparable=$$(ver $${min_airflow_version})
        if (( airflow_version_comparable < min_airflow_version_comparable )); then
          echo
          echo -e "\033[1;31mERROR!!!: Too old Airflow version $${airflow_version}!\e[0m"
          echo "The minimum Airflow version supported: $${min_airflow_version}. Only use this or higher!"
          echo
          exit 1
        fi
        if [[ -z "${AIRFLOW_UID}" ]]; then
          echo
          echo -e "\033[1;33mWARNING!!!: AIRFLOW_UID not set!\e[0m"
          echo "If you are on Linux, you SHOULD follow the instructions below to set "
          echo "AIRFLOW_UID environment variable, otherwise files will be owned by root."
          echo "For other operating systems you can get rid of the warning with manually created .env file:"
          echo "    See: https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html#setting-the-right-airflow-user"
          echo
        fi
        one_meg=1048576
        mem_available=$$(($$(getconf _PHYS_PAGES) * $$(getconf PAGE_SIZE) / one_meg))
        cpus_available=$$(grep -cE 'cpu[0-9]+' /proc/stat)
        disk_available=$$(df / | tail -1 | awk '{print $$4}')
        warning_resources="false"
        if (( mem_available < 4000 )) ; then
          echo
          echo -e "\033[1;33mWARNING!!!: Not enough memory available for Docker.\e[0m"
          echo "At least 4GB of memory required. You have $$(numfmt --to iec $$((mem_available * one_meg)))"
          echo
          warning_resources="true"
        fi
        if (( cpus_available < 2 )); then
          echo
          echo -e "\033[1;33mWARNING!!!: Not enough CPUS available for Docker.\e[0m"
          echo "At least 2 CPUs recommended. You have $${cpus_available}"
          echo
          warning_resources="true"
        fi
        if (( disk_available < one_meg * 10 )); then
          echo
          echo -e "\033[1;33mWARNING!!!: Not enough Disk space available for Docker.\e[0m"
          echo "At least 10 GBs recommended. You have $$(numfmt --to iec $$((disk_available * 1024 )))"
          echo
          warning_resources="true"
        fi
        if [[ $${warning_resources} == "true" ]]; then
          echo
          echo -e "\033[1;33mWARNING!!!: You have not enough resources to run Airflow (see above)!\e[0m"
          echo "Please follow the instructions to increase amount of resources available:"
          echo "   https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html#before-you-begin"
          echo
        fi
        mkdir -p /sources/logs /sources/dags /sources/plugins
        chown -R "${AIRFLOW_UID}:0" /sources/{logs,dags,plugins}
        exec /entrypoint airflow version
    # yamllint enable rule:line-length
    environment:
      <<: *airflow-common-env
      _AIRFLOW_DB_UPGRADE: 'true'
      _AIRFLOW_WWW_USER_CREATE: 'true'
      _AIRFLOW_WWW_USER_USERNAME: ${_AIRFLOW_WWW_USER_USERNAME:-airflow}
      _AIRFLOW_WWW_USER_PASSWORD: ${_AIRFLOW_WWW_USER_PASSWORD:-airflow}
      _PIP_ADDITIONAL_REQUIREMENTS: ''
    user: "0:0"
    volumes:
      - ${AIRFLOW_PROJ_DIR:-.}:/sources

  airflow-cli:
    <<: *airflow-common
    profiles:
      - debug
    environment:
      <<: *airflow-common-env
      CONNECTION_CHECK_MAX_COUNT: "0"
    # Workaround for entrypoint issue. See: https://github.com/apache/airflow/issues/16252
    command:
      - bash
      - -c
      - airflow

  # You can enable flower by adding "--profile flower" option e.g. docker-compose --profile flower up
  # or by explicitly targeted on the command line e.g. docker-compose up flower.
  # See: https://docs.docker.com/compose/profiles/
  flower:
    <<: *airflow-common
    command: celery flower
    profiles:
      - flower
    ports:
      - 5555:5555
    healthcheck:
      test: ["CMD", "curl", "--fail", "http://localhost:5555/"]
      interval: 10s
      timeout: 10s
      retries: 5
    restart: always
    depends_on:
      <<: *airflow-common-depends-on
      airflow-init:
        condition: service_completed_successfully

volumes:
  postgres-db-volume:
```

**Explanation of the docker-compose.yaml File**

- ```x-airflow-common```: Defines common configurations for Airflow services, such as the image, environment variables, volumes, and user ID.
- ```postgres```: This service runs a PostgreSQL database, which Airflow uses to store metadata about DAGs, tasks, and runs.
- ```redis```: This service runs a Redis server, which is used as the Celery broker.
- ```airflow-webserver```: This service runs the Airflow web server, which provides a user interface for managing and monitoring DAGs.
- ```airflow-scheduler```: This service runs the Airflow scheduler, which is responsible for scheduling and executing DAGs.
- ```airflow-worker```: This service runs the Airflow worker, which executes the tasks defined in the DAGs.
- ```airflow-triggerer```: The airflow-triggerer is a crucial component for running asynchronous operators in Airflow.
- ```airflow-init```: This service runs a script to initialize the Airflow database, create a user, and ensure proper file permissions.
- Volumes: The volumes section maps the dags, logs, and plugins directories on your host machine to the corresponding directories in the containers.
- Environment Variables: Environment variables such as AIRFLOW__CORE__EXECUTOR and AIRFLOW__DATABASE__SQL_ALCHEMY_CONN configure Airflow's behavior.

**Step-by-Step Guide**

- **Create a Directory**: Create a new directory for your Airflow project.

```
mkdir airflow-docker-setup
cd airflow-docker-setup
```

- **Create a python virtual enviroment in this folder** (If Windows ```python -m venv venv```, if Linux ```python3 -m venv venv```)

- **Active the virtual enviroment** (If Windows ```.\venv\Scripts\activate```, if Linux ```source venv/bin/activate````)

- **Save the Docker Compose File**: Save the provided docker-compose.yaml file into this directory.

- **Create .env File (Optional)**: You can create a .env file to override the default environment variables. This is useful for setting your own passwords, user IDs, or Airflow image version.

Here’s an example .env file:

```
AIRFLOW_IMAGE_NAME=apache/airflow:2.4.2
AIRFLOW_UID=50000
```

- **Directory Structure**: Create dags, logs, and plugins folders.

```
mkdir -p dags logs plugins
```

These directories are mounted as volumes in the Docker Compose file, allowing you to add DAGs, check logs, and add plugins easily.

- **Run Docker Compose**: Start the Airflow environment using Docker Compose.

```
docker-compose up -d
```

This command will download the necessary images and start the containers in detached mode.

```
WARN[0000] The "AIRFLOW_UID" variable is not set. Defaulting to a blank string.
WARN[0000] The "AIRFLOW_UID" variable is not set. Defaulting to a blank string.
WARN[0000] /mnt/c/Workspace/airflow-tutorial/docker-compose.yml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion
[+] Running 0/6
 ⠙ airflow-worker Pulling                                                                                          8.2s
 ⠙ redis Pulling                                                                                                   8.2s
 ⠙ airflow-webserver Pulling                                                                                       8.2s
 ⠙ airflow-scheduler Pulling                                                                                       8.2s
 ⠙ airflow-init Pulling                                                                                            8.2s
 ⠙ airflow-triggerer Pulling                                                                                       8.2s
```

- You will see many lines scrolled, wait until it's done. Docker is downloading Airflow to run it. It can take up to 5 mins depending on your connection. If Docker raises an error saying it can't download the docker image, ensure you are not behind a proxy/vpn or corporate network. You may need to use your personal connection to make it work. At the end, you should end up with something like this

```
 ✔ Network airflow-tutorial_default                Created                                                         0.0s
 ✔ Volume "airflow-tutorial_postgres-db-volume"    Created                                                         0.0s
 ✔ Container airflow-tutorial-postgres-1           Healthy                                                         6.9s
 ✔ Container airflow-tutorial-redis-1              Healthy                                                         6.9s
 ✔ Container airflow-tutorial-airflow-init-1       Exited                                                         21.0s
 ✔ Container airflow-tutorial-airflow-scheduler-1  Started                                                        21.8s
 ✔ Container airflow-tutorial-airflow-worker-1     Started                                                        21.8s
 ✔ Container airflow-tutorial-airflow-webserver-1  Started                                                        21.8s
 ✔ Container airflow-tutorial-airflow-triggerer-1  Started                                                        21.8s
```

- If you make a ```docker ps```, you will see this

```
CONTAINER ID   IMAGE                  COMMAND                  CREATED          STATUS                    PORTS                                       NAMES
22c09aea6657   apache/airflow:2.5.1   "/usr/bin/dumb-init …"   53 seconds ago   Up 31 seconds (healthy)   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp   airflow-tutorial-airflow-webserver-1
43a661ab5fda   apache/airflow:2.5.1   "/usr/bin/dumb-init …"   53 seconds ago   Up 31 seconds (healthy)   8080/tcp
                              airflow-tutorial-airflow-triggerer-1
a7b13dd3fbbe   apache/airflow:2.5.1   "/usr/bin/dumb-init …"   53 seconds ago   Up 31 seconds (healthy)   8080/tcp                                    airflow-tutorial-airflow-scheduler-1
763381cd5116   apache/airflow:2.5.1   "/usr/bin/dumb-init …"   53 seconds ago   Up 31 seconds (healthy)   8080/tcp                                    airflow-tutorial-airflow-worker-1
d8a039bfdf66   redis:latest           "docker-entrypoint.s…"   53 seconds ago   Up 52 seconds (healthy)   6379/tcp                                    airflow-tutorial-redis-1
```

- This means, that everthing is ok. Now, open your browser and enter the page ```http://localhost:8080```

- You will enter in the Airflow log in page. Put ```airflow``` as username and password

<br>

<div align="center"><img src="img/airflowuipage-w1913-h440.png" width=1913 height=440><br><sub>Airflow Log In Page - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>

- Now, you you have the DAGs page

<br>

<div align="center"><img src="img/airflowuipage2-w1913-h417.png" width=1913 height=417><br><sub>Airflow Dags Page - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>


- **Check the Status**: Verify that all containers are running correctly.

```
docker-compose ps
```

You should see all services (postgres, redis, airflow-webserver, airflow-scheduler, airflow-worker, airflow-triggerer) listed as running.

- **Access Airflow UI**: Open your web browser and go to http://localhost:8080. Log in with the username and password specified in your .env file or the default (airflow:airflow).

- **Stopping the Environment**: When you're done, you can stop the environment by running:

```
docker-compose down
```

To remove the volumes as well (if you want to reset the environment completely):

```
docker-compose down -v
```

#### <a name="chapter1part4.4"></a>Chapter 1 - Part 4.4: Customizing Your Airflow Environment

The docker-compose.yaml file provides a basic Airflow setup. You can customize it to suit your specific needs.

**Mounting DAGs**

The docker-compose.yaml file mounts the ./dags directory on your host machine to the /opt/airflow/dags directory in the container. This allows you to add DAGs to your Airflow environment by simply placing them in the ./dags directory.

Create a dags directory in your project directory. Any .py files placed in this directory will be recognized as DAGs by Airflow.

**Adding Plugins**

Similarly, the docker-compose.yaml file mounts the ./plugins directory on your host machine to the /opt/airflow/plugins directory in the container. This allows you to add custom operators, hooks, and sensors to your Airflow environment by placing them in the ./plugins directory.

Create a plugins directory in your project directory. Place your plugin files in this directory.

**Configuring Environment Variables**

You can configure Airflow by setting environment variables in the docker-compose.yaml file. The environment section of each service allows you to specify environment variables that will be available to the container.

For example, you can set the AIRFLOW__CORE__EXECUTOR environment variable to LocalExecutor to use the LocalExecutor instead of the CeleryExecutor. However, for a production-like setup, CeleryExecutor is recommended.

**Using a Different Database**

While the docker-compose.yaml file uses PostgreSQL as the metadata database, you can also use other databases, such as MySQL or SQLite. To use a different database, you need to:

- Change the database image in the docker-compose.yaml file.
- Update the AIRFLOW__CORE__SQL_ALCHEMY_CONN environment variable to point to the new database.
- Ensure that the necessary database drivers are installed in the Airflow container.

Using SQLite is generally not recommended for production environments due to its limitations in terms of concurrency and scalability.

#### <a name="chapter1part4.5"></a>Chapter 1 - Part 4.5: Troubleshooting Common Issues

- **Airflow UI not accessible**: Ensure that the Docker containers are running and that the ports are correctly mapped in the docker-compose.yaml file. Check the logs of the airflow-webserver container for any errors.

- **DAGs not showing up**: Ensure that the DAG files are placed in the ./dags directory and that the directory is correctly mounted in the docker-compose.yaml file. Check the logs of the airflow-scheduler container for any errors.

- **Database connection errors**: Ensure that the PostgreSQL database is running and that the AIRFLOW__CORE__SQL_ALCHEMY_CONN environment variable is correctly configured. Check the logs of the Airflow containers for any database connection errors.

- **Permission issues**: Ensure that the user running the Docker containers has the necessary permissions to access the mounted directories.

#### <a name="chapter1part5"></a>Chapter 1 - Part 5: Introduction to the Airflow UI

The Airflow UI is your primary interface for interacting with your Airflow environment. It provides a comprehensive view of your DAGs, tasks, and infrastructure, allowing you to monitor, trigger, and troubleshoot your workflows. Understanding the UI is crucial for effectively managing your data pipelines and ensuring their smooth operation. This lesson will guide you through the key components of the Airflow UI, explaining their functionalities and how to use them to manage your workflows.

#### <a name="chapter1part5.1"></a>Chapter 1 - Part 5.1: Accessing the Airflow UI

After setting up your local Airflow environment using Docker (as covered in the previous lesson), you can access the Airflow UI through your web browser. By default, the Airflow webserver runs on port 8080. Therefore, you can access the UI by navigating to http://localhost:8080 in your browser.

If you configured a different port during the setup process, make sure to use that port instead. Once you access the UI, you'll be prompted to log in. The default credentials are airflow for both username and password. It is crucial to change these default credentials in a production environment for security reasons.

#### <a name="chapter1part5.2"></a>Chapter 1 - Part 5.2: Key Components of the Airflow UI

The Airflow UI is organized into several key sections, each providing specific functionalities for managing your workflows.

**DAGs View**

The DAGs view is the main landing page of the Airflow UI. It provides a list of all DAGs that are currently loaded in your Airflow environment. For each DAG, you can see its current status, schedule, and a summary of recent runs.

- **DAG Name**: The name of the DAG, as defined in your Python code. Clicking on the DAG name will take you to the DAG details page.
- **Status**: The current status of the DAG, which can be one of the following:
  - **Running**: The DAG is currently running.
  - **Success**: The DAG has completed successfully.
  - **Failed**: The DAG has failed.
  - **Upstream Failed**: One or more upstream tasks have failed.
  - **Queued**: The DAG is queued to run.
  - **Scheduled**: The DAG is scheduled to run in the future.
  - **Paused**: The DAG is paused and will not be scheduled to run.
- **Schedule**: The schedule interval for the DAG, defined using a cron expression or a predefined schedule (e.g., @daily, @weekly).
- **Last Run**: The date and time of the last DAG run.
- **Next Run**: The date and time of the next scheduled DAG run.
- **Recent Tasks**: A summary of the status of recent tasks in the DAG, providing a quick overview of the DAG's health.
- **Actions**: A set of actions that you can perform on the DAG, such as:
  - **Trigger DAG**: Manually trigger a new DAG run.
  - **Pause/Unpause DAG**: Pause or unpause the DAG, enabling or disabling its schedule.
  - **Delete DAG**: Remove the DAG from the Airflow environment (use with caution!).
  - **Refresh**: Refresh the DAG's status and information.
 
**Example**:

Imagine you have a DAG named process_data_daily that processes data every day at midnight. In the DAGs view, you would see the DAG name, its status (e.g., "Success" if the last run was successful), the schedule (@daily), the last run time, the next run time, and a summary of the recent task statuses.


**DAG Details View**

Clicking on a DAG name in the DAGs view will take you to the DAG details view. This view provides a more detailed look at the DAG, including its graph representation, task details, and run history.

- **Graph View**: A visual representation of the DAG, showing the tasks and their dependencies. You can see the status of each task (e.g., success, failed, running, queued) and the dependencies between them.
- **Task Details**: Clicking on a task in the graph view will display its details, such as its operator type, start time, end time, duration, and logs.
- **Grid View**: A tabular view of the DAG runs, showing the status of each task in each run. This view is useful for comparing the performance of different DAG runs.
- **Code View**: Displays the Python code that defines the DAG. This is useful for reviewing the DAG's logic and identifying potential issues.
- **Run History**: A list of all DAG runs, showing their status, start time, end time, and duration. You can click on a DAG run to view its details.

**Example**:

In the DAG details view for the process_data_daily DAG, you would see a graph showing the tasks involved in processing the data, such as "extract_data", "transform_data", and "load_data". You could click on the "transform_data" task to see its details, such as the Python code that performs the transformation and the logs generated during its execution.

**Task Instance Details**

From the DAG Details view, you can click on a specific task instance (a specific run of a task within a DAG run) to view its details. This provides the most granular level of information about a task's execution.

- **Logs**: The logs generated by the task during its execution. This is the primary source of information for troubleshooting task failures.
- **Task Attributes**: Information about the task, such as its operator type, retries, start time, end time, duration, and state.
- **XComs**: (Covered in a later module) Information about data passed between tasks using XComs.
- **Try Number**: If the task has been retried, this indicates the current retry attempt number.

**Example**:

If the "transform_data" task in the process_data_daily DAG failed, you would examine its logs in the Task Instance Details view to identify the cause of the failure. The logs might show an error message indicating a problem with the data transformation logic.

**Browse Menu**

The "Browse" menu in the Airflow UI provides access to various administrative and monitoring features.

- **DAG Runs**: A list of all DAG runs in the Airflow environment, across all DAGs.
- **Task Instances**: A list of all task instances in the Airflow environment, across all DAGs and DAG runs.
- **Code**: Allows you to browse the code files in your Airflow environment, including DAG definitions and custom modules.
- **Variables**: (Covered in a later module) Allows you to view and manage Airflow variables, which are key-value pairs that can be used to configure DAGs.
- **Connections**: (Covered in a later module) Allows you to view and manage Airflow connections, which store connection information for external systems such as databases and APIs.
- **Pools**: Allows you to manage resource pools, which can be used to limit the number of tasks that run concurrently.
- **Users**: Allows you to manage user accounts and permissions.
- **Roles**: Allows you to manage user roles and permissions.
- **Audit Logs**: A log of all actions performed in the Airflow UI, providing an audit trail for security and compliance purposes.

**Admin Menu**

The "Admin" menu provides access to administrative functionalities.

- **Configurations**: Displays the current Airflow configuration settings.
- **Plugins**: Displays the installed Airflow plugins.
- **REST API**: Provides information about the Airflow REST API.
- **Clear Data**: Allows you to clear data from the Airflow metadata database (use with caution!).

#### <a name="chapter1part5.3"></a>Chapter 1 - Part 5.3: Using the Airflow UI for Monitoring and Troubleshooting

The Airflow UI is your primary tool for monitoring the health and performance of your data pipelines. By regularly checking the DAGs view, DAG details view, and task instance details, you can quickly identify and resolve issues.

- **Monitoring DAG Status**: The DAGs view provides a quick overview of the status of all DAGs. Pay attention to DAGs that are in a "Failed" or "Upstream Failed" state.
- **Examining Task Logs**: When a task fails, the first step is to examine its logs in the Task Instance Details view. The logs will often contain error messages or stack traces that can help you identify the cause of the failure.
- **Identifying Performance Bottlenecks**: The DAG details view and Grid View can help you identify performance bottlenecks in your DAGs. Look for tasks that take a long time to run or that are frequently retried.
- **Triggering DAGs Manually**: You can use the "Trigger DAG" button in the DAGs view to manually trigger a DAG run. This is useful for testing changes or for running a DAG on demand.
- **Clearing Task Instances**: If a task instance is in a failed state and you want to retry it, you can clear it using the "Clear" button in the Task Instance Details view. This will reset the task's state and allow it to be retried.

## <a name="chapter2"></a>Chapter 2: Building Your First DAG

#### <a name="chapter2part1"></a>Chapter 2 - Part 1: Defining a Simple DAG: A "Hello World" Example

Defining a DAG is the foundational step in using Apache Airflow. A DAG, or Directed Acyclic Graph, represents a workflow, a series of tasks you want to execute. This lesson will guide you through creating a simple "Hello World" DAG, introducing you to the core concepts and syntax required to define your own workflows. We'll cover the essential components of a DAG, including defining tasks and setting dependencies, laying the groundwork for more complex workflows in later lessons.

#### <a name="chapter2part1.1"></a>Chapter 2 - Part 1.1: Understanding the Basic Structure of a DAG

A DAG in Airflow is defined using Python code. The code specifies the tasks to be executed and their dependencies. Let's break down the fundamental components:

- **DAG Definition**: The DAG() object is the entry point for defining your workflow. It encapsulates all the tasks and their relationships.
- **Tasks**: Tasks represent individual units of work. They are defined using Operators (e.g., BashOperator, PythonOperator).
- **Task Dependencies**: Dependencies define the order in which tasks are executed. You can specify that a task should run only after another task has completed successfully.

**DAG Definition with Context Manager**

The most common and recommended way to define a DAG is using a context manager (with DAG(...) as dag:). This approach automatically associates tasks defined within the with block with the DAG.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='hello_world_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,  # Set to None for manual triggering
    catchup=False,
    tags=['example']
) as dag:
    # Define tasks within this block
    pass # Placeholder for tasks
```

Let's break down the parameters used in the DAG() constructor:

- **dag_id**: A unique identifier for your DAG. This is how Airflow identifies and manages your workflow.
- **start_date**: The date from which Airflow will start scheduling DAG runs. It's crucial to set this correctly, especially when using schedules.
- **schedule_interval**: Defines how often the DAG should run. None means the DAG will only be triggered manually. Other options include cron expressions (e.g., "0 0 * * *") or predefined schedules like "@daily". We'll explore scheduling in more detail in a later lesson.
- **catchup**: Determines whether Airflow should backfill DAG runs for past dates if the start_date is in the past. Setting it to False prevents backfilling.
- **tags**: A list of tags that can be used to categorize and filter DAGs in the Airflow UI.

**Defining Tasks Using Operators**

Operators are the building blocks of Airflow DAGs. They represent a single, ideally idempotent, task. The BashOperator is a simple operator that executes a bash command.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='hello_world_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example']
) as dag:
    # Define a task that executes a bash command
    hello_task = BashOperator(
        task_id='hello_task',
        bash_command='echo "Hello, World!"'
    )
```

In this example:

- **task_id**: A unique identifier for the task within the DAG.
- **bash_command**: The bash command to be executed.

**Setting Task Dependencies**

Task dependencies define the order in which tasks are executed. Airflow provides several ways to define dependencies:

- **Using the >> operator**: This is the most common and readable way to define dependencies. It indicates that the task on the left should run before the task on the right.
- **Using the << operator**: This is the reverse of the >> operator. It indicates that the task on the right should run before the task on the left.
- **Using the set_upstream() method**: This method explicitly sets a task as a dependency of another task.
- **Using the set_downstream() method**: This method explicitly sets a task as a dependent of another task.

Let's add another task and define a dependency:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='hello_world_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example']
) as dag:
    # Define a task that executes a bash command
    hello_task = BashOperator(
        task_id='hello_task',
        bash_command='echo "Hello, World!"'
    )

    # Define another task
    goodbye_task = BashOperator(
        task_id='goodbye_task',
        bash_command='echo "Goodbye, World!"'
    )

    # Define the task dependency: hello_task runs before goodbye_task
    hello_task >> goodbye_task
```

This code defines two tasks: hello_task and goodbye_task. The hello_task >> goodbye_task line specifies that hello_task must complete successfully before goodbye_task can start.

#### <a name="chapter2part1.2"></a>Chapter 2 - Part 1.2: Practical Examples and Demonstrations

Let's explore some more practical examples to solidify your understanding.

**Example 1: Printing the Current Date**

This example demonstrates how to use the BashOperator to print the current date.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='date_printer_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example']
) as dag:
    # Define a task that prints the current date
    print_date = BashOperator(
        task_id='print_date',
        bash_command='date'
    )
```

This DAG defines a single task, print_date, which executes the date command in bash.

**Example 2: Creating a Directory and a File**

This example demonstrates how to create a directory and a file using the BashOperator.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='create_directory_and_file_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example']
) as dag:
    # Define a task that creates a directory
    create_directory = BashOperator(
        task_id='create_directory',
        bash_command='mkdir -p /tmp/my_directory'
    )

    # Define a task that creates a file inside the directory
    create_file = BashOperator(
        task_id='create_file',
        bash_command='touch /tmp/my_directory/my_file.txt'
    )

    # Define the task dependency: create_directory runs before create_file
    create_directory >> create_file
```

This DAG defines two tasks: create_directory and create_file. The create_directory task creates a directory named /tmp/my_directory. The create_file task creates a file named /tmp/my_directory/my_file.txt inside the directory. The dependency ensures that the directory is created before the file.

**Example 3: Using Multiple Dependencies**

This example demonstrates how to define multiple dependencies for a task.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='multiple_dependencies_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example']
) as dag:
    # Define three tasks
    task_1 = BashOperator(
        task_id='task_1',
        bash_command='echo "Task 1"'
    )

    task_2 = BashOperator(
        task_id='task_2',
        bash_command='echo "Task 2"'
    )

    task_3 = BashOperator(
        task_id='task_3',
        bash_command='echo "Task 3"'
    )

    # Define dependencies: task_1 and task_2 run before task_3
    [task_1, task_2] >> task_3
```

In this example, task_3 depends on both task_1 and task_2. This means that task_3 will only start after both task_1 and task_2 have completed successfully.

#### <a name="chapter2part2"></a>Chapter 2 - Part 2: Understanding Task Dependencies and Workflow Orchestration

Understanding task dependencies and workflow orchestration is crucial for building robust and reliable data pipelines in Airflow. It allows you to define the order in which tasks should be executed, ensuring that data is processed correctly and efficiently. Without proper dependency management, tasks might run out of order, leading to errors or incorrect results. This lesson will delve into the core concepts of task dependencies and workflow orchestration, providing you with the knowledge to design and implement complex workflows effectively.

#### <a name="chapter2part2.1"></a>Chapter 2 - Part 2.1: Defining Task Dependencies

Task dependencies define the order in which tasks within a DAG are executed. Airflow uses these dependencies to determine the execution order, ensuring that tasks are run only when their prerequisites are met. This is essential for data pipelines where the output of one task is often the input for another.

**Basic Dependencies**

The simplest way to define dependencies is using the set_upstream() and set_downstream() methods. These methods establish a direct relationship between two tasks, indicating which task must complete before the other can start.

Example:

```py
from airflow import DAG
from airflow.operators.bash_operator import BashOperator
from datetime import datetime

with DAG('basic_dependencies', start_date=datetime(2023, 1, 1), schedule_interval=None, catchup=False) as dag:
    task_1 = BashOperator(
        task_id='task_1',
        bash_command='echo "Task 1 running"'
    )

    task_2 = BashOperator(
        task_id='task_2',
        bash_command='echo "Task 2 running"'
    )

    task_3 = BashOperator(
        task_id='task_3',
        bash_command='echo "Task 3 running"'
    )

    # Define dependencies
    task_1.set_downstream(task_2)  # Task 2 depends on Task 1
    task_2.set_downstream(task_3)  # Task 3 depends on Task 2
```

In this example, task_2 will only run after task_1 completes successfully, and task_3 will only run after task_2 completes. This creates a linear dependency chain.

**Using Bitshift Operators**

Airflow also supports using bitshift operators (>> and <<) to define dependencies, which can make DAG definitions more readable, especially for complex workflows.

Example:

```py
from airflow import DAG
from airflow.operators.bash_operator import BashOperator
from datetime import datetime

with DAG('bitshift_dependencies', start_date=datetime(2023, 1, 1), schedule_interval=None, catchup=False) as dag:
    task_1 = BashOperator(
        task_id='task_1',
        bash_command='echo "Task 1 running"'
    )

    task_2 = BashOperator(
        task_id='task_2',
        bash_command='echo "Task 2 running"'
    )

    task_3 = BashOperator(
        task_id='task_3',
        bash_command='echo "Task 3 running"'
    )

    # Define dependencies using bitshift operators
    task_1 >> task_2 >> task_3  # Equivalent to task_1.set_downstream(task_2) and task_2.set_downstream(task_3)
```

The >> operator means "downstream of," so task_1 >> task_2 means task_2 depends on task_1.

**Multiple Dependencies**

Tasks can have multiple upstream and downstream dependencies, allowing for more complex workflow structures.

Example:

```py
from airflow import DAG
from airflow.operators.bash_operator import BashOperator
from datetime import datetime

with DAG('multiple_dependencies', start_date=datetime(2023, 1, 1), schedule_interval=None, catchup=False) as dag:
    task_1 = BashOperator(
        task_id='task_1',
        bash_command='echo "Task 1 running"'
    )

    task_2 = BashOperator(
        task_id='task_2',
        bash_command='echo "Task 2 running"'
    )

    task_3 = BashOperator(
        task_id='task_3',
        bash_command='echo "Task 3 running"'
    )

    task_4 = BashOperator(
        task_id='task_4',
        bash_command='echo "Task 4 running"'
    )

    # Define multiple dependencies
    task_1 >> [task_2, task_3]  # Task 2 and Task 3 depend on Task 1
    [task_2, task_3] >> task_4  # Task 4 depends on both Task 2 and Task 3
```

In this example, task_2 and task_3 both depend on task_1, and task_4 depends on both task_2 and task_3. This means that task_2 and task_3 can run in parallel after task_1 completes, and task_4 will only run after both task_2 and task_3 have finished successfully.

**Conditional Dependencies (Brief Introduction)**

While a full discussion of conditional dependencies belongs in a later lesson, it's important to briefly mention that Airflow provides mechanisms for creating conditional workflows where the execution path depends on the outcome of a task. This is typically achieved using the BranchPythonOperator, which allows you to define different downstream tasks based on a Python function's return value. We will explore this in more detail in Module 5.

#### <a name="chapter2part2.2"></a>Chapter 2 - Part 2.2: Workflow Orchestration

Workflow orchestration involves managing and coordinating the execution of tasks within a DAG to achieve a specific goal. It encompasses defining task dependencies, scheduling DAG runs, monitoring task status, and handling failures. Airflow's scheduler plays a central role in workflow orchestration by ensuring that tasks are executed in the correct order and at the appropriate time.

**Scheduling and Triggering DAGs**

Airflow allows you to schedule DAGs to run automatically at specific intervals using the schedule_interval parameter. This parameter can be defined using cron expressions or predefined schedules like @daily or @weekly. Alternatively, DAGs can be triggered manually through the Airflow UI or via the Airflow API. We will explore DAG schedules in more detail in the next lesson.

**Monitoring Task Status**

The Airflow UI provides a comprehensive view of DAG and task status, allowing you to monitor the progress of your workflows. You can see which tasks are running, which have succeeded, and which have failed. The UI also provides logs for each task, which can be invaluable for debugging issues.

**Handling Task Failures**

Airflow provides several mechanisms for handling task failures, including retries and error handling. You can configure the number of retries for a task using the retries parameter, and Airflow will automatically retry the task if it fails. You can also define custom error handling logic using callbacks or by implementing exception handling within your tasks. We will explore error handling in more detail in Module 5.

#### <a name="chapter2part2.3"></a>Chapter 2 - Part 2.3: Real-World Application

Consider an e-commerce company that needs to process daily sales data. The workflow might involve the following tasks:

- **Extract**: Extract sales data from various sources (e.g., databases, APIs).
- **Transform**: Clean and transform the data into a consistent format.
- **Load**: Load the transformed data into a data warehouse for analysis.
- **Report**: Generate daily sales reports.

These tasks have clear dependencies: the transformation task depends on the extraction task, the loading task depends on the transformation task, and the reporting task depends on the loading task. Airflow can be used to orchestrate this workflow, ensuring that each task is executed in the correct order and that any failures are handled appropriately.

Another example is a financial institution that needs to calculate risk metrics daily. The workflow might involve:

- **Fetch Market Data**: Retrieve the latest stock prices, interest rates, and other market data.
- **Calculate Risk Factors**: Compute various risk factors based on the market data.
- **Aggregate Risk Metrics**: Combine the risk factors to calculate overall risk metrics for different portfolios.
- **Generate Reports**: Produce risk reports for management and regulatory compliance.

Again, Airflow can orchestrate this workflow, ensuring data accuracy and timely report generation.

A hypothetical scenario involves a research team analyzing climate data. Their workflow might include:

- **Download Data**: Download climate data from various sources.
- **Process Data**: Clean and process the downloaded data.
- **Run Simulations**: Run climate simulations using the processed data.
- **Analyze Results**: Analyze the simulation results and generate visualizations.

Airflow can manage the dependencies between these tasks, ensuring that simulations are run only after the data has been properly processed and that results are analyzed only after the simulations have completed.

#### <a name="chapter2part3"></a>Chapter 2 - Part 3: Using BashOperator for Simple Commands

The BashOperator is a fundamental tool in Airflow for executing shell commands. It allows you to integrate external scripts, utilities, and system-level operations directly into your data pipelines. Understanding how to use the BashOperator effectively is crucial for automating tasks such as data processing, file manipulation, and system administration within your workflows. This lesson will provide a comprehensive guide to using the BashOperator, covering its parameters, common use cases, and best practices.

#### <a name="chapter2part3.1"></a>Chapter 2 - Part 3.1: Understanding the BashOperator

The BashOperator in Airflow is designed to execute bash commands or scripts. It's a simple yet powerful operator that bridges the gap between your Airflow DAG and the underlying operating system.

**Key Parameters**

The BashOperator has several important parameters that control its behavior:

- **task_id (required)**: A unique identifier for the task within the DAG. This is how Airflow tracks and manages the task.
- **bash_command (required)**: The bash command or script to be executed. This can be a simple command like echo "Hello, world!" or a more complex script.
- **env (optional)**: A dictionary of environment variables to be set for the bash command. This allows you to pass configuration values or secrets to the script.
- **append_env (optional)**: If True, the env variables are appended to the existing environment. If False (default), the existing environment is replaced.
- **cwd (optional)**: The working directory to execute the bash command in. If not specified, the default working directory is used.
- **xcom_push (optional)**: If True, the standard output of the bash command is pushed to XCom, allowing it to be used by downstream tasks. We will cover XComs in more detail in a later module.
- **output_encoding (optional)**: Encoding of the standard output. Defaults to 'utf-8'.
- **skip_exit_code (optional)**: Exit code(s) that will be regarded as success.
- **do_xcom_push_fn (optional)**: A callable to determine whether or not to push stdout to XCom.

**Basic Usage**

The most basic usage of the BashOperator involves specifying a task_id and a bash_command.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='bash_operator_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a BashOperator task
    print_date = BashOperator(
        task_id='print_date',
        bash_command='date'
    )

    # Define another BashOperator task
    print_hello = BashOperator(
        task_id='print_hello',
        bash_command='echo "Hello, world!"'
    )

    print_date >> print_hello # Define task dependency
```

In this example, we define two BashOperator tasks: print_date and print_hello. The print_date task executes the date command, and the print_hello task executes the echo "Hello, world!" command. The >> operator defines a task dependency, ensuring that print_date runs before print_hello.

**Using Environment Variables**

You can pass environment variables to the bash command using the env parameter. This is useful for configuring the behavior of the script or passing sensitive information.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='bash_operator_env_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a BashOperator task with environment variables
    print_env = BashOperator(
        task_id='print_env',
        bash_command='echo "The value of MY_VAR is: $MY_VAR"',
        env={'MY_VAR': 'Airflow is awesome!'}
    )
```

In this example, we define a BashOperator task that prints the value of the MY_VAR environment variable. The env parameter is a dictionary that maps the variable name to its value.

**Setting the Working Directory**

The cwd parameter allows you to specify the working directory for the bash command. This is useful when the script needs to access files in a specific directory.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime
import os

with DAG(
    dag_id='bash_operator_cwd_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Create a dummy file in a temporary directory
    temp_dir = '/tmp/airflow_test'
    os.makedirs(temp_dir, exist_ok=True)
    with open(os.path.join(temp_dir, 'test.txt'), 'w') as f:
        f.write('This is a test file.')

    # Define a BashOperator task with a working directory
    list_files = BashOperator(
        task_id='list_files',
        bash_command='ls -l',
        cwd=temp_dir
    )
```

In this example, we create a temporary directory and a dummy file inside it. The BashOperator task then lists the files in that directory using the ls -l command. The cwd parameter is set to the temporary directory, ensuring that the command is executed in the correct context.

**Capturing Output with XCom**

The xcom_push parameter allows you to capture the standard output of the bash command and push it to XCom. This allows downstream tasks to access the output.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.operators.python import PythonOperator
from datetime import datetime

with DAG(
    dag_id='bash_operator_xcom_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a BashOperator task that pushes output to XCom
    get_date = BashOperator(
        task_id='get_date',
        bash_command='date +%Y-%m-%d',
        xcom_push=True
    )

    # Define a PythonOperator task that retrieves the output from XCom
    def print_date_fn(**kwargs):
        ti = kwargs['ti']
        date_from_xcom = ti.xcom_pull(task_ids='get_date')
        print(f"The date from XCom is: {date_from_xcom}")

    print_date = PythonOperator(
        task_id='print_date',
        python_callable=print_date_fn,
        provide_context=True,
    )

    get_date >> print_date
```

In this example, the get_date task executes the date +%Y-%m-%d command and pushes the output to XCom. The print_date task then retrieves the output from XCom using the xcom_pull method and prints it. We will cover PythonOperator in the next module.

#### <a name="chapter2part3.2"></a>Chapter 2 - Part 3.2: Practical Examples and Demonstrations

Let's explore some practical examples of using the BashOperator in real-world scenarios.

**Example 1: Data Processing**

Suppose you have a script that processes data from a file. You can use the BashOperator to execute this script as part of your Airflow DAG.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='data_processing_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a BashOperator task to execute a data processing script
    process_data = BashOperator(
        task_id='process_data',
        bash_command='/path/to/your/data_processing_script.sh'
    )
```

In this example, the process_data task executes the data_processing_script.sh script. You can pass environment variables to the script using the env parameter if needed.

**Example 2: File Manipulation**

You can use the BashOperator to perform file manipulation tasks, such as copying, moving, or deleting files.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='file_manipulation_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a BashOperator task to copy a file
    copy_file = BashOperator(
        task_id='copy_file',
        bash_command='cp /path/to/source/file.txt /path/to/destination/file.txt'
    )
```

In this example, the copy_file task copies a file from one location to another.

**Example 3: System Administration**

You can use the BashOperator to perform system administration tasks, such as restarting a service or checking the status of a system.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='system_administration_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a BashOperator task to restart a service
    restart_service = BashOperator(
        task_id='restart_service',
        bash_command='sudo systemctl restart my_service'
    )
```

In this example, the restart_service task restarts a service using the systemctl command. Note that you may need to configure sudo access for the Airflow user to execute this command.

#### <a name="chapter2part3.3"></a>Chapter 2 - Part 3.3: Best Practices

- **Keep commands simple**: For complex logic, prefer calling an external script rather than embedding it directly in the bash_command. This improves readability and maintainability.
- **Use environment variables**: Avoid hardcoding sensitive information in the bash_command. Use environment variables to pass configuration values and secrets.
- **Handle errors**: Ensure that your bash commands handle errors gracefully. Use error codes and conditional logic to prevent the DAG from failing unexpectedly.
- **Consider security**: Be mindful of the security implications of executing bash commands. Avoid running commands with elevated privileges unless absolutely necessary.
- **Use full paths**: When referencing files or executables, use full paths to avoid ambiguity and ensure that the command is executed in the correct context.

#### <a name="chapter2part4"></a>Chapter 2 - Part 4: Defining DAG Schedules and Catchup

In this lesson, we'll delve into the crucial aspects of scheduling your Directed Acyclic Graphs (DAGs) in Apache Airflow and understanding the concept of "catchup." Proper scheduling ensures your workflows run automatically and consistently, while understanding catchup helps you manage backfilling and historical data processing. We'll explore how to define schedules using various methods and how to control the catchup behavior to suit your specific needs.

#### <a name="chapter2part4.1"></a>Chapter 2 - Part 4.1: Understanding DAG Schedules

A DAG schedule defines when and how often your DAG will run. Airflow provides several ways to define schedules, offering flexibility to accommodate various use cases. The schedule is a crucial part of the DAG definition, as it dictates the rhythm of your data pipelines.

**Cron Expressions**

Cron expressions are a widely used standard for defining schedules. They provide a concise and powerful way to specify complex recurring schedules. A cron expression consists of five or six fields representing:

- Minute (0-59)
- Hour (0-23)
- Day of the month (1-31)
- Month (1-12 or JAN-DEC)
- Day of the week (0-6 or SUN-SAT)
- (Optional) Year

Here are some examples of cron expressions:

- 0 0 * * *: Run the DAG every day at midnight.
- 0 9 * * 1-5: Run the DAG every weekday (Monday to Friday) at 9:00 AM.
- 0 12 1 * *: Run the DAG on the first day of every month at 12:00 PM.
- 0 18 * * 0: Run the DAG every Sunday at 6:00 PM.
- 0 0 1,15 * *: Run the DAG on the 1st and 15th of every month at midnight.

**Example:**

Let's say you want to run a DAG that updates your sales report every day at 7:00 AM. You would use the following cron expression:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='sales_report_daily',
    schedule_interval='0 7 * * *',  # Run at 7:00 AM every day
    start_date=datetime(2023, 1, 1),
    catchup=False,
    tags=['sales'],
) as dag:
    update_report = BashOperator(
        task_id='update_sales_report',
        bash_command='echo "Updating sales report..."',
    )
```

In this example, schedule_interval='0 7 * * *' defines the schedule. The start_date specifies when the DAG should start running, and catchup=False (explained later) prevents backfilling missed runs.

**Timedelta Objects**

Instead of cron expressions, you can use datetime.timedelta objects to define schedules based on fixed time intervals. This is useful for running DAGs at regular intervals, such as every hour, every 30 minutes, or every week.

**Example:**

To run a DAG every hour, you can use timedelta(hours=1):

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime, timedelta

with DAG(
    dag_id='hourly_data_processing',
    schedule_interval=timedelta(hours=1),  # Run every hour
    start_date=datetime(2023, 1, 1),
    catchup=False,
    tags=['data_processing'],
) as dag:
    process_data = BashOperator(
        task_id='process_hourly_data',
        bash_command='echo "Processing hourly data..."',
    )
```

Here, schedule_interval=timedelta(hours=1) sets the DAG to run every hour.

**Preset Schedules**

Airflow provides several preset schedules for common use cases, making it easier to define simple schedules without writing cron expressions or timedelta objects. Some of the most common preset schedules include:

- @once: Run the DAG only once.
- @hourly: Run the DAG every hour.
- @daily: Run the DAG every day.
- @weekly: Run the DAG every week.
- @monthly: Run the DAG every month.
- @yearly: Run the DAG every year.

**Example:**

To run a DAG daily, you can simply use @daily:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='daily_backup',
    schedule_interval='@daily',  # Run every day
    start_date=datetime(2023, 1, 1),
    catchup=False,
    tags=['backup'],
) as dag:
    backup_database = BashOperator(
        task_id='backup_db',
        bash_command='echo "Backing up database..."',
    )
```

Using @daily is more readable and less error-prone than writing the equivalent cron expression (0 0 * * *).

**None or [] for Manual Triggers**

If you want to trigger your DAG manually without any automated schedule, you can set schedule_interval to None or []. This is useful for DAGs that are triggered by external events or on-demand.

Example:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='on_demand_report',
    schedule_interval=None,  # Run only when triggered manually
    start_date=datetime(2023, 1, 1),
    catchup=False,
    tags=['report'],
) as dag:
    generate_report = BashOperator(
        task_id='generate_report',
        bash_command='echo "Generating report..."',
    )
```

With schedule_interval=None, the DAG will only run when you manually trigger it from the Airflow UI or using the Airflow CLI.

#### <a name="chapter2part4.2"></a>Chapter 2 - Part 4.2: Understanding Catchup

The catchup parameter in a DAG definition controls whether Airflow should run the DAG for all missed intervals between the start_date and the current date. By default, catchup is set to True, meaning Airflow will attempt to "catch up" on all past runs.

**Catchup Enabled (catchup=True)**

When catchup is enabled, Airflow will schedule DAG runs for all intervals that have not been executed since the start_date. This is useful for backfilling data or processing historical data that was not processed when the DAG was initially deployed.

**Example:**

Suppose you have a DAG with start_date=datetime(2023, 1, 1) and schedule_interval='@daily'. If you deploy this DAG on January 10, 2023, with catchup=True, Airflow will schedule runs for January 1st, 2nd, 3rd, ..., 9th, and 10th.

**Catchup Disabled (catchup=False)**

When catchup is disabled, Airflow will only schedule runs for the current and future intervals, ignoring any missed intervals between the start_date and the current date. This is useful when you only want to process new data and don't need to backfill historical data.

**Example:**

Using the same DAG as above, if you deploy it on January 10, 2023, with catchup=False, Airflow will only schedule a run for January 10th and subsequent days, skipping the runs for January 1st to 9th.

**Implications of Catchup**

- **Resource Consumption**: Enabling catchup can consume significant resources, especially for DAGs with frequent schedules or long historical periods. Be mindful of the potential impact on your Airflow infrastructure.
- **Data Consistency**: Catchup ensures that all historical data is processed, maintaining data consistency and completeness.
- **DAG Behavior**: Disabling catchup can simplify DAG execution and reduce resource consumption, but it may result in incomplete historical data.

**Controlling Catchup Behavior**

You can control the catchup behavior at the DAG level using the catchup parameter. However, you can also control it at the task level using the depends_on_past parameter in the operator definition.

- **depends_on_past=True**: The task will only run if the previous task instance has succeeded. This is useful for ensuring data dependencies are met when backfilling data.
- **depends_on_past=False**: The task will run regardless of the status of the previous task instance.

**Example:**

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='data_backfill',
    schedule_interval='@daily',
    start_date=datetime(2023, 1, 1),
    catchup=True,
    tags=['data_processing'],
) as dag:
    extract_data = BashOperator(
        task_id='extract_data',
        bash_command='echo "Extracting data..."',
        depends_on_past=False,  # Extract data regardless of previous runs
    )

    transform_data = BashOperator(
        task_id='transform_data',
        bash_command='echo "Transforming data..."',
        depends_on_past=True,  # Transform data only if previous extraction succeeded
    )

    load_data = BashOperator(
        task_id='load_data',
        bash_command='echo "Loading data..."',
        depends_on_past=True,  # Load data only if previous transformation succeeded
    )

    extract_data >> transform_data >> load_data
```

In this example, the extract_data task will run for all missed intervals, regardless of whether previous runs have succeeded. However, the transform_data and load_data tasks will only run if the previous task instance has succeeded, ensuring data dependencies are met during backfilling.

#### <a name="chapter2part4.3"></a>Chapter 2 - Part 4.3: Practical Examples and Demonstrations

Let's consider a few practical examples to illustrate the concepts of DAG schedules and catchup.

**Example 1: Daily Data Aggregation**
.
Suppose you have a DAG that aggregates daily sales data and generates a report. You want this DAG to run every day at 8:00 AM. You also want to backfill data for the past week in case the DAG was not running.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='daily_sales_aggregation',
    schedule_interval='0 8 * * *',  # Run at 8:00 AM every day
    start_date=datetime(2023, 1, 1),
    catchup=True,  # Backfill data for missed intervals
    tags=['sales', 'aggregation'],
) as dag:
    aggregate_sales = BashOperator(
        task_id='aggregate_sales',
        bash_command='echo "Aggregating daily sales data..."',
    )

    generate_report = BashOperator(
        task_id='generate_report',
        bash_command='echo "Generating sales report..."',
    )

    aggregate_sales >> generate_report
```

In this example, catchup=True ensures that the DAG will backfill data for any missed days since the start_date.

**Example 2: Weekly Data Backup**

Suppose you have a DAG that backs up your database every Sunday at midnight. You don't need to backfill data for missed weeks, as the latest backup is sufficient.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='weekly_database_backup',
    schedule_interval='0 0 * * 0',  # Run every Sunday at midnight
    start_date=datetime(2023, 1, 1),
    catchup=False,  # Do not backfill data for missed weeks
    tags=['backup', 'database'],
) as dag:
    backup_database = BashOperator(
        task_id='backup_db',
        bash_command='echo "Backing up database..."',
    )
```

Here, catchup=False prevents the DAG from backfilling data for missed weeks, ensuring that only the latest backup is performed.

**Example 3: Event-Triggered Data Processing**

Suppose you have a DAG that processes data when a new file arrives in a specific directory. This DAG should only run when a new file is detected and should not have a fixed schedule.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='event_triggered_data_processing',
    schedule_interval=None,  # Run only when triggered manually
    start_date=datetime(2023, 1, 1),
    catchup=False,  # Not applicable for manual triggers
    tags=['data_processing', 'event_driven'],
) as dag:
    process_data = BashOperator(
        task_id='process_data',
        bash_command='echo "Processing data from new file..."',
    )
```

In this case, schedule_interval=None indicates that the DAG is triggered manually, and catchup=False is not relevant as there is no fixed schedule.

#### <a name="chapter2part5"></a>Chapter 2 - Part 5: Running and Monitoring Your DAG in the Airflow UI

After defining your DAG, setting up task dependencies, and configuring a schedule, the next crucial step is to run and monitor it. The Airflow UI provides a comprehensive interface for interacting with your DAGs, triggering runs, and observing their execution. This lesson will guide you through the various features of the Airflow UI that are essential for managing your workflows.

#### <a name="chapter2part5.1"></a>Chapter 2 - Part 5.1: Accessing the Airflow UI

The Airflow UI is typically accessed through a web browser. If you followed the setup instructions in Module 1, you should have a local Airflow instance running. By default, the UI is accessible at http://localhost:8080. Open this address in your browser to access the Airflow UI. You'll likely be prompted for login credentials. The default username and password (if you haven't changed them) are usually airflow and airflow.

#### <a name="chapter2part5.2"></a>Chapter 2 - Part 5.2: Understanding the DAGs View

Upon logging in, you'll be presented with the DAGs view. This is the central hub for managing your DAGs.

**DAG List**

The DAGs view displays a list of all DAGs that Airflow has discovered in your dags_folder (configured in your airflow.cfg file or environment variables). For each DAG, you'll see key information:

- **DAG ID**: The unique identifier for the DAG.
- **Owner**: The owner of the DAG (defined in the DAG definition).
- **Schedule**: The schedule interval defined for the DAG.
- **Last Run**: The date and time of the most recent DAG run.
- **Next Run**: The scheduled date and time for the next DAG run.
- **Recent Tasks**: A visual representation of the status of recent task instances.
- **Links**: A set of icons providing quick access to various DAG-related actions and views.

**DAG Actions**

The DAGs view provides several actions you can perform on a DAG:

- **Trigger DAG**: Manually trigger a new DAG run. This is useful for testing or running a DAG on demand.
- **Pause/Unpause DAG**: Enable or disable the DAG's scheduler. Paused DAGs will not be scheduled to run automatically.
- **Delete DAG**: Remove the DAG from Airflow. Use this with caution, as it will delete the DAG definition and its run history.
- **Refresh**: Reload the DAGs to reflect any changes in the DAG definitions.

#### <a name="chapter2part5.3"></a>Chapter 2 - Part 5.3: Exploring the DAG Details View

Clicking on a DAG ID in the DAGs view will take you to the DAG Details view. This view provides a more in-depth look at the DAG's structure, status, and history.

**Graph View**

The Graph View is a visual representation of the DAG's tasks and dependencies. Each task is represented as a node, and dependencies are represented as arrows connecting the nodes. The color of each node indicates the task's current status:

- **Green**: Success
- **Red**: Failed
- **Yellow**: Running
- **Light Blue**: Upstream Failed (a task that was skipped because one of its upstream dependencies failed)
- **White**: Scheduled/Queued
- **Gray**: Not yet run

You can hover over a task node to see more information about the task, such as its task ID, start time, and end time. You can also click on a task node to access the Task Instance Details.

**Grid View**

The Grid View provides a tabular representation of the DAG's past and future runs. Each row represents a DAG run, and each column represents a task. The cells in the grid show the status of each task instance for each DAG run. This view is useful for quickly identifying patterns of success and failure across multiple DAG runs.

**Tree View**

The Tree View presents a hierarchical view of the DAG runs and their task instances. It's similar to the Grid View but organized in a tree structure, making it easier to navigate complex DAGs with many tasks and dependencies.

**Code View**

The Code View displays the Python code that defines the DAG. This is useful for quickly reviewing the DAG's logic and configuration.

**Task Instance Details**

Clicking on a task in the Graph, Grid, or Tree View will take you to the Task Instance Details page. This page provides detailed information about a specific task instance, including:

- **Log**: The task's execution logs, which can be invaluable for debugging.
- **Task Attributes**: The task's configuration parameters.
- **Try Number**: The number of times the task has been attempted (including retries).
- **Start Time**: The time the task instance started running.
- **End Time**: The time the task instance finished running.
- **Duration**: The total time the task instance took to run.
- **Mark Success/Fail**: Manually mark the task as successful or failed. Use this with caution, as it can affect the DAG's execution flow.
- **Clear**: Clear the task instance's state, allowing it to be re-run. This is useful for recovering from errors or re-processing data.

#### <a name="chapter2part5.4"></a>Chapter 2 - Part 5.4: Triggering DAG Runs

You can trigger DAG runs manually from the Airflow UI in several ways:

- **From the DAGs View**: Click the "Trigger DAG" button next to the DAG you want to run.
- **From the DAG Details View**: Click the "Trigger DAG" button in the top right corner of the screen.

When you trigger a DAG run, Airflow will create a new DAG run instance and schedule the tasks according to their dependencies.

#### <a name="chapter2part5.5"></a>Chapter 2 - Part 5.5: Monitoring DAG Runs

The Airflow UI provides several ways to monitor the progress of DAG runs:

- **Graph View**: The Graph View provides a real-time visual representation of the DAG's execution. You can see which tasks are running, which have succeeded, and which have failed.
- **Grid View**: The Grid View provides a tabular overview of the DAG's past and future runs. You can quickly see the status of each task instance for each DAG run.
- **Task Instance Details**: The Task Instance Details page provides detailed information about a specific task instance, including its logs, attributes, and execution time.

#### <a name="chapter2part5.6"></a>Chapter 2 - Part 5.6: Common Use Cases for the Airflow UI

Here are some common scenarios where the Airflow UI is essential:

- **Debugging Failed Tasks**: When a task fails, the Airflow UI provides access to the task's logs, which can help you identify the cause of the failure.
- **Monitoring DAG Performance**: The Airflow UI provides information about task execution times, which can help you identify performance bottlenecks in your DAG.
- **Manually Triggering DAG Runs**: You can use the Airflow UI to manually trigger DAG runs for testing or on-demand processing.
- **Clearing Task Instances**: If a task fails due to a transient error, you can use the Airflow UI to clear the task instance and re-run it.
- **Pausing and Unpausing DAGs**: You can use the Airflow UI to pause DAGs that you don't want to run automatically, or to unpause DAGs that have been paused.

## <a name="chapter3"></a>Chapter 3: Core Airflow Operator

#### <a name="chapter3part1"></a>Chapter 3 - Part 1: Introduction to Common Operators: PythonOperator, EmailOperator

#### <a name="chapter3part1.1"></a>Chapter 3 - Part 1.1: PythonOperator: Executing Python Code

#### <a name="chapter3part1.2"></a>Chapter 3 - Part 1.2: EmailOperator: Sending Email Notifications

#### <a name="chapter3part2"></a>Chapter 3 - Part 2: Working with Data Transfer Operators: S3Hook and S3FileTransferOperator

#### <a name="chapter3part2.1"></a>Chapter 3 - Part 2.1: Understanding S3Hook

#### <a name="chapter3part2.2"></a>Chapter 3 - Part 2.2: Understanding S3FileTransferOperator

#### <a name="chapter3part2.3"></a>Chapter 3 - Part 2.3: Real-World Application

#### <a name="chapter3part3"></a>Chapter 3 - Part 3: Using the PostgresOperator to Interact with Databases

#### <a name="chapter3part3.1"></a>Chapter 3 - Part 3.1: Understanding the PostgresOperator

#### <a name="chapter3part3.2"></a>Chapter 3 - Part 3.2: Advanced Usage and Best Practices

#### <a name="chapter3part4"></a>Chapter 3 - Part 4: Understanding Idempotency and Task Retries

#### <a name="chapter3part4.1"></a>Chapter 3 - Part 4.1: Understanding Idempotency

#### <a name="chapter3part4.2"></a>Chapter 3 - Part 4.2: Understanding Task Retries

#### <a name="chapter3part4.3"></a>Chapter 3 - Part 4.3: Real-World Application

#### <a name="chapter3part5"></a>Chapter 3 - Part 5: Best Practices for Operator Usage

#### <a name="chapter3part5.1"></a>Chapter 3 - Part 5.1: Understanding Operator Idempotency

#### <a name="chapter3part5.2"></a>Chapter 3 - Part 5.2: Configuring Task Retries

#### <a name="chapter3part5.3"></a>Chapter 3 - Part 5.3: Choosing the Right Operator

## <a name="chapter4"></a>Chapter 4: Variables and Connections

#### <a name="chapter4part1"></a>Chapter 4 - Part 1: Introduction to Airflow Variables

#### <a name="chapter4part1.1"></a>Chapter 4 - Part 1.1: Understanding Airflow Variables

#### <a name="chapter4part1.2"></a>Chapter 4 - Part 1.2: Setting and Retrieving Variables

#### <a name="chapter4part1.3"></a>Chapter 4 - Part 1.3: Practical Examples

#### <a name="chapter4part2"></a>Chapter 4 - Part 2: Setting and Retrieving Variables in the UI and DAGs

#### <a name="chapter4part2.1"></a>Chapter 4 - Part 2.1: Understanding Airflow Variables

#### <a name="chapter4part2.2"></a>Chapter 4 - Part 2.2: Setting Variables in the Airflow UI

#### <a name="chapter4part2.3"></a>Chapter 4 - Part 2.3: Retrieving Variables in DAGs

#### <a name="chapter4part2.4"></a>Chapter 4 - Part 2.4: Best Practices for Using Variables

#### <a name="chapter4part3"></a>Chapter 4 - Part 3: Understanding Airflow Connections

#### <a name="chapter4part3.1"></a>Chapter 4 - Part 3.1: Understanding Airflow Connections

#### <a name="chapter4part3.2"></a>Chapter 4 - Part 3.2: Best Practices for Using Connections

#### <a name="chapter4part4"></a>Chapter 4 - Part 4: Configuring Connections for Databases, APIs, and Cloud Services

#### <a name="chapter4part4.1"></a>Chapter 4 - Part 4.1: Understanding Airflow Connections

#### <a name="chapter4part4.2"></a>Chapter 4 - Part 4.2: Configuring Connections

#### <a name="chapter4part4.3"></a>Chapter 4 - Part 4.3: Using Connections in DAGs

#### <a name="chapter4part4.4"></a>Chapter 4 - Part 4.4: Connection Examples for Different Services

#### <a name="chapter4part4.5"></a>Chapter 4 - Part 4.5: Practice Activities

#### <a name="chapter4part5"></a>Chapter 4 - Part 5: Using Variables and Connections for Secure Configuration Management

#### <a name="chapter4part5.1"></a>Chapter 4 - Part 5.1: Understanding the Need for Secure Configuration Management

#### <a name="chapter4part5.2"></a>Chapter 4 - Part 5.2: Airflow Variables: Dynamic Configuration Options

#### <a name="chapter4part5.3"></a>Chapter 4 - Part 5.3: Airflow Connections: Securely Storing Credentials

#### <a name="chapter4part5.4"></a>Chapter 4 - Part 5.4: Using Variables and Connections Together

#### <a name="chapter4part5.5"></a>Chapter 4 - Part 5.5: Practice Activities

## <a name="chapter5"></a>Chapter 5: Advanced DAG Concepts

#### <a name="chapter5part1"></a>Chapter 5 - Part 1: SubDAGs and TaskGroups for Modular DAG Design

#### <a name="chapter5part1.1"></a>Chapter 5 - Part 1.1: Understanding SubDAGs

#### <a name="chapter5part1.2"></a>Chapter 5 - Part 1.2: Understanding TaskGroups

#### <a name="chapter5part1.3"></a>Chapter 5 - Part 1.3: SubDAGs vs. TaskGroups: A Comparison

#### <a name="chapter5part1.4"></a>Chapter 5 - Part 1.4: Practical Examples and Demonstrations

#### <a name="chapter5part2"></a>Chapter 5 - Part 2: Using BranchPythonOperator for Conditional Logic

#### <a name="chapter5part2.1"></a>Chapter 5 - Part 2.1: Understanding the BranchPythonOperator

#### <a name="chapter5part3"></a>Chapter 5 - Part 3: Dynamic DAG Generation with Python

#### <a name="chapter5part3.1"></a>Chapter 5 - Part 3.1: Understanding Dynamic DAG Generation

#### <a name="chapter5part3.2"></a>Chapter 5 - Part 3.2: Implementing Dynamic DAG Generation

#### <a name="chapter5part4"></a>Chapter 5 - Part 4: Understanding XComs for Inter-Task Communication

#### <a name="chapter5part4.1"></a>Chapter 5 - Part 4.1: Understanding XComs

#### <a name="chapter5part5"></a>Chapter 5 - Part 5: Implementing Error Handling and Alerting

#### <a name="chapter5part5.1"></a>Chapter 5 - Part 5.1: Understanding Error Handling in Airflow

## <a name="chapter6"></a>Chapter 6: Airflow Sensors

#### <a name="chapter6part1"></a>Chapter 6 - Part 1: Introduction to Airflow Sensors

#### <a name="chapter6part1.1"></a>Chapter 6 - Part 1.1: Understanding Airflow Sensors

#### <a name="chapter6part1.2"></a>Chapter 6 - Part 1.2: Types of Airflow Sensors

#### <a name="chapter6part1.3"></a>Chapter 6 - Part 1.3: Sensor Parameters

#### <a name="chapter6part1.4"></a>Chapter 6 - Part 1.4: Practical Examples

#### <a name="chapter6part1.5"></a>Chapter 6 - Part 1.5: Best Practices for Using Sensors

#### <a name="chapter6part2"></a>Chapter 6 - Part 2: Using FileSensor to wait for file arrival

#### <a name="chapter6part2.1"></a>Chapter 6 - Part 2.1: Understanding the FileSensor

#### <a name="chapter6part3"></a>Chapter 6 - Part 3: Using HttpSensor to check for API availability

#### <a name="chapter6part3.1"></a>Chapter 6 - Part 3.1: Understanding the HttpSensor

#### <a name="chapter6part3.2"></a>Chapter 6 - Part 3.2: Best Practices for Using HttpSensor

#### <a name="chapter6part4"></a>Chapter 6 - Part 4: Creating Custom Sensors

#### <a name="chapter6part4.1"></a>Chapter 6 - Part 4.1: Understanding Custom Sensors

#### <a name="chapter6part4.2"></a>Chapter 6 - Part 4.2: Advanced Custom Sensors

#### <a name="chapter6part4.3"></a>Chapter 6 - Part 4.3: Best Practices for Custom Sensors

#### <a name="chapter6part4.4"></a>Chapter 6 - Part 4.4: Real-World Application

#### <a name="chapter6part5"></a>Chapter 6 - Part 5: Best practices for using Sensors

#### <a name="chapter6part5.1"></a>Chapter 6 - Part 5.1: Sensor Timeouts and Failure Modes

#### <a name="chapter6part5.2"></a>Chapter 6 - Part 5.2: Sensor Modes: Poke vs. Deferrable

#### <a name="chapter6part5.3"></a>Chapter 6 - Part 5.3: Optimizing Sensor Performance

#### <a name="chapter6part5.4"></a>Chapter 6 - Part 5.4: Best Practices for Sensor Design

## <a name="chapter7"></a>Chapter 7: Deploying Airflow to Production

#### <a name="chapter7part1"></a>Chapter 7 - Part 1: Choosing a Deployment Strategy: Kubernetes, Docker Compose, Managed Services

#### <a name="chapter7part1.1"></a>Chapter 7 - Part 1.1: Deployment Strategies for Apache Airflow

#### <a name="chapter7part1.2"></a>Chapter 7 - Part 1.2: Choosing the Right Strategy

#### <a name="chapter7part1.3"></a>Chapter 7 - Part 1.3: Practice Activities

#### <a name="chapter7part2"></a>Chapter 7 - Part 2: Configuring Airflow for Production: Database, Executor, Logging

#### <a name="chapter7part2.1"></a>Chapter 7 - Part 2.1: Database Configuration

#### <a name="chapter7part2.2"></a>Chapter 7 - Part 2.2: Executor Configuration

#### <a name="chapter7part2.3"></a>Chapter 7 - Part 2.3: Logging Configuration

#### <a name="chapter7part3"></a>Chapter 7 - Part 3: Implementing Monitoring and Alerting

#### <a name="chapter7part3.1"></a>Chapter 7 - Part 3.1: Key Monitoring Metrics

#### <a name="chapter7part3.2"></a>Chapter 7 - Part 3.2: Tools for Monitoring Airflow

#### <a name="chapter7part3.3"></a>Chapter 7 - Part 3.3: Implementing Alerting

#### <a name="chapter7part3.4"></a>Chapter 7 - Part 3.4: Best Practices for Monitoring and Alerting

#### <a name="chapter7part4"></a>Chapter 7 - Part 4: Understanding Airflow Security Best Practices

#### <a name="chapter7part4.1"></a>Chapter 7 - Part 4.1: Authentication and Authorization

#### <a name="chapter7part4.2"></a>Chapter 7 - Part 4.2: Encryption

#### <a name="chapter7part4.3"></a>Chapter 7 - Part 4.3: Network Security

#### <a name="chapter7part4.4"></a>Chapter 7 - Part 4.4: Other Security Considerations

#### <a name="chapter7part5"></a>Chapter 7 - Part 5: Scaling Airflow for High Availability

#### <a name="chapter7part5.1"></a>Chapter 7 - Part 5.1: Understanding High Availability and Scalability in Airflow

#### <a name="chapter7part5.2"></a>Chapter 7 - Part 5.2: Architectures for Scaling Airflow

#### <a name="chapter7part5.3"></a>Chapter 7 - Part 5.3: Configuring Airflow for High Availability

#### <a name="chapter7part5.4"></a>Chapter 7 - Part 5.4: Implementing Monitoring and Alerting

#### <a name="chapter7part5.5"></a>Chapter 7 - Part 5.5: Airflow Security Best Practices
