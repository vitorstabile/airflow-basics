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
    - [Chapter 4 - Part 5: Using Variables and Connections for Secure Configuration Management](#chapter4part5)
      - [Chapter 4 - Part 5.1: Understanding the Need for Secure Configuration Management](#chapter4part5.1)
      - [Chapter 4 - Part 5.2: Airflow Variables: Dynamic Configuration Options](#chapter4part5.2)
      - [Chapter 4 - Part 5.3: Airflow Connections: Securely Storing Credentials](#chapter4part5.3)
      - [Chapter 4 - Part 5.4: Using Variables and Connections Together](#chapter4part5.4)
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

In Apache Airflow, operators are the building blocks of your workflows. They represent a single, self-contained task in a DAG. Airflow provides a wide range of operators for various tasks, such as executing shell commands, running Python functions, transferring data between systems, and sending emails. Understanding how to use operators effectively is crucial for building robust and maintainable data pipelines. This lesson will focus on two fundamental operators: PythonOperator and EmailOperator. We'll explore their functionalities, parameters, and practical applications, equipping you with the knowledge to integrate them into your Airflow DAGs.

#### <a name="chapter3part1.1"></a>Chapter 3 - Part 1.1: PythonOperator: Executing Python Code

In Apache Airflow, operators are the building blocks of your workflows. They represent a single, self-contained task in a DAG. Airflow provides a wide range of operators for various tasks, such as executing shell commands, running Python functions, transferring data between systems, and sending emails. Understanding how to use operators effectively is crucial for building robust and maintainable data pipelines. This lesson will focus on two fundamental operators: PythonOperator and EmailOperator. We'll explore their functionalities, parameters, and practical applications, equipping you with the knowledge to integrate them into your Airflow DAGs.

**Basic Usage**

The PythonOperator requires a python_callable argument, which specifies the Python function to be executed.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def my_python_function():
    print("Hello from my Python function!")

with DAG(
    dag_id='python_operator_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    python_task = PythonOperator(
        task_id='my_python_task',
        python_callable=my_python_function
    )
```

In this example:

- We define a simple Python function my_python_function that prints a message.
- We create a PythonOperator named python_task and assign my_python_function to its python_callable argument.
- When the DAG runs, the python_task will execute my_python_function, and the message "Hello from my Python function!" will be printed to the Airflow logs.

**Passing Arguments to the Python Callable**

You can pass arguments to your Python function using the op_kwargs parameter.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def greet(name):
    print(f"Hello, {name}!")

with DAG(
    dag_id='python_operator_with_args',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    greet_task = PythonOperator(
        task_id='greet_task',
        python_callable=greet,
        op_kwargs={'name': 'Airflow'}
    )
```

Here, we define a greet function that takes a name argument. We pass the value "Airflow" to the name argument using op_kwargs. When the DAG runs, the greet_task will execute greet("Airflow"), and the message "Hello, Airflow!" will be printed.

**Accessing DAG Context**

The PythonOperator can also access the DAG context, which provides information about the current task instance, DAG run, and other relevant details. To access the context, set the provide_context parameter to True. The context will be passed as a keyword argument (kwargs) to your Python function.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def print_context(ds=None, **kwargs):
    print(kwargs)
    print(ds)
    return 'Whatever you return gets printed in the logs'

with DAG(
    dag_id='python_operator_with_context',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    print_context_task = PythonOperator(
        task_id='print_context',
        python_callable=print_context,
        provide_context=True,
    )
```

In this example:

- We define a print_context function that accepts ds (the execution date) and kwargs (the context dictionary) as arguments.
- We set provide_context=True in the PythonOperator.
- When the DAG runs, the print_context_task will execute print_context, and the context dictionary will be printed to the Airflow logs. The ds variable will contain the execution date of the DAG run.

**Returning Values from the Python Callable**

The PythonOperator can also return values from the Python callable. These values can be accessed by downstream tasks using XComs (Cross-Communication). We will cover XComs in detail in a later lesson, but here's a brief example:

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.operators.bash import BashOperator
from datetime import datetime

def return_value():
    return "This is the returned value"

with DAG(
    dag_id='python_operator_return_value',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    return_value_task = PythonOperator(
        task_id='return_value_task',
        python_callable=return_value
    )

    print_value_task = BashOperator(
        task_id='print_value_task',
        bash_command="echo \"{{ ti.xcom_pull(task_ids='return_value_task') }}\""
    )

    return_value_task >> print_value_task
```

In this example:

- The return_value_task executes the return_value function, which returns a string.
- The print_value_task uses a BashOperator to print the returned value. The ti.xcom_pull method retrieves the value from XCom using the task_id of the upstream task (return_value_task).

**Error Handling**

When using the PythonOperator, it's important to handle potential errors in your Python code. If an exception occurs within the python_callable, the task will fail. You can use try...except blocks to catch and handle exceptions gracefully.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def risky_function():
    try:
        result = 1 / 0  # This will cause a ZeroDivisionError
    except ZeroDivisionError as e:
        print(f"Caught an error: {e}")
        raise  # Re-raise the exception to fail the task

with DAG(
    dag_id='python_operator_error_handling',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    risky_task = PythonOperator(
        task_id='risky_task',
        python_callable=risky_function
    )
```

In this example, the risky_function attempts to divide by zero, which will raise a ZeroDivisionError. The try...except block catches the error, prints an error message, and then re-raises the exception to ensure that the task fails.

#### <a name="chapter3part1.2"></a>Chapter 3 - Part 1.2: EmailOperator: Sending Email Notifications

The EmailOperator allows you to send email notifications from your Airflow DAGs. This is useful for alerting users about task failures, DAG completion, or other important events.

**Basic Usage**

The EmailOperator requires several parameters, including:

- **to**: The recipient email address(es).
- **subject**: The email subject.
- **html_content**: The email body in HTML format.

Before using the EmailOperator, you need to configure your Airflow environment to send emails. This typically involves setting up an SMTP server and configuring the airflow.cfg file.

```py
from airflow import DAG
from airflow.operators.email import EmailOperator
from datetime import datetime

with DAG(
    dag_id='email_operator_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    send_email_task = EmailOperator(
        task_id='send_email',
        to='recipient@example.com',
        subject='Airflow DAG Notification',
        html_content='<h1>DAG completed successfully!</h1>'
    )
```

In this example:

- We create an EmailOperator named send_email_task.
- We set the to, subject, and html_content parameters to specify the recipient, subject, and body of the email.
- When the DAG runs, the send_email_task will send an email to recipient@example.com with the specified subject and body.

**Using Jinja Templating**

The EmailOperator supports Jinja templating, which allows you to dynamically generate the email subject and body based on the DAG context.

```py
from airflow import DAG
from airflow.operators.email import EmailOperator
from datetime import datetime

with DAG(
    dag_id='email_operator_with_jinja',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    send_email_task = EmailOperator(
        task_id='send_email',
        to='recipient@example.com',
        subject='Airflow DAG Notification - Run ID: {{ dag_run.run_id }}',
        html_content='<h1>DAG completed successfully!</h1><p>Execution date: {{ ds }}</p>'
    )
```

In this example, we use Jinja templates to include the DAG run ID (dag_run.run_id) and execution date (ds) in the email subject and body.

**Attaching Files**

The EmailOperator can also attach files to the email. To attach a file, use the files parameter, which accepts a list of file paths.

```py
from airflow import DAG
from airflow.operators.email import EmailOperator
from datetime import datetime

with DAG(
    dag_id='email_operator_with_attachment',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    send_email_task = EmailOperator(
        task_id='send_email',
        to='recipient@example.com',
        subject='Airflow DAG Notification with Attachment',
        html_content='<h1>DAG completed successfully!</h1>',
        files=['/path/to/your/file.txt']
    )
```

In this example, the send_email_task will attach the file /path/to/your/file.txt to the email.

**Real-World Application**

Consider a scenario where you have a data pipeline that processes customer orders. You can use the EmailOperator to send notifications to the sales team when a critical task in the pipeline fails, such as a data validation check. This allows the sales team to quickly identify and resolve issues that may impact order processing.

Another example is sending daily summary reports. A DAG can generate a report and then use the EmailOperator to send it to stakeholders.

Hypothetically, imagine a DAG that monitors social media sentiment for a particular brand. If the sentiment drops below a certain threshold, the EmailOperator could be used to alert the marketing team.

#### <a name="chapter3part2"></a>Chapter 3 - Part 2: Working with Data Transfer Operators: S3Hook and S3FileTransferOperator

Working with data in the cloud often involves transferring files to and from services like Amazon S3. Airflow provides operators and hooks specifically designed to simplify these data transfer operations. This lesson will focus on two key components: the S3Hook and the S3FileTransferOperator. We'll explore how to use them to interact with S3, upload files, download files, and manage data transfer tasks within your Airflow DAGs. Understanding these tools is crucial for building robust and scalable data pipelines that leverage cloud storage.

#### <a name="chapter3part2.1"></a>Chapter 3 - Part 2.1: Understanding S3Hook

The S3Hook is an interface to Amazon's Simple Storage Service (S3). It provides methods for interacting with S3, such as uploading, downloading, deleting, and listing objects. Think of it as a Python client specifically designed for Airflow to communicate with S3.

**Key Features of S3Hook**

- **Connection Management**: The S3Hook uses Airflow connections to securely store and retrieve your AWS credentials. This avoids hardcoding sensitive information in your DAGs.
- **Simplified S3 Operations**: It provides high-level functions for common S3 tasks, making it easier to interact with S3 without writing verbose boto3 code.
- **Error Handling**: The hook handles common S3 errors and exceptions, providing a more robust and reliable way to interact with S3.
- **Flexibility**: While it simplifies common tasks, it also allows you to access the underlying boto3 client for more advanced or customized operations.

**Creating an S3Hook Instance**

To use the S3Hook, you first need to create an instance of it within your DAG. This typically involves specifying the Airflow connection ID that contains your AWS credentials.

```py
from airflow.providers.amazon.aws.hooks.s3 import S3Hook

# Replace 'aws_default' with the name of your Airflow connection
s3_hook = S3Hook(aws_conn_id='aws_default')
```

Explanation:

- **from airflow.providers.amazon.aws.hooks.s3 import S3Hook**: This line imports the S3Hook class from the Airflow library.
- **s3_hook = S3Hook(aws_conn_id='aws_default')**: This line creates an instance of the S3Hook. The aws_conn_id parameter specifies the Airflow connection that contains your AWS credentials (access key ID and secret access key). You must create this connection in the Airflow UI under Admin -> Connections. Choose "Amazon S3" as the connection type.

**Common S3Hook Methods**

Here are some of the most commonly used methods provided by the S3Hook:

- **load_file(filename, key, bucket_name, replace=True)**: Uploads a local file to S3.
  - **filename**: The path to the local file to upload.
  - **key**: The S3 key (path) where the file will be stored.
  - **bucket_name**: The name of the S3 bucket.
  - **replace**: If True, overwrites the file if it already exists in S3.
 
- **load_string(string_data, key, bucket_name, replace=True, encoding='utf-8')**: Uploads a string to S3 as a file.
  - **string_data**: The string to upload.
  - **key**: The S3 key (path) where the string will be stored.
  - **bucket_name**: The name of the S3 bucket.
  - **replace**: If True, overwrites the file if it already exists in S3.
  - **encoding**: The encoding to use for the string (default is UTF-8).
 
- **download_file(key, bucket_name, local_path=None)**: Downloads a file from S3 to a local directory.
  - **key**: The S3 key (path) of the file to download.
  - **bucket_name**: The name of the S3 bucket.
  - **local_path**: The local path where the file will be saved. If None, a temporary file is created.
 
- **delete_objects(keys, bucket_name, delete_version=False, mfa_delete=False)**: Deletes one or more objects from S3.
  - **keys**: A list of S3 keys (paths) to delete.
  - **bucket_name**: The name of the S3 bucket.
  - **delete_version**: If True, deletes a specific version of the object.
  - **mfa_delete**: If True, requires multi-factor authentication for deletion.
 
- **check_for_key(key, bucket_name)**: Checks if a key exists in S3.
  - **key**: The S3 key (path) to check.
  - **bucket_name**: The name of the S3 bucket.
 
- **list_keys(bucket_name, prefix=None, delimiter=None)**: Lists keys in a bucket.
  - **bucket_name**: The name of the S3 bucket.
  - **prefix**: An optional prefix to filter the keys.
  - **delimiter**: An optional delimiter to simulate directory structure.
 
**Example: Uploading a File to S3 using S3Hook**

```py
from airflow import DAG
from airflow.providers.amazon.aws.hooks.s3 import S3Hook
from airflow import utils
import datetime as dt

with DAG(
    dag_id='s3_hook_upload_example',
    start_date=utils.dates.days_ago(2),
    schedule_interval=None,
    catchup=False
) as dag:
    def upload_to_s3():
        s3_hook = S3Hook(aws_conn_id='aws_default')
        filename = 'local_file.txt'
        key = 's3_file.txt'
        bucket_name = 'your-s3-bucket'  # Replace with your bucket name

        # Create a dummy local file
        with open(filename, 'w') as f:
            f.write("This is a test file for S3Hook.")

        s3_hook.load_file(filename=filename, key=key, bucket_name=bucket_name, replace=True)
        print(f"File {filename} uploaded to s3://{bucket_name}/{key}")

    from airflow.operators.python import PythonOperator
    upload_task = PythonOperator(
        task_id='upload_file_to_s3',
        python_callable=upload_to_s3
    )
```

**Explanation:**

- **Import necessary modules**: We import DAG, S3Hook, days_ago, and PythonOperator.
- **Define the DAG**: We create a DAG with a unique dag_id, a start_date, and a schedule_interval.
- **Define the upload_to_s3 function**:
  - Creates an S3Hook instance using the aws_default connection.
  - Defines the local filename, the S3 key, and the bucket_name. Important: Replace 'your-s3-bucket' with the actual name of your S3 bucket.
  - Creates a dummy local file named local_file.txt and writes some content to it.
  - Calls the load_file method of the S3Hook to upload the local file to S3. The replace=True argument ensures that the file will be overwritten if it already exists in S3.
  - Prints a confirmation message to the console.
 
- **Create a PythonOperator**:
  - Creates a PythonOperator named upload_task that executes the upload_to_s3 function.
  - Sets the task_id to upload_file_to_s3.
  - Sets the python_callable to the upload_to_s3 function.
 
- **Set task dependencies (implicit)**: In this simple example, there's only one task, so no explicit dependencies are needed.

**Example: Downloading a File from S3 using S3Hook**

```py
from airflow import DAG
from airflow.providers.amazon.aws.hooks.s3 import S3Hook
from airflow import utils
import datetime as dt

with DAG(
    dag_id='s3_hook_download_example',
    start_date=utils.dates.days_ago(2),
    schedule_interval=None,
    catchup=False
) as dag:
    def download_from_s3():
        s3_hook = S3Hook(aws_conn_id='aws_default')
        key = 's3_file.txt'  # Replace with the S3 key of the file you want to download
        bucket_name = 'your-s3-bucket'  # Replace with your bucket name
        local_path = 'downloaded_file.txt'

        s3_hook.download_file(key=key, bucket_name=bucket_name, local_path=local_path)
        print(f"File s3://{bucket_name}/{key} downloaded to {local_path}")

    from airflow.operators.python import PythonOperator
    download_task = PythonOperator(
        task_id='download_file_from_s3',
        python_callable=download_from_s3
    )
```

**Explanation:**

- **Import necessary modules**: We import DAG, S3Hook, days_ago, and PythonOperator.
- **Define the DAG**: We create a DAG with a unique dag_id, a start_date, and a schedule_interval.
- **Define the download_from_s3 function**:
  - Creates an S3Hook instance using the aws_default connection.
  - Defines the S3 key, the bucket_name, and the local_path where the downloaded file will be saved. Important: Replace 'your-s3-bucket' with the actual name of your S3 bucket and ensure the key matches the file you uploaded in the previous example.
  - Calls the download_file method of the S3Hook to download the file from S3.
  - Prints a confirmation message to the console.
 
- **Create a PythonOperator**:
  - Creates a PythonOperator named download_task that executes the download_from_s3 function.
  - Sets the task_id to download_file_from_s3.
  - Sets the python_callable to the download_from_s3 function.
 
- **Set task dependencies (implicit)**: In this simple example, there's only one task, so no explicit dependencies are needed.

#### <a name="chapter3part2.2"></a>Chapter 3 - Part 2.2: Understanding S3FileTransferOperator

The S3FileTransferOperator is a specialized Airflow operator that simplifies the process of transferring files between S3 buckets or between your local filesystem and S3. It encapsulates the logic for copying files, making your DAGs cleaner and easier to read.

**Key Features of S3FileTransferOperator**

- **Simplified Syntax**: It provides a concise way to define file transfer tasks without writing custom Python code.
- **Flexibility**: It supports transferring single files or entire directories.
- **Efficiency**: It leverages the underlying boto3 library for efficient data transfer.
- **Idempotency**: The operator can be configured to be idempotent, ensuring that the transfer is only performed once, even if the task is retried.

**Using the S3FileTransferOperator**

To use the S3FileTransferOperator, you need to specify the source and destination locations, as well as the S3 connection ID.

```py
from airflow import DAG
from airflow.providers.amazon.aws.transfers.s3_to_s3 import S3ToS3TransferOperator
from airflow import utils
import datetime as dt

with DAG(
    dag_id='s3_file_transfer_example',
    start_date=utils.dates.days_ago(2),
    schedule_interval=None,
    catchup=False
) as dag:
    transfer_task = S3ToS3TransferOperator(
        task_id='transfer_file_s3_to_s3',
        source_s3_key='s3_file.txt',  # Replace with the source S3 key
        dest_s3_key='s3_file_copy.txt',  # Replace with the destination S3 key
        source_bucket_name='your-s3-bucket',  # Replace with your source bucket name
        dest_bucket_name='your-s3-bucket',  # Replace with your destination bucket name (can be the same)
        aws_conn_id='aws_default',
        replace=True  # Overwrite if the destination file exists
    )
```

**Explanation:**

- **from airflow.providers.amazon.aws.transfers.s3_to_s3 import S3ToS3TransferOperator**: This line imports the S3ToS3TransferOperator class.
- **transfer_task = S3ToS3TransferOperator(...)**: This line creates an instance of the S3ToS3TransferOperator.
  - **task_id**: A unique identifier for the task.
  - **source_s3_key**: The S3 key (path) of the file to transfer.
  - **dest_s3_key**: The S3 key (path) where the file will be copied.
  - **source_bucket_name**: The name of the source S3 bucket.
  - **dest_bucket_name**: The name of the destination S3 bucket.
  - **aws_conn_id**: The Airflow connection ID for your AWS credentials.
  - **replace**: If True, overwrites the destination file if it already exists.
 
**Key Parameters of S3FileTransferOperator**

- **source_s3_key**: The S3 key of the file to transfer.
- **dest_s3_key**: The S3 key where the file will be copied.
- **source_bucket_name**: The name of the source S3 bucket.
- **dest_bucket_name**: The name of the destination S3 bucket.
- **aws_conn_id**: The Airflow connection ID for your AWS credentials.
- **replace**: If True, overwrites the destination file if it already exists.
- **verify**: Whether or not to verify the SSL certificate for S3.
- **copy_object**: Whether to use copy_object or get_object followed by put_object. copy_object is more efficient, but may not be supported by all S3-compatible storage.

**Example: Transferring a File Between S3 Buckets**

The previous example demonstrates transferring a file within the same bucket. You can easily modify it to transfer a file between different buckets by changing the source_bucket_name and dest_bucket_name parameters. Make sure your AWS credentials have the necessary permissions to access both buckets.

**Example: Transferring all objects with a prefix**

```py
from airflow import DAG
from airflow.providers.amazon.aws.transfers.s3_to_s3 import S3ToS3TransferOperator
from airflow import utils
import datetime as dt

with DAG(
    dag_id='s3_file_transfer_prefix_example',
    start_date=utils.dates.days_ago(2),
    schedule_interval=None,
    catchup=False
) as dag:
    transfer_task = S3ToS3TransferOperator(
        task_id='transfer_files_with_prefix',
        source_s3_key='data/',  # Replace with the source S3 prefix
        dest_s3_key='processed_data/',  # Replace with the destination S3 prefix
        source_bucket_name='your-source-bucket',  # Replace with your source bucket name
        dest_bucket_name='your-destination-bucket',  # Replace with your destination bucket name
        aws_conn_id='aws_default',
        replace=True,  # Overwrite if the destination file exists
        prefix=True  # Transfer all objects with the specified prefix
    )
```

**Explanation:**

- **prefix=True**: This parameter tells the operator to transfer all objects in the source bucket that start with the source_s3_key prefix.
- **source_s3_key='data/'**: This specifies that all objects in the source bucket with keys starting with "data/" should be transferred.
- **dest_s3_key='processed_data/'**: This specifies that the transferred objects should be placed in the destination bucket under the "processed_data/" prefix. The original object names will be preserved under this new prefix.

#### <a name="chapter3part2.3"></a>Chapter 3 - Part 2.3: Real-World Application

Data transfer operators like S3Hook and S3FileTransferOperator are fundamental building blocks in many real-world data pipelines. Here are a few examples:

- **Data Ingestion**: Moving data from various sources (e.g., web server logs, application databases) to a central data lake in S3 for further processing. The S3Hook can be used to upload these files.
- **ETL (Extract, Transform, Load)**: Transferring data between S3 buckets as part of an ETL process. For example, moving raw data from a landing zone to a staging area, and then to a data warehouse after transformation. The S3FileTransferOperator is ideal for this.
- **Backup and Archiving**: Copying data from one S3 bucket to another for backup or archival purposes. This can be automated using Airflow and the S3FileTransferOperator.
- **Disaster Recovery**: Replicating data across different AWS regions for disaster recovery. The S3FileTransferOperator can be used to automate this replication process.

In each of these scenarios, Airflow provides the orchestration and scheduling capabilities, while the S3Hook and S3FileTransferOperator handle the actual data transfer.

#### <a name="chapter3part3"></a>Chapter 3 - Part 3: Using the PostgresOperator to Interact with Databases

The PostgresOperator is a crucial tool in Airflow for interacting with PostgreSQL databases. It allows you to execute SQL commands, manage database schemas, and perform data manipulation tasks directly from your DAGs. This eliminates the need for external scripts or manual database interactions, streamlining your data pipelines and ensuring consistency. By leveraging the PostgresOperator, you can automate complex database operations, making your workflows more efficient and reliable.

#### <a name="chapter3part3.1"></a>Chapter 3 - Part 3.1: Understanding the PostgresOperator

The PostgresOperator in Airflow is designed to execute SQL queries against a PostgreSQL database. It's a wrapper around the psycopg2 library, which is the most popular PostgreSQL adapter for Python. The operator handles the connection to the database, executes the provided SQL, and manages the transaction.

**Key Parameters**

- **task_id (str)**: A unique identifier for the task within the DAG.
- **postgres_conn_id (str)**: The Airflow connection ID that specifies the PostgreSQL connection details. This connection should be configured in the Airflow UI (Admin -> Connections).
- **sql (str or list[str])**: The SQL query or a list of SQL queries to execute.
- **parameters (dict or tuple or list)**: (optional) Parameters to pass into the SQL query. This is useful for preventing SQL injection and making your queries more dynamic.
- **autocommit (bool)**: (optional) Whether to automatically commit the transaction after executing the SQL. Defaults to False.
- **database (str)**: (optional) The database to use. If not specified, the database from the connection will be used.

**Connection Configuration**

Before using the PostgresOperator, you need to configure a connection in the Airflow UI. This connection stores the credentials and connection details for your PostgreSQL database.

- Go to Admin -> Connections in the Airflow UI.
- Click the "+" button to create a new connection.
- Set the "Conn Id" to a meaningful name (e.g., postgres_default). This is the postgres_conn_id you'll use in your DAG.
- Choose "Postgres" as the "Conn Type".
- Fill in the "Host", "Schema" (database name), "Login", and "Password" fields with your PostgreSQL credentials.
- You can optionally specify the "Port" if it's different from the default (5432).
- Save the connection.

**Example DAG**

Here's a basic example of using the PostgresOperator in a DAG:

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime

with DAG(
    dag_id='postgres_operator_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Create a table
    create_table = PostgresOperator(
        task_id='create_table',
        postgres_conn_id='postgres_default',
        sql="""
            CREATE TABLE IF NOT EXISTS my_table (
                id SERIAL PRIMARY KEY,
                name VARCHAR(255),
                value INTEGER
            );
        """
    )

    # Insert data into the table
    insert_data = PostgresOperator(
        task_id='insert_data',
        postgres_conn_id='postgres_default',
        sql="""
            INSERT INTO my_table (name, value) VALUES ('example', 123);
        """
    )

    create_table >> insert_data
```

In this example:

- We define a DAG called postgres_operator_example.
- The create_table task uses the PostgresOperator to create a table named my_table if it doesn't already exist.
- The insert_data task uses the PostgresOperator to insert a row into my_table.
- We define a task dependency to ensure that the table is created before data is inserted.

#### <a name="chapter3part3.2"></a>Chapter 3 - Part 3.2: Advanced Usage and Best Practices

**Using Parameters to Prevent SQL Injection**

It's crucial to use parameters when your SQL queries include user-provided data or data from other tasks. This prevents SQL injection vulnerabilities.

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime

with DAG(
    dag_id='postgres_operator_with_params',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    insert_data_with_params = PostgresOperator(
        task_id='insert_data_with_params',
        postgres_conn_id='postgres_default',
        sql="""
            INSERT INTO my_table (name, value) VALUES (%s, %s);
        """,
        parameters=('dynamic_name', 456)
    )
```

In this example, %s acts as a placeholder for the values provided in the parameters tuple. The psycopg2 library will properly escape these values, preventing SQL injection.

**Executing Multiple SQL Statements**

The PostgresOperator can execute multiple SQL statements in a single task. This can be useful for performing a series of related operations.

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime

with DAG(
    dag_id='postgres_operator_multiple_sql',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    multiple_sql = PostgresOperator(
        task_id='multiple_sql',
        postgres_conn_id='postgres_default',
        sql=[
            "INSERT INTO my_table (name, value) VALUES ('first', 1);",
            "INSERT INTO my_table (name, value) VALUES ('second', 2);"
        ]
    )
```

Here, the sql parameter is a list of SQL statements. The operator will execute each statement in the order it appears in the list.

**Using autocommit**

The autocommit parameter controls whether the transaction is automatically committed after the SQL is executed. If autocommit is False (the default), you need to explicitly commit the transaction using a separate SQL statement (e.g., COMMIT;). Setting autocommit to True can simplify your DAGs, but it's important to understand the implications for data consistency.

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime

with DAG(
    dag_id='postgres_operator_autocommit',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    insert_data_autocommit = PostgresOperator(
        task_id='insert_data_autocommit',
        postgres_conn_id='postgres_default',
        sql="""
            INSERT INTO my_table (name, value) VALUES ('autocommit', 789);
        """,
        autocommit=True
    )
```

In this example, the autocommit parameter is set to True, so the transaction will be automatically committed after the INSERT statement is executed.

**Error Handling**

The PostgresOperator will raise an exception if the SQL query fails. Airflow's built-in retry mechanism will automatically retry the task if it fails. You can configure the number of retries and the delay between retries in the DAG definition or at the task level.

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime

with DAG(
    dag_id='postgres_operator_error_handling',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    default_args={'retries': 3, 'retry_delay': timedelta(minutes=5)}
) as dag:
    # This task will retry 3 times with a 5-minute delay if it fails
    failing_task = PostgresOperator(
        task_id='failing_task',
        postgres_conn_id='postgres_default',
        sql="""
            SELECT * FROM non_existent_table;
        """
    )
```

In this example, the failing_task will retry three times with a 5-minute delay if the SELECT query fails because the table non_existent_table does not exist.

**Idempotency**

As discussed in previous lessons, idempotency is a crucial concept in Airflow. When using the PostgresOperator, ensure that your SQL queries are idempotent, meaning that running them multiple times has the same effect as running them once.

For example, instead of using INSERT statements, consider using INSERT ... ON CONFLICT DO UPDATE or MERGE statements to ensure that your data is consistent even if the task is retried.

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime
from datetime import timedelta

with DAG(
    dag_id='postgres_operator_idempotency',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    default_args={'retries': 1, 'retry_delay': timedelta(minutes=1)}
) as dag:
    # Create a table with a unique constraint
    create_table_unique = PostgresOperator(
        task_id='create_table_unique',
        postgres_conn_id='postgres_default',
        sql="""
            CREATE TABLE IF NOT EXISTS unique_table (
                id SERIAL PRIMARY KEY,
                name VARCHAR(255) UNIQUE,
                value INTEGER
            );
        """
    )

    # Insert data using ON CONFLICT DO UPDATE for idempotency
    insert_data_idempotent = PostgresOperator(
        task_id='insert_data_idempotent',
        postgres_conn_id='postgres_default',
        sql="""
            INSERT INTO unique_table (name, value) VALUES ('unique_name', 100)
            ON CONFLICT (name) DO UPDATE SET value = EXCLUDED.value;
        """
    )

    create_table_unique >> insert_data_idempotent
```

In this example, the INSERT ... ON CONFLICT DO UPDATE statement ensures that if a row with the same name already exists, its value is updated instead of throwing an error. This makes the task idempotent.

#### <a name="chapter3part4"></a>Chapter 3 - Part 4: Understanding Idempotency and Task Retries

Idempotency and task retries are crucial concepts in Apache Airflow, especially when dealing with distributed systems and potentially unreliable operations. Understanding these concepts allows you to build more robust and reliable data pipelines. Idempotency ensures that even if a task is executed multiple times, the final outcome remains the same. Task retries provide a mechanism to automatically re-execute failed tasks, increasing the likelihood of successful DAG runs.

#### <a name="chapter3part4.1"></a>Chapter 3 - Part 4.1: Understanding Idempotency

Idempotency, in the context of Airflow, means that a task can be executed multiple times without changing the result beyond the initial execution. In other words, running an idempotent task once has the same effect as running it multiple times. This is particularly important in distributed systems like Airflow, where tasks might fail and be retried due to network issues, worker failures, or other transient errors.

**Why is Idempotency Important?**

- **Data Consistency**: Ensures that your data remains consistent even if tasks are retried. Without idempotency, retries could lead to duplicate data, incorrect calculations, or corrupted states.
- **Reliability**: Makes your DAGs more resilient to failures. If a task fails and is retried, you can be confident that it won't cause unintended side effects.
- **Debugging**: Simplifies debugging. When tasks are idempotent, you can easily re-run them without worrying about the consequences.

**Examples of Idempotent Operations**

- **Setting a Value**: Setting a specific value in a database or file is generally idempotent. For example, setting the value of a database field status to completed.
- **Deleting a File**: Deleting a file (if it exists) is idempotent. If the file doesn't exist, deleting it again has no effect.
- **Updating a Record with Specific Values**: Updating a database record with specific values (as opposed to incrementing a counter) can be idempotent.

**Examples of Non-Idempotent Operations**

- **Incrementing a Counter**: Incrementing a counter in a database is not idempotent. Each retry will increase the counter further.
- **Appending to a File**: Appending data to a file is not idempotent. Each retry will add the same data to the file again.
- **Sending an Email**: Sending an email is generally not idempotent. Each retry will send another email.

**Achieving Idempotency**

Achieving idempotency often requires careful design and implementation. Here are some common strategies:

- **Check-Then-Act**: Before performing an action, check if it has already been performed. For example, before processing a file, check if a flag file exists indicating that it has already been processed.
- **Unique Identifiers**: Use unique identifiers to track operations. For example, assign a unique ID to each record being processed and use this ID to prevent duplicates.
- **Atomic Operations**: Use atomic operations that either succeed completely or fail completely. This prevents partial updates that can lead to inconsistencies.
- **Upsert Operations**: Use "upsert" (update or insert) operations in databases. These operations either update an existing record or insert a new record if it doesn's already present.

**Example: Idempotent Data Processing**

Let's say you have a DAG that processes log files and loads the data into a database. To make this process idempotent, you can use a check-then-act approach.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime
import os
import logging

def process_log_file(file_path, processed_files_path):
    """
    Processes a log file and loads the data into a database.
    This function is designed to be idempotent.
    """
    file_name = os.path.basename(file_path)
    processed_file_flag = os.path.join(processed_files_path, f"{file_name}.processed")

    if os.path.exists(processed_file_flag):
        logging.info(f"File {file_path} already processed. Skipping.")
        return  # Already processed, skip

    try:
        # Simulate processing the log file and loading data into a database
        logging.info(f"Processing log file: {file_path}")
        # Replace this with your actual data processing logic
        with open(file_path, 'r') as f:
            for line in f:
                # Simulate loading data into a database
                logging.info(f"Loading data: {line.strip()}")

        # Create a flag file to indicate that the file has been processed
        with open(processed_file_flag, 'w') as f:
            f.write("Processed")

        logging.info(f"File {file_path} processed successfully.")

    except Exception as e:
        logging.error(f"Error processing file {file_path}: {e}")
        raise  # Re-raise the exception to trigger a retry

with DAG(
    dag_id='idempotent_data_processing',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example'],
) as dag:
    process_task = PythonOperator(
        task_id='process_log_file_task',
        python_callable=process_log_file,
        op_kwargs={
            'file_path': '/tmp/log_file.txt',  # Replace with your log file path
            'processed_files_path': '/tmp/processed_files' # Directory to store processed flags
        }
    )

# Create dummy log file and processed files directory for testing
os.makedirs('/tmp/processed_files', exist_ok=True)
with open('/tmp/log_file.txt', 'w') as f:
    f.write("Log entry 1\n")
    f.write("Log entry 2\n")
```

In this example, the process_log_file function first checks if a flag file exists indicating that the log file has already been processed. If the flag file exists, the function skips processing the file. Otherwise, it processes the file, loads the data into the database (simulated in the example), and creates the flag file. This ensures that the log file is processed only once, even if the task is retried.

#### <a name="chapter3part4.2"></a>Chapter 3 - Part 4.2: Understanding Task Retries

Task retries are a mechanism in Airflow to automatically re-execute a failed task. When a task fails, Airflow will retry it according to the retry configuration defined in the DAG. This is useful for handling transient errors, such as network issues, temporary service outages, or resource contention.

**Why Use Task Retries?**

- **Increased Reliability**: Retries can automatically recover from transient errors, reducing the need for manual intervention.
- **Reduced Downtime**: By automatically retrying failed tasks, you can minimize the impact of failures on your data pipelines.
- **Improved Efficiency**: Retries can save time and effort by automatically handling errors that would otherwise require manual investigation and resolution.

**Configuring Task Retries**

You can configure task retries using the retries and retry_delay parameters in the task definition.

- **retries**: Specifies the number of times a task should be retried before failing.
- **retry_delay**: Specifies the delay between retries, typically as a timedelta object.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime, timedelta

default_args = {
    'owner': 'airflow',
    'depends_on_past': False,
    'start_date': datetime(2023, 1, 1),
    'retries': 3,  # Retry the task up to 3 times
    'retry_delay': timedelta(minutes=5),  # Wait 5 minutes between retries
}

with DAG(
    dag_id='task_retries_example',
    default_args=default_args,
    schedule_interval=None,
    catchup=False,
    tags=['example'],
) as dag:
    # This task will simulate a failure on the first attempt and succeed on a retry
    failing_task = BashOperator(
        task_id='failing_task',
        bash_command="""
        if [ $AIRFLOW_ATTEMPT_NUMBER -eq 1 ]; then
            echo "Simulating failure on first attempt"
            exit 1
        else
            echo "Succeeding on retry"
            exit 0
        fi
        """
    )
```

In this example, the failing_task is configured to retry up to 3 times, with a 5-minute delay between retries. The bash_command simulates a failure on the first attempt by checking the AIRFLOW_ATTEMPT_NUMBER environment variable. On subsequent retries, it succeeds.

**Retry Strategies**

Airflow provides a simple retry mechanism, but you can implement more sophisticated retry strategies using custom logic. Some common strategies include:

- **Exponential Backoff**: Increase the retry delay exponentially with each retry. This can help avoid overwhelming a failing service.
- **Randomized Delay**: Add a random delay to the retry delay. This can help prevent multiple tasks from retrying at the same time and exacerbating the problem.
- **Circuit Breaker**: Stop retrying a task if it fails repeatedly within a certain time period. This can help prevent wasting resources on tasks that are unlikely to succeed.

**Example: Exponential Backoff**

You can implement exponential backoff using a PythonOperator and a custom retry function.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime, timedelta
import time
import random
import logging

def my_task(attempt_number):
    """
    Simulates a task that may fail and retries with exponential backoff.
    """
    if attempt_number < 3:  # Simulate failure for the first 2 attempts
        logging.error(f"Task failed on attempt {attempt_number}. Retrying...")
        raise ValueError(f"Simulated failure on attempt {attempt_number}")
    else:
        logging.info(f"Task succeeded on attempt {attempt_number}.")
        return "Task completed successfully"

def retry_with_exponential_backoff(context):
    """
    Calculates the retry delay using exponential backoff.
    """
    attempt = context['ti'].try_number
    delay = 2 ** (attempt - 1) + random.uniform(0, 1)  # Exponential backoff with jitter
    logging.info(f"Retry attempt {attempt}, waiting {delay:.2f} seconds.")
    time.sleep(delay)  # Simulate waiting before retrying
    return delay

with DAG(
    dag_id='exponential_backoff_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example'],
) as dag:
    task = PythonOperator(
        task_id='my_task',
        python_callable=my_task,
        op_kwargs={'attempt_number': '{{ ti.try_number }}'},
        retries=5,  # Maximum number of retries
        retry_delay=timedelta(seconds=1), # Initial retry delay (overridden by custom retry)
        on_failure_callback=retry_with_exponential_backoff,
    )
```

In this example, the retry_with_exponential_backoff function calculates the retry delay using an exponential backoff formula. The on_failure_callback parameter is used to specify this function as the callback to be executed when the task fails. The ti.try_number variable provides the current attempt number.

#### <a name="chapter3part4.3"></a>Chapter 3 - Part 4.3: Real-World Application

Consider a scenario where you are building a data pipeline to ingest data from a third-party API. The API might be unreliable and experience occasional outages. To handle these outages, you can implement task retries with exponential backoff.

- **Task Definition**: Define a PythonOperator task that calls the API to retrieve data.
- **Retry Configuration**: Configure the task to retry up to 5 times with an initial delay of 1 minute and exponential backoff.
- **Idempotency**: Implement idempotency by storing the retrieved data in a database using an upsert operation. This ensures that if the task is retried, it won't create duplicate records.
- **Error Handling**: Add error handling to catch API errors and log them.
- **Alerting**: Configure alerting to notify you if the task fails after all retries have been exhausted.

#### <a name="chapter3part5"></a>Chapter 3 - Part 5: Best Practices for Operator Usage

Airflow operators are the building blocks of your workflows, defining the individual tasks that need to be executed. Choosing the right operator and using it effectively is crucial for building robust, maintainable, and efficient data pipelines. This lesson delves into best practices for operator usage, focusing on idempotency, retries, and proper operator selection to ensure your Airflow DAGs run smoothly and reliably.

#### <a name="chapter3part5.1"></a>Chapter 3 - Part 5.1: Understanding Operator Idempotency

Idempotency is a critical concept in distributed systems, and it's particularly important in Airflow. An operation is idempotent if it can be applied multiple times without changing the result beyond the initial application. In the context of Airflow operators, this means that if a task is retried (due to failure or other reasons), running the operator again should not cause unintended side effects or data corruption.

**Why Idempotency Matters in Airflow**

Airflow is designed to handle failures gracefully. When a task fails, Airflow will often retry it. If your operators are not idempotent, retries can lead to inconsistent data, duplicate processing, or other undesirable outcomes.

Example: Imagine an operator that transfers data from a source to a destination. If the operator is not idempotent, a retry might cause the same data to be transferred multiple times, resulting in duplicate records in the destination.

**Achieving Idempotency**

There are several strategies for making your Airflow operators idempotent:

- **Check-then-Act**: Before performing an action, check if it has already been done. If it has, skip the action.

Example: Before inserting a record into a database, check if the record already exists.

```py
from airflow.providers.postgres.hooks.postgres import PostgresHook
from airflow.models import BaseOperator
from airflow.utils.decorators import apply_defaults

class IdempotentPostgresOperator(BaseOperator):
    """
    Custom operator to insert data into Postgres, ensuring idempotency.
    """
    template_fields = ('sql', 'postgres_conn_id')

    @apply_defaults
    def __init__(self,
                 sql,
                 postgres_conn_id,
                 *args, **kwargs):
        super(IdempotentPostgresOperator, self).__init__(*args, **kwargs)
        self.sql = sql
        self.postgres_conn_id = postgres_conn_id

    def execute(self, context):
        postgres_hook = PostgresHook(postgres_conn_id=self.postgres_conn_id)
        # Extract the values to check for existence (example: checking if a record with a specific ID exists)
        # This part depends on your specific SQL query and how you identify duplicates
        # For simplicity, let's assume the SQL inserts a record with a unique ID
        # and we can extract that ID from the SQL query.  This is a placeholder.
        # In a real scenario, you'd need to parse the SQL or have a more robust method.
        unique_id = self.extract_id_from_sql(self.sql) # Replace with actual extraction logic

        if self.record_exists(postgres_hook, unique_id):
            self.log.info(f"Record with ID {unique_id} already exists. Skipping insertion.")
            return  # Skip insertion if the record already exists

        postgres_hook.run(self.sql)
        self.log.info("Data inserted successfully.")

    def extract_id_from_sql(self, sql):
        """
        Placeholder function to extract the unique ID from the SQL query.
        Replace this with your actual logic to parse the SQL and extract the ID.
        """
        # This is a simplified example.  In reality, you'd need a robust SQL parser.
        # Assuming the SQL is like "INSERT INTO table (id, ...) VALUES (123, ...)"
        try:
            start_index = sql.find("VALUES (") + len("VALUES (")
            end_index = sql.find(",", start_index)  # Find the first comma after "VALUES ("
            if end_index == -1:
                end_index = sql.find(")", start_index) # Or the closing parenthesis
            unique_id_str = sql[start_index:end_index].strip()
            return int(unique_id_str)
        except:
            return None # Or raise an exception if ID extraction fails

    def record_exists(self, postgres_hook, unique_id):
        """
        Checks if a record with the given ID already exists in the database.
        """
        if unique_id is None:
            return False # Cannot check if ID is not available

        check_sql = f"SELECT EXISTS (SELECT 1 FROM your_table WHERE id = {unique_id})" # Replace your_table and id
        result = postgres_hook.get_first(check_sql)
        return result[0]  # Returns True if the record exists, False otherwise
```

Explanation: This custom operator checks if a record with a specific ID already exists in the database before attempting to insert it. The extract_id_from_sql function is a placeholder and needs to be replaced with actual logic to parse the SQL query and extract the unique ID. The record_exists function then queries the database to check for the existence of the record.

- **Use Unique Identifiers**: Assign unique identifiers to your data and use them to track which records have already been processed.

Example: When processing files, use the file's name and modification timestamp as a unique identifier. Store these identifiers in a database or other persistent storage.

- **Atomic Operations**: Use atomic operations that either succeed completely or fail completely. This prevents partial updates that can lead to inconsistencies.

Example: When updating a database record, use a transaction to ensure that all changes are applied together or none at all.

- **Upsert Operations**: Use "upsert" (update or insert) operations that either update an existing record or insert a new one if it doesn't exist.

Example: Many databases provide upsert functionality (e.g., ON CONFLICT DO UPDATE in PostgreSQL).

```py
# Example using PostgresOperator with ON CONFLICT DO UPDATE
from airflow.providers.postgres.operators.postgres import PostgresOperator

upsert_task = PostgresOperator(
    task_id='upsert_data',
    postgres_conn_id='your_postgres_connection',
    sql="""
    INSERT INTO your_table (id, column1, column2)
    VALUES (123, 'value1', 'value2')
    ON CONFLICT (id) DO UPDATE
    SET column1 = EXCLUDED.column1, column2 = EXCLUDED.column2;
    """
)
```

Explanation: This PostgresOperator uses the ON CONFLICT DO UPDATE clause to either insert a new record or update an existing one if a conflict on the id column is detected. EXCLUDED refers to the values proposed for insertion.

**Hypothetical Scenario**

Imagine you're building a DAG that processes customer orders. Each order has a unique order ID. Your DAG includes a task that sends an email confirmation to the customer. If the email-sending task fails and is retried, the customer might receive multiple confirmation emails. To make this task idempotent, you could:

- Store a record of each email that has been sent in a database.
- Before sending an email, check if a record exists for the order ID.
- If a record exists, skip sending the email.

#### <a name="chapter3part5.2"></a>Chapter 3 - Part 5.2: Configuring Task Retries

Airflow provides built-in support for task retries. You can configure the number of retries and the delay between retries at the DAG level or at the task level.

**retries and retry_delay Parameters**

The retries parameter specifies the number of times a task should be retried if it fails. The retry_delay parameter specifies the time (as a timedelta object) to wait between retries.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime, timedelta

default_args = {
    'owner': 'airflow',
    'depends_on_past': False,
    'start_date': datetime(2024, 1, 1),
    'retries': 3,
    'retry_delay': timedelta(minutes=5)
}

dag = DAG(
    'retry_example',
    default_args=default_args,
    schedule_interval=None
)

task1 = BashOperator(
    task_id='failing_task',
    bash_command='exit 1',  # This command will always fail
    dag=dag
)
```

Explanation: In this example, the failing_task will be retried up to 3 times, with a 5-minute delay between each retry.

**Retry Strategies**

Airflow offers different retry strategies to handle task failures:

- **Simple Retries**: The task is retried a fixed number of times with a fixed delay between each retry (as shown in the previous example).

- **Exponential Backoff**: The delay between retries increases exponentially. This can be useful for handling transient errors that might resolve themselves over time.

While Airflow doesn't have built-in exponential backoff, you can implement it using custom logic within your task or by using a library like tenacity.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime, timedelta
import time
import random

def my_failing_function():
    """
    A function that fails randomly to simulate a transient error.
    """
    if random.random() < 0.5:  # 50% chance of failure
        raise Exception("Simulated failure")
    else:
        print("Function succeeded")

def task_with_exponential_backoff(context):
    """
    A task that retries with exponential backoff.
    """
    max_retries = 5
    base_delay = 1  # seconds
    for attempt in range(max_retries):
        try:
            my_failing_function()
            print("Task succeeded after", attempt, "retries")
            return  # Exit the function if it succeeds
        except Exception as e:
            print(f"Attempt {attempt + 1} failed: {e}")
            if attempt == max_retries - 1:
                raise  # Re-raise the exception if max retries reached
            delay = base_delay * (2 ** attempt)  # Exponential backoff
            print(f"Waiting {delay} seconds before retrying...")
            time.sleep(delay)

with DAG(
    'exponential_backoff_example',
    default_args={
        'owner': 'airflow',
        'depends_on_past': False,
        'start_date': datetime(2024, 1, 1),
    },
    schedule_interval=None,
    catchup=False,
) as dag:
    task = PythonOperator(
        task_id='exponential_backoff_task',
        python_callable=task_with_exponential_backoff,
    )
```

Explanation: This example demonstrates how to implement exponential backoff within a PythonOperator. The task_with_exponential_backoff function retries the my_failing_function with an exponentially increasing delay.

**Best Practices for Retries**

- **Set reasonable retry values**: Don't set the number of retries too high, as this can lead to excessive resource consumption. Consider the nature of the task and the likelihood of transient errors.
- **Use exponential backoff for transient errors**: For errors that are likely to resolve themselves over time (e.g., network connectivity issues), use exponential backoff.
- **Avoid retries for permanent errors**: For errors that are unlikely to resolve themselves (e.g., invalid input data), avoid retrying the task. Instead, implement error handling to alert you to the issue.
- **Consider using SLAs**: Airflow allows you to define Service Level Agreements (SLAs) for your DAGs and tasks. If a task fails to meet its SLA, Airflow can send an alert. This can be a useful way to monitor the performance of your DAGs and identify tasks that are frequently failing.

**Real-World Application**

A data engineering team uses Airflow to ingest data from various sources, transform it, and load it into a data warehouse. One of the data sources is an external API that is known to be unreliable. To handle this, the team configures the task that calls the API to retry up to 5 times with exponential backoff. This ensures that the DAG can recover from transient API outages without manual intervention.

#### <a name="chapter3part5.3"></a>Chapter 3 - Part 5.3: Choosing the Right Operator

Airflow provides a wide range of operators for different tasks. Choosing the right operator is essential for building efficient and maintainable DAGs.

**General-Purpose Operators**

- **BashOperator**: Executes a bash command. Useful for running simple scripts or system commands.
- **PythonOperator**: Executes a Python function. Useful for performing complex logic or interacting with external libraries.
- **EmailOperator**: Sends an email. Useful for sending notifications or alerts.

**Data Transfer Operators**
- **S3FileTransferOperator**: Transfers files between S3 buckets.
- **SFTPOperator**: Transfers files to/from an SFTP server.

**Database Operators**
- **PostgresOperator**: Executes SQL commands in a PostgreSQL database.
- **MySqlOperator**: Executes SQL commands in a MySQL database.
- **BigQueryOperator**: Executes queries in Google BigQuery.

**Cloud Operators**

Airflow has a rich ecosystem of operators for interacting with cloud services like AWS, Google Cloud, and Azure. These operators provide a convenient way to perform tasks such as:

- Launching and managing virtual machines
- Storing and retrieving data from cloud storage services
- Running machine learning models

**Custom Operators**

If none of the built-in operators meet your needs, you can create your own custom operators. This allows you to encapsulate complex logic or interact with systems that are not supported by the standard operators.

**Best Practices for Operator Selection**

- **Use the most specific operator available**: If there is a specific operator for the task you need to perform (e.g., S3FileTransferOperator for transferring files between S3 buckets), use it instead of a more general-purpose operator like BashOperator or PythonOperator.
- **Consider the operator's dependencies**: Some operators have external dependencies (e.g., the PostgresOperator requires the psycopg2 library). Make sure that these dependencies are installed in your Airflow environment.
- **Read the operator's documentation**: Before using an operator, read its documentation to understand its parameters, behavior, and limitations.
- **Test your operators thoroughly**: After implementing a task with an operator, test it thoroughly to ensure that it works as expected.

## <a name="chapter4"></a>Chapter 4: Variables and Connections

#### <a name="chapter4part1"></a>Chapter 4 - Part 1: Introduction to Airflow Variables

Airflow Variables are a fundamental component for managing dynamic configurations and sensitive information within your workflows. They provide a centralized and accessible way to store and retrieve values that can be used across different DAGs and tasks. This lesson will explore how to effectively use Airflow Variables to enhance the flexibility and maintainability of your data pipelines.

#### <a name="chapter4part1.1"></a>Chapter 4 - Part 1.1: Understanding Airflow Variables

Airflow Variables are key-value pairs stored in the Airflow metadata database. They allow you to externalize configuration settings from your DAG code, making your DAGs more adaptable to different environments and use cases. Instead of hardcoding values directly into your DAGs, you can store them as variables and retrieve them at runtime.

**Key Characteristics of Airflow Variables**

- **Centralized Storage**: Variables are stored in the Airflow metadata database, providing a single source of truth for configuration values.
- **Dynamic Configuration**: Variables can be updated without modifying the DAG code, allowing you to change the behavior of your workflows without redeploying them.
- **Accessibility**: Variables can be accessed from within your DAGs using the Variable class.
- **Security**: While not designed for highly sensitive secrets, variables can be used to store configuration values that you don't want to hardcode in your DAGs. For sensitive information, Airflow Connections or Secrets Backends are more appropriate.
- **Data Types**: Variables are stored as strings, but can be parsed into other data types (integers, booleans, lists, dictionaries) within your DAGs.

**When to Use Airflow Variables**

- **Environment-Specific Settings**: Store database connection details, API keys, or file paths that vary between development, staging, and production environments.
- **Configuration Parameters**: Store parameters that control the behavior of your tasks, such as batch sizes, thresholds, or retry limits.
- **Dynamic Values**: Store values that are calculated or updated outside of the DAG code, such as the date of the last successful data load.
- **Feature Flags**: Use variables to enable or disable certain features in your DAGs, allowing you to test new functionality without deploying new code.

**When NOT to Use Airflow Variables**

- **Highly Sensitive Secrets**: For storing passwords, API keys, or other highly sensitive information, use Airflow Connections or a Secrets Backend. These provide encryption and access control mechanisms that are not available with variables.
- **Large Data**: Variables are not designed for storing large amounts of data. If you need to share large datasets between tasks, use XComs (covered in a later module) or external storage systems like S3.
- **Frequently Changing Values**: If a value changes very frequently (e.g., every few seconds), storing it in a variable might not be the most efficient approach. Consider using a real-time data stream or a dedicated configuration management system.

#### <a name="chapter4part1.2"></a>Chapter 4 - Part 1.2: Setting and Retrieving Variables

Airflow provides several ways to set and retrieve variables: the Airflow UI, the Airflow CLI, and within DAGs using Python code.

**Setting Variables in the Airflow UI**

The Airflow UI provides a user-friendly interface for managing variables.

- Navigate to the "Admin" tab and select "Variables".
- Click the "Create" button to add a new variable.
- Enter a key (name) and a value for the variable.
- Click "Save" to store the variable in the metadata database.

**Setting Variables Using the Airflow CLI**

The Airflow CLI allows you to manage variables from the command line.

```
# Set a variable
airflow variables set my_variable "my_value"

# Get a variable
airflow variables get my_variable

# Delete a variable
airflow variables delete my_variable
```

**Retrieving Variables in DAGs**

Within your DAGs, you can retrieve variables using the Variable class from airflow.models.variable.

```py
from airflow.models.variable import Variable
from airflow import DAG
from airflow.operators.python import PythonOperator
import datetime as dt

def print_variable():
    my_variable = Variable.get("my_variable")
    print(f"The value of my_variable is: {my_variable}")

with DAG(
    dag_id="variable_example",
    start_date=dt.datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
) as dag:
    print_variable_task = PythonOperator(
        task_id="print_variable",
        python_callable=print_variable,
    )
```

In this example, the Variable.get("my_variable") method retrieves the value of the variable named "my_variable".

**Data Type Considerations**

Airflow Variables are stored as strings. If you need to use a variable as a different data type (e.g., integer, boolean, list, dictionary), you'll need to convert it within your DAG.

```py
import json
from airflow.models.variable import Variable
from airflow import DAG
from airflow.operators.python import PythonOperator
import datetime as dt

def use_variable_data_types():
    # Get string variable
    string_variable = Variable.get("string_variable")
    print(f"String variable: {string_variable}, Type: {type(string_variable)}")

    # Get integer variable
    integer_variable = int(Variable.get("integer_variable"))
    print(f"Integer variable: {integer_variable}, Type: {type(integer_variable)}")

    # Get boolean variable
    boolean_variable = Variable.get("boolean_variable").lower() == 'true'
    print(f"Boolean variable: {boolean_variable}, Type: {type(boolean_variable)}")

    # Get list variable
    list_variable = json.loads(Variable.get("list_variable"))
    print(f"List variable: {list_variable}, Type: {type(list_variable)}")

    # Get dictionary variable
    dict_variable = json.loads(Variable.get("dict_variable"))
    print(f"Dictionary variable: {dict_variable}, Type: {type(dict_variable)}")

with DAG(
    dag_id="variable_data_types",
    start_date=dt.datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
) as dag:
    use_variable_data_types_task = PythonOperator(
        task_id="use_variable_data_types",
        python_callable=use_variable_data_types,
    )
```

In this example, the json.loads() function is used to parse the list and dictionary variables from their string representation.

#### <a name="chapter4part1.3"></a>Chapter 4 - Part 1.3: Practical Examples

**Example 1: Database Connection Details**

Instead of hardcoding database connection details in your DAG, you can store them as variables.

- Set the following variables in the Airflow UI or CLI:
  - **db_host**: your_db_host
  - **db_port**: 5432
  - **db_name**: your_db_name
  - **db_user**: your_db_user
 
- Retrieve the variables in your DAG and use them to establish a database connection.

```py
from airflow.models.variable import Variable
from airflow import DAG
from airflow.operators.python import PythonOperator
import datetime as dt
import psycopg2  # Or your preferred database library

def connect_to_database():
    db_host = Variable.get("db_host")
    db_port = int(Variable.get("db_port"))
    db_name = Variable.get("db_name")
    db_user = Variable.get("db_user")
    db_password = Variable.get("db_password") #It is better to use connection for passwords

    try:
        conn = psycopg2.connect(
            host=db_host,
            port=db_port,
            database=db_name,
            user=db_user,
            password=db_password
        )
        print("Successfully connected to the database!")
        conn.close()
    except Exception as e:
        print(f"Error connecting to the database: {e}")

with DAG(
    dag_id="database_connection_example",
    start_date=dt.datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
) as dag:
    connect_to_database_task = PythonOperator(
        task_id="connect_to_database",
        python_callable=connect_to_database,
    )
```

Note: It's highly recommended to store passwords using Airflow Connections or Secrets Backends instead of variables.

**Example 2: API Endpoint**

Store the API endpoint as a variable to easily switch between different environments (e.g., development, staging, production).

- Set the api_endpoint variable in the Airflow UI or CLI:
  - **api_endpoint**: https://api.example.com/v1
 
- Retrieve the variable in your DAG and use it to make API requests.

```py
from airflow.models.variable import Variable
from airflow import DAG
from airflow.operators.python import PythonOperator
import datetime as dt
import requests

def call_api():
    api_endpoint = Variable.get("api_endpoint")
    response = requests.get(f"{api_endpoint}/data")
    print(f"API response: {response.text}")

with DAG(
    dag_id="api_call_example",
    start_date=dt.datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
) as dag:
    call_api_task = PythonOperator(
        task_id="call_api",
        python_callable=call_api,
    )
```

**Example 3: Feature Flags**

Use variables to enable or disable certain features in your DAG.

- Set the enable_feature_x variable in the Airflow UI or CLI:
  - **enable_feature_x**: True
 
- Retrieve the variable in your DAG and use it to conditionally execute code.

```py
from airflow.models.variable import Variable
from airflow import DAG
from airflow.operators.python import PythonOperator
import datetime as dt

def run_feature_x():
    print("Running Feature X!")

def run_default_task():
    print("Running Default Task!")

def check_feature_flag():
    enable_feature_x = Variable.get("enable_feature_x").lower() == 'true'
    if enable_feature_x:
        run_feature_x()
    else:
        run_default_task()

with DAG(
    dag_id="feature_flag_example",
    start_date=dt.datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
) as dag:
    check_feature_flag_task = PythonOperator(
        task_id="check_feature_flag",
        python_callable=check_feature_flag,
    )
```

#### <a name="chapter4part2"></a>Chapter 4 - Part 2: Setting and Retrieving Variables in the UI and DAGs

Airflow Variables are a crucial component for managing dynamic configurations and sensitive information within your workflows. They provide a centralized and easily accessible way to store and retrieve values that can be used across different DAGs and tasks. This lesson will delve into the process of setting and retrieving Airflow Variables through both the Airflow UI and directly within your DAG definitions, ensuring you understand how to effectively leverage this feature for building robust and maintainable data pipelines.

#### <a name="chapter4part2.1"></a>Chapter 4 - Part 2.1: Understanding Airflow Variables

Airflow Variables are key-value pairs stored in the Airflow metadata database. They allow you to decouple configuration values from your DAG code, making your DAGs more flexible and easier to manage. Instead of hardcoding values like API keys, database connection strings, or file paths directly into your DAGs, you can store them as Variables and retrieve them at runtime.

**Benefits of Using Variables**

- **Centralized Configuration**: Manage all your configuration values in one place, making it easier to update and maintain them.
- **Dynamic DAG Behavior**: Modify DAG behavior without changing the DAG code itself.
- **Security**: Store sensitive information like passwords and API keys securely (though Connections are generally preferred for credentials).
- **Reusability**: Use the same Variables across multiple DAGs.
- **Environment-Specific Configuration**: Easily switch between different configurations for development, testing, and production environments.

**When to Use Variables**

- Storing configuration settings that might change over time.
- Passing parameters to tasks that need to be configurable.
- Managing environment-specific settings.
- Storing small amounts of data that need to be accessed by multiple DAGs.

**Real-World Example 1: Database Connection Details**

Imagine you have a DAG that extracts data from a PostgreSQL database. Instead of hardcoding the database host, port, username, and password in your DAG, you can store them as Airflow Variables. This allows you to easily change the database connection details without modifying the DAG code.

**Real-World Example 2: API Keys**

If your DAG interacts with a third-party API, you can store the API key as an Airflow Variable. This is especially useful if you have different API keys for different environments (e.g., development and production).

**Hypothetical Scenario: Feature Flags**

Suppose you're developing a new feature in your data pipeline. You can use an Airflow Variable to enable or disable the feature. This allows you to test the feature in production without affecting all users.

#### <a name="chapter4part2.2"></a>Chapter 4 - Part 2.2: Setting Variables in the Airflow UI

The Airflow UI provides a user-friendly interface for managing Variables.

**Accessing the Variables Section**

- Log in to the Airflow UI.
- Navigate to the "Admin" tab.
- Click on "Variables".

**Creating a New Variable**

- In the Variables section, click on the "Create" button.
- Enter a key for the variable (e.g., database_host).
- Enter a value for the variable (e.g., localhost).
- Optionally, you can provide a description for the variable.
- Click on the "Save" button.

**Editing an Existing Variable**

- In the Variables section, find the variable you want to edit.
- Click on the "Edit" button (usually a pencil icon) next to the variable.
- Modify the value or description of the variable.
- Click on the "Save" button.

**Deleting a Variable**

- In the Variables section, find the variable you want to delete.
- Click on the "Delete" button (usually a trash can icon) next to the variable.
- Confirm the deletion.

#### <a name="chapter4part2.3"></a>Chapter 4 - Part 2.3: Retrieving Variables in DAGs

You can retrieve Airflow Variables within your DAGs using the Variable class from the airflow.models.variable module.

**Importing the Variable Class**

First, import the Variable class into your DAG file:

```py
from airflow.models.variable import Variable
```

**Retrieving a Variable Value**

Use the Variable.get() method to retrieve the value of a variable.

```py
database_host = Variable.get("database_host")
```

If the variable does not exist, the Variable.get() method will raise an exception. You can provide a default value as a second argument to the Variable.get() method to avoid this exception.

```py
database_host = Variable.get("database_host", default_value="localhost")
```

**Example DAG**

Here's an example of a DAG that retrieves an Airflow Variable and uses it in a BashOperator:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.models.variable import Variable
from datetime import datetime

with DAG(
    dag_id="variable_example",
    start_date=datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
    tags=["example"],
) as dag:
    # Retrieve the value of the 'greeting' variable. If it doesn't exist, default to "Hello"
    greeting = Variable.get("greeting", default_value="Hello")

    # Define a BashOperator that uses the retrieved variable in its bash_command
    print_greeting = BashOperator(
        task_id="print_greeting",
        bash_command=f"echo '{greeting}, Airflow!'",
    )
```

In this example, the DAG retrieves the value of the greeting variable. If the variable is not defined in the Airflow UI, the default_value of "Hello" will be used. The BashOperator then prints the greeting to the console.

**Using Variables with PythonOperator**

You can also use Airflow Variables with the PythonOperator. Here's an example:

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.models.variable import Variable
from datetime import datetime

def print_variable(variable_name):
    value = Variable.get(variable_name)
    print(f"The value of {variable_name} is: {value}")

with DAG(
    dag_id="python_variable_example",
    start_date=datetime(2023, 1, 1),
    schedule=None,
    catchup=False,
    tags=["example"],
) as dag:
    print_db_host = PythonOperator(
        task_id="print_db_host",
        python_callable=print_variable,
        op_kwargs={"variable_name": "database_host"},
    )
```

In this example, the print_variable function retrieves the value of the database_host variable and prints it to the console. The op_kwargs parameter of the PythonOperator is used to pass the variable name to the function.

#### <a name="chapter4part2.4"></a>Chapter 4 - Part 2.4: Best Practices for Using Variables

- **Use Descriptive Names**: Choose variable names that clearly indicate their purpose.
- **Provide Default Values**: Always provide default values to avoid errors if a variable is not defined.
- **Consider Connections for Sensitive Information**: While Variables can be used to store sensitive information, Airflow Connections are generally a better choice for storing credentials like passwords and API keys. Connections provide more secure storage and management options. We will cover Connections in the next lesson.
- **Document Your Variables**: Add descriptions to your variables in the Airflow UI to explain their purpose and usage.
- **Avoid Storing Large Amounts of Data**: Variables are stored in the Airflow metadata database, which is not designed for storing large amounts of data. If you need to store large amounts of data, consider using an external storage system like S3 or a database.

#### <a name="chapter4part3"></a>Chapter 4 - Part 3: Understanding Airflow Connections

Airflow Connections are crucial for interacting with external systems. They provide a secure and manageable way to store connection details like usernames, passwords, hosts, and ports, which are necessary to connect to databases, APIs, cloud services, and other platforms. Instead of hardcoding these sensitive details directly into your DAGs, you store them in Airflow's metadata database and reference them by a unique conn_id. This approach enhances security, simplifies configuration management, and promotes code reusability.

#### <a name="chapter4part3.1"></a>Chapter 4 - Part 3.1: Understanding Airflow Connections

An Airflow Connection represents a way to access an external system. It's essentially a named configuration that stores the necessary information to establish a connection. This information can include:

- **Connection ID (conn_id)**: A unique identifier for the connection. This is how you reference the connection in your DAGs.
- **Connection Type**: The type of system you're connecting to (e.g., HTTP, Postgres, MySQL, S3).
- **Host**: The hostname or IP address of the system.
- **Schema**: The database schema or path.
- **Login**: The username for authentication.
- **Password**: The password for authentication.
- **Port**: The port number to connect to.
- **Extra**: A JSON field for storing additional connection parameters specific to the connection type.

**Connection Types**

Airflow supports a wide variety of connection types out-of-the-box. Here are some of the most commonly used ones:

- **HTTP**: For connecting to HTTP endpoints and APIs.
- **Postgres**: For connecting to PostgreSQL databases.
- **MySQL**: For connecting to MySQL databases.
- **S3**: For connecting to Amazon S3.
- **Snowflake**: For connecting to Snowflake data warehouses.
- **BigQuery**: For connecting to Google BigQuery.
- **SSH**: For connecting to remote servers via SSH.
- **Generic**: A flexible connection type that can be used for various systems.

**Creating and Managing Connections**

You can create and manage Airflow Connections through the Airflow UI, the Airflow CLI, or programmatically using the Airflow API.

**Using the Airflow UI**

- Navigate to the Airflow UI.
- Go to Admin -> Connections.
- Click the Create button.
- Fill in the connection details, including the conn_id, connection type, and other relevant parameters.
- Click the Save button.

**Using the Airflow CLI**

You can use the Airflow CLI to create, update, and delete connections. Here are some examples:

```
# Create a new connection
airflow connections add my_postgres_conn \
    --conn-type postgres \
    --conn-host my_postgres_host \
    --conn-schema my_postgres_db \
    --conn-login my_postgres_user \
    --conn-password my_postgres_password \
    --conn-port 5432

# List existing connections
airflow connections list

# Delete a connection
airflow connections delete my_postgres_conn
```

**Programmatically**

You can also create and manage connections programmatically using the Airflow API. This is useful for automating connection management as part of your infrastructure provisioning process.

```py
from airflow.models.connection import Connection
from airflow.utils.db import create_session

conn = Connection(
    conn_id='my_postgres_conn',
    conn_type='postgres',
    host='my_postgres_host',
    schema='my_postgres_db',
    login='my_postgres_user',
    password='my_postgres_password',
    port=5432
)

with create_session() as session:
    session.add(conn)
```

**Accessing Connections in DAGs**

To access a connection in your DAG, you can use the BaseHook.get_connection() method. This method retrieves the connection object based on the conn_id.

```py
from airflow.hooks.base import BaseHook
from airflow.operators.python import PythonOperator
from airflow import DAG
from datetime import datetime

def my_task():
    conn = BaseHook.get_connection('my_postgres_conn')
    # Use the connection details to connect to the database
    print(f"Host: {conn.host}")
    print(f"User: {conn.login}")
    print(f"Password: {conn.password}")

with DAG(
    dag_id='connection_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    task = PythonOperator(
        task_id='my_task',
        python_callable=my_task
    )
```

**Example: Connecting to a REST API**

Let's say you want to connect to a REST API to retrieve some data. You can create an HTTP connection in Airflow and then use the HttpHook to interact with the API.

- **Create an HTTP connection**: In the Airflow UI, create a new connection with the following details:
  - Conn Id: my_api_conn
  - Conn Type: HTTP
  - Host: https://api.example.com
 
- **Use the HttpHook in your DAG**:

```py
from airflow.hooks.http import HttpHook
from airflow.operators.python import PythonOperator
from airflow import DAG
from datetime import datetime

def get_data_from_api():
    http_hook = HttpHook(http_conn_id='my_api_conn', method='GET')
    response = http_hook.run(endpoint='/data')
    print(response.json())

with DAG(
    dag_id='http_connection_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    get_data_task = PythonOperator(
        task_id='get_data',
        python_callable=get_data_from_api
    )
```

In this example, the HttpHook uses the connection details stored in the my_api_conn connection to make a GET request to the /data endpoint of the API.

**Example: Connecting to a Database**

Connecting to a database is a common use case for Airflow Connections. Let's look at an example of connecting to a PostgreSQL database.

- **Create a Postgres connection**: In the Airflow UI, create a new connection with the following details:
  - Conn Id: my_postgres_conn
  - Conn Type: Postgres
  - Host: my_postgres_host
  - Schema: my_postgres_db
  - Login: my_postgres_user
  - Password: my_postgres_password
  - Port: 5432

- **Use the PostgresHook in your DAG:**

```py
from airflow.providers.postgres.hooks.postgres import PostgresHook
from airflow.operators.python import PythonOperator
from airflow import DAG
from datetime import datetime

def execute_query():
    postgres_hook = PostgresHook(postgres_conn_id='my_postgres_conn')
    records = postgres_hook.get_records("SELECT * FROM my_table")
    print(records)

with DAG(
    dag_id='postgres_connection_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    execute_query_task = PythonOperator(
        task_id='execute_query',
        python_callable=execute_query
    )
```

In this example, the PostgresHook uses the connection details stored in the my_postgres_conn connection to execute a query against the PostgreSQL database.

**Hypothetical Scenario: Connecting to a Cloud Storage Service**

Imagine you're building a data pipeline that needs to read data from a cloud storage service like Azure Blob Storage. You can create an Azure Blob Storage connection in Airflow and then use the appropriate hook to interact with the storage service.

- **Create an Azure Blob Storage connection**: In the Airflow UI, create a new connection with the following details:
  - Conn Id: my_azure_blob_conn
  - Conn Type: wasb (This is the connection type for Azure Blob Storage)
  - Login: <your_account_name> (Azure Storage Account Name)
  - Password: <your_account_key> (Azure Storage Account Key)
  - Extra: {"container_name": "<your_container_name>"} (JSON with container name)
 
- **Use the WasbHook in your DAG**:

```py
from airflow.providers.microsoft.azure.hooks.wasb import WasbHook
from airflow.operators.python import PythonOperator
from airflow import DAG
from datetime import datetime

def list_blobs():
    wasb_hook = WasbHook(wasb_conn_id='my_azure_blob_conn')
    blobs = wasb_hook.list_blobs()
    print(blobs)

with DAG(
    dag_id='azure_blob_connection_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    list_blobs_task = PythonOperator(
        task_id='list_blobs',
        python_callable=list_blobs
    )
```

In this example, the WasbHook uses the connection details stored in the my_azure_blob_conn connection to list the blobs in the specified container.

#### <a name="chapter4part3.2"></a>Chapter 4 - Part 3.2: Best Practices for Using Connections

- **Use descriptive conn_ids**: Choose conn_ids that clearly indicate the purpose of the connection (e.g., production_db, staging_api).
- **Store sensitive information securely**: Use Airflow's built-in encryption features to protect sensitive information like passwords.
- **Avoid hardcoding connection details**: Never hardcode connection details directly into your DAGs. Always use Airflow Connections.
- **Use environment variables**: You can use environment variables to override connection details at runtime. This is useful for deploying your DAGs to different environments.
- **Regularly rotate credentials**: Regularly rotate your passwords and API keys to minimize the risk of security breaches.
- **Limit access to connections**: Restrict access to connections based on the principle of least privilege. Only grant users the permissions they need to access the connections they require.

#### <a name="chapter4part4"></a>Chapter 4 - Part 4: Configuring Connections for Databases, APIs, and Cloud Services

Airflow connections are crucial for interacting with external systems like databases, APIs, and cloud services. They provide a secure and manageable way to store connection details, preventing sensitive information from being hardcoded in your DAGs. This lesson will cover how to configure and use Airflow connections for various services, ensuring your workflows can seamlessly integrate with your data infrastructure.

#### <a name="chapter4part4.1"></a>Chapter 4 - Part 4.1: Understanding Airflow Connections

Airflow Connections are objects that store the information needed to connect to external systems. This information includes hostnames, ports, usernames, passwords, and other authentication details. By using connections, you can avoid hardcoding sensitive information directly into your DAGs, making your workflows more secure and easier to manage.

**Why Use Connections?**

- **Security**: Connections allow you to store sensitive information like passwords and API keys in a centralized and encrypted location (the Airflow metadata database).
- **Centralized Management**: You can manage all your connection details in one place, making it easier to update credentials or change connection parameters without modifying your DAGs.
- **Reusability**: Connections can be reused across multiple DAGs, reducing redundancy and ensuring consistency.
- **Abstraction**: Connections abstract away the underlying connection details, allowing you to focus on the logic of your DAGs rather than the specifics of how to connect to each service.

**Connection Types**

Airflow supports a wide range of connection types, each tailored to a specific service or protocol. Some of the most common connection types include:

- **Postgres**: For connecting to PostgreSQL databases.
- **MySQL**: For connecting to MySQL databases.
- **Amazon S3**: For connecting to Amazon S3 buckets.
- **HTTP**: For connecting to HTTP endpoints.
- **Snowflake**: For connecting to Snowflake data warehouses.
- **Google Cloud Platform (GCP)**: For connecting to various GCP services like BigQuery, Cloud Storage, and Dataproc.
- **SSH**: For connecting to remote servers via SSH.

You can find a complete list of supported connection types in the Airflow documentation.

#### <a name="chapter4part4.2"></a>Chapter 4 - Part 4.2: Configuring Connections

You can configure Airflow connections through the Airflow UI, the Airflow CLI, or programmatically using environment variables.

**Configuring Connections via the Airflow UI**

The Airflow UI provides a user-friendly interface for creating and managing connections.

- **Access the Airflow UI**: Open your web browser and navigate to the Airflow UI (usually at http://localhost:8080).

- **Navigate to the Connections Page**: Click on the "Admin" tab and then select "Connections".

- **Create a New Connection**: Click on the "+" button to create a new connection.

- **Fill in the Connection Details:**
  - **Conn Id**: A unique identifier for the connection (e.g., postgres_db, s3_bucket, api_endpoint).
  - **Conn Type**: Select the appropriate connection type from the dropdown menu (e.g., Postgres, S3, HTTP).
  - **Host**: The hostname or IP address of the service (e.g., localhost, s3.amazonaws.com, api.example.com).
  - **Schema**: The database schema or bucket name (e.g., public, my_bucket).
  - **Login**: The username for authentication (if required).
  - **Password**: The password for authentication (if required).
  - **Port**: The port number for the service (e.g., 5432, 80, 443).
  - **Extra**: A JSON dictionary containing additional configuration parameters specific to the connection type.

For example, to configure a connection to a PostgreSQL database, you might enter the following details:
- **Conn Id**: postgres_db
- **Conn Type**: Postgres
- **Host**: localhost
- **Schema**: public
- **Login**: airflow
- **Password**: airflow
- **Port**: 5432

- **Test the Connection**: Click on the "Test" button to verify that the connection is working correctly.

- **Save the Connection**: Click on the "Save" button to save the connection.

**Configuring Connections via the Airflow CLI**

The Airflow CLI provides a command-line interface for managing connections. You can use the airflow connections command to create, update, and delete connections.

To create a new connection, use the following command:

```
airflow connections add <conn_id> \
    --conn-type <conn_type> \
    --conn-host <conn_host> \
    --conn-schema <conn_schema> \
    --conn-login <conn_login> \
    --conn-password <conn_password> \
    --conn-port <conn_port> \
    --conn-extra <conn_extra>
```

For example, to create a PostgreSQL connection using the CLI, you would use the following command:

```
airflow connections add postgres_db \
    --conn-type postgres \
    --conn-host localhost \
    --conn-schema public \
    --conn-login airflow \
    --conn-password airflow \
    --conn-port 5432
```

To update an existing connection, use the same command with the --replace flag:

```
airflow connections add postgres_db \
    --conn-type postgres \
    --conn-host new_host \
    --conn-schema public \
    --conn-login airflow \
    --conn-password airflow \
    --conn-port 5432 \
    --replace
```

To delete a connection, use the following command:

```
airflow connections delete <conn_id>
```

For example, to delete the postgres_db connection, you would use the following command:

```
airflow connections delete postgres_db
```

**Configuring Connections via Environment Variables**

Airflow also allows you to configure connections using environment variables. This can be useful for automating the configuration of connections in a production environment.

To configure a connection using environment variables, you need to set an environment variable with the following format:

```
AIRFLOW_CONN_<CONN_ID>=<conn_uri>
```

Where <CONN_ID> is the connection ID in uppercase and with spaces replaced by underscores, and <conn_uri> is a URI that describes the connection.

The connection URI has the following format:

```
<conn_type>://<login>:<password>@<host>:<port>/<schema>?<extra>
```

For example, to configure a PostgreSQL connection using environment variables, you would set the following environment variable:

```
AIRFLOW_CONN_POSTGRES_DB=postgres://airflow:airflow@localhost:5432/public
```

You can set environment variables in your shell or in your Airflow configuration file.

#### <a name="chapter4part4.3"></a>Chapter 4 - Part 4.3: Using Connections in DAGs

Once you have configured a connection, you can use it in your DAGs to interact with the corresponding service. Most Airflow operators that interact with external systems accept a conn_id parameter, which specifies the connection to use.

Here's an example of using the PostgresOperator to execute a SQL query using a connection:

```py
from airflow import DAG
from airflow.providers.postgres.operators.postgres import PostgresOperator
from datetime import datetime

with DAG(
    dag_id='postgres_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    create_table = PostgresOperator(
        task_id='create_table',
        postgres_conn_id='postgres_db',  # Use the connection ID
        sql="""
            CREATE TABLE IF NOT EXISTS users (
                id SERIAL PRIMARY KEY,
                name VARCHAR(255) NOT NULL,
                email VARCHAR(255) UNIQUE NOT NULL
            );
        """
    )
```

In this example, the postgres_conn_id parameter is set to postgres_db, which tells the operator to use the connection with that ID to connect to the PostgreSQL database.

Here's another example using the S3Hook to interact with an S3 bucket:

```py
from airflow import DAG
from airflow.providers.amazon.aws.hooks.s3 import S3Hook
from airflow.operators.python import PythonOperator
from datetime import datetime

def upload_to_s3():
    s3_hook = S3Hook(aws_conn_id='s3_connection') # Use the connection ID
    s3_hook.load_string(
        string_data='Hello, S3!',
        key='hello.txt',
        bucket_name='my-s3-bucket',
        replace=True
    )

with DAG(
    dag_id='s3_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    upload_task = PythonOperator(
        task_id='upload_to_s3',
        python_callable=upload_to_s3
    )
```

In this example, the S3Hook is initialized with the aws_conn_id parameter set to s3_connection, which tells the hook to use the connection with that ID to connect to the S3 bucket.

#### <a name="chapter4part4.4"></a>Chapter 4 - Part 4.4: Connection Examples for Different Services

Here are some examples of how to configure connections for different services:

**PostgreSQL**
- **Conn Id**: postgres_db
- **Conn Type**: Postgres
- **Host**: localhost
- **Schema**: public
- **Login**: airflow
- **Password**: airflow
- **Port**: 5432

**Amazon S3**
- **Conn Id**: s3_connection
- **Conn Type**: S3
- **Login**: YOUR_AWS_ACCESS_KEY_ID
- **Password**: YOUR_AWS_SECRET_ACCESS_KEY
- **Extra**: {"region_name": "us-east-1"} (Optional, but recommended)

**HTTP**
- **Conn Id**: api_endpoint
- **Conn Type**: HTTP
- **Host**: api.example.com
- **Schema**: https (or http)
- **Login**: YOUR_API_USERNAME (Optional)
- **Password**: YOUR_API_PASSWORD (Optional)
- **Extra**: {"verify": "true"} (Optional, for SSL verification)

**Snowflake**
- **Conn Id**: snowflake_connection
- **Conn Type**: Snowflake
- **Login**: YOUR_SNOWFLAKE_USERNAME
- **Password**: YOUR_SNOWFLAKE_PASSWORD
- **Host**: YOUR_ACCOUNT.snowflakecomputing.com
- **Schema**: YOUR_DATABASE.YOUR_SCHEMA
- **Extra**: {"account": "YOUR_ACCOUNT", "warehouse": "YOUR_WAREHOUSE", "database": "YOUR_DATA"}

**Google Cloud Platform (GCP)**

For GCP connections, it's generally recommended to use a service account and store the credentials in a JSON file.

- **Conn Id**: google_cloud_default
- **Conn Type**: Google Cloud
- **Extra**: {"extra__google_cloud_platform__key_path": "/path/to/your/service_account.json"}

#### <a name="chapter4part5"></a>Chapter 4 - Part 5: Using Variables and Connections for Secure Configuration Management

Airflow Variables and Connections are crucial for managing configurations securely and efficiently within your workflows. Instead of hardcoding sensitive information like passwords, API keys, or database connection strings directly into your DAGs, you can store them securely in Airflow's metadata database and access them dynamically. This approach enhances security, simplifies maintenance, and promotes reusability across multiple DAGs. This lesson will delve into how to effectively use Variables and Connections for secure configuration management.

#### <a name="chapter4part5.1"></a>Chapter 4 - Part 5.1: Understanding the Need for Secure Configuration Management

Hardcoding sensitive information directly into your DAGs poses several risks:

- **Security Vulnerabilities**: Exposing credentials in your code can lead to unauthorized access to your systems and data.
- **Maintenance Challenges**: Updating credentials requires modifying and redeploying your DAGs, which can be time-consuming and error-prone.
- **Lack of Reusability**: Hardcoded values limit the reusability of your DAGs across different environments or projects.

Airflow Variables and Connections provide a centralized and secure way to manage configurations, addressing these challenges.

#### <a name="chapter4part5.2"></a>Chapter 4 - Part 5.2: Airflow Variables: Dynamic Configuration Options

Airflow Variables are key-value pairs stored in the Airflow metadata database. They allow you to externalize configuration settings from your DAGs, making them more flexible and maintainable.

**Setting and Retrieving Variables**

You can set and retrieve Variables through the Airflow UI, the Airflow CLI, or programmatically within your DAGs.

**Using the Airflow UI:**

- Navigate to the "Admin" tab and select "Variables".
- Click "Create" to add a new variable.
- Enter a key (name) and a value for the variable.
- Optionally, provide a description for the variable.
- Click "Save".

**Using the Airflow CLI:**

```
# Set a variable
airflow variables set my_variable "my_value"

# Get a variable
airflow variables get my_variable
```

**Programmatically in a DAG:**

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.models import Variable
from datetime import datetime

def print_variable():
    my_variable = Variable.get("my_variable")
    print(f"The value of my_variable is: {my_variable}")

with DAG(
    dag_id="variable_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
) as dag:
    print_variable_task = PythonOperator(
        task_id="print_variable",
        python_callable=print_variable,
    )
```

In this example, the Variable.get() method retrieves the value of the "my_variable" variable.

**Variable Data Types and Serialization**

Airflow Variables store values as strings. If you need to store more complex data types like lists or dictionaries, you can serialize them using JSON.

**Example:**

```py
import json
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.models import Variable
from datetime import datetime

def print_json_variable():
    json_variable = Variable.get("my_json_variable", deserialize_json=True)
    print(f"The value of my_json_variable is: {json_variable}")
    print(f"The type of my_json_variable is: {type(json_variable)}")

with DAG(
    dag_id="json_variable_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
) as dag:
    print_json_variable_task = PythonOperator(
        task_id="print_json_variable",
        python_callable=print_json_variable,
    )
```

In the Airflow UI or CLI, you would set the "my_json_variable" to a JSON string like {"key1": "value1", "key2": 123}. The deserialize_json=True argument in Variable.get() automatically converts the JSON string to a Python dictionary.

**Variable Scope and Best Practices**

- **Naming Conventions**: Use descriptive and consistent naming conventions for your variables. For example, s3_bucket_name, api_endpoint, or database_connection_string.
- **Descriptions**: Provide clear descriptions for each variable to explain its purpose and usage.
- **Avoid Storing Large Data**: Variables are stored in the metadata database, so avoid storing large amounts of data in them. For large datasets, consider using external storage solutions like S3 or databases.
- **Environment-Specific Variables**: Use variables to manage environment-specific configurations. For example, you can have different variables for development, staging, and production environments.

#### <a name="chapter4part5.3"></a>Chapter 4 - Part 5.3: Airflow Connections: Securely Storing Credentials

Airflow Connections provide a secure way to store connection information for external systems like databases, APIs, and cloud services. Connections store sensitive information like usernames, passwords, and hostnames in an encrypted format within the Airflow metadata database.

**Configuring Connections**

You can configure Connections through the Airflow UI or programmatically using the Airflow CLI or the Airflow API.

**Using the Airflow UI:**

- Navigate to the "Admin" tab and select "Connections".
- Click "Create" to add a new connection.
- Enter a connection ID (name) for the connection.
- Select the connection type (e.g., Postgres, S3, HTTP).
- Fill in the required connection parameters, such as Host, Schema, Login, Password, Port.
- Optionally, provide a description for the connection.
- Click "Save".

**Using the Airflow CLI:**

```
# Create a Postgres connection
airflow connections add postgres_conn \
    --conn-type postgres \
    --conn-host localhost \
    --conn-schema my_database \
    --conn-login my_user \
    --conn-password my_password \
    --conn-port 5432
```

**Using Connections in DAGs**

You can access Connections within your DAGs using the BaseHook.get_connection() method. This method retrieves the connection object, which contains the connection parameters.

**Example:**

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.hooks.base import BaseHook
from datetime import datetime

def print_connection_details():
    conn = BaseHook.get_connection("postgres_conn")
    print(f"Connection Host: {conn.host}")
    print(f"Connection Schema: {conn.schema}")
    print(f"Connection Login: {conn.login}")
    print(f"Connection Password: {conn.password}")
    print(f"Connection Port: {conn.port}")

with DAG(
    dag_id="connection_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
) as dag:
    print_connection_task = PythonOperator(
        task_id="print_connection",
        python_callable=print_connection_details,
    )
```

In this example, the BaseHook.get_connection() method retrieves the connection object for the "postgres_conn" connection. The connection object's attributes (e.g., conn.host, conn.login) provide access to the connection parameters.

**Connection Types**

Airflow supports various connection types for different systems and services. Some common connection types include:

- **Postgres**: For connecting to PostgreSQL databases.
- **MySQL**: For connecting to MySQL databases.
- **S3**: For connecting to Amazon S3.
- **HTTP**: For making HTTP requests.
- **Snowflake**: For connecting to Snowflake data warehouses.
- **Google Cloud**: For connecting to Google Cloud services like BigQuery and Cloud Storage.

Each connection type has its own set of required and optional parameters. Refer to the Airflow documentation for a complete list of connection types and their parameters.

**Connection Scope and Best Practices**

- **Centralized Management**: Use Connections to manage all your external system credentials in a central location.
- **Least Privilege**: Grant each connection only the necessary permissions to access the required resources.
- **Regular Rotation**: Rotate your credentials regularly to minimize the risk of unauthorized access.
- **Environment-Specific Connections**: Use different connections for different environments (e.g., development, staging, production).
- **Avoid Sharing Connections**: Avoid sharing connections between different DAGs or tasks unless absolutely necessary.

#### <a name="chapter4part5.4"></a>Chapter 4 - Part 5.4: Using Variables and Connections Together

Variables and Connections can be used together to create flexible and secure configurations. For example, you can store the database name in a Variable and use it in conjunction with a Connection to connect to a specific database.

**Example:**

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.hooks.base import BaseHook
from airflow.models import Variable
from datetime import datetime
import psycopg2  # Assuming you are using psycopg2 for PostgreSQL

def connect_to_database():
    conn_id = "postgres_conn"
    database_name = Variable.get("database_name")

    try:
        conn = BaseHook.get_connection(conn_id)
        # Construct the connection string using information from both the Connection and Variable
        connection_string = f"host={conn.host} dbname={database_name} user={conn.login} password={conn.password} port={conn.port}"

        # Establish the connection
        pg_conn = psycopg2.connect(connection_string)
        print("Successfully connected to the database!")
        pg_conn.close()

    except Exception as e:
        print(f"Error connecting to the database: {e}")

with DAG(
    dag_id="variable_connection_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
) as dag:
    connect_task = PythonOperator(
        task_id="connect_to_db",
        python_callable=connect_to_database,
    )
```

In this example, the database_name is retrieved from a Variable, while the other connection parameters (host, login, password, port) are retrieved from the "postgres_conn" Connection. This approach allows you to easily switch between different databases by simply updating the "database_name" variable.

## <a name="chapter5"></a>Chapter 5: Advanced DAG Concepts

#### <a name="chapter5part1"></a>Chapter 5 - Part 1: SubDAGs and TaskGroups for Modular DAG Design

In complex data pipelines, DAGs can become unwieldy and difficult to manage. This lesson introduces two powerful techniques for structuring and organizing your Airflow DAGs: SubDAGs and TaskGroups. By using these features, you can create more modular, readable, and maintainable workflows. We'll explore the concepts behind each approach, their advantages and disadvantages, and how to implement them effectively.

#### <a name="chapter5part1.1"></a>Chapter 5 - Part 1.1: Understanding SubDAGs

A SubDAG is essentially a DAG embedded within another DAG. It allows you to encapsulate a reusable sequence of tasks into a self-contained unit. Think of it as a function in programming, but for DAGs.

**Core Concepts of SubDAGs**

- **Encapsulation**: SubDAGs hide the complexity of a group of tasks, making the main DAG easier to understand.
- **Reusability**: A SubDAG can be reused in multiple DAGs, promoting code reuse and reducing redundancy.
- **Modularity**: SubDAGs break down a large DAG into smaller, more manageable components.
- **Independent Execution**: A SubDAG runs as a separate DAG instance within Airflow.

**Implementing SubDAGs**

To create a SubDAG, you define a function that returns a DAG object. This DAG represents the SubDAG. You then use the SubDagOperator in your main DAG to include the SubDAG.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.operators.subdag import SubDagOperator
from datetime import datetime

def subdag(parent_dag_name, child_dag_name, args):
    """
    Creates a subdag.

    :param parent_dag_name: The dag name of parent DAG.
    :param child_dag_name: The dag name of child DAG.
    :param args: The arguments of parent DAG.
    :return: DAG object
    """
    dag_subdag = DAG(
        dag_id=f"{parent_dag_name}.{child_dag_name}",
        default_args=args,
        schedule=None,
    )

    with dag_subdag:
        task_1 = BashOperator(
            task_id="subdag_task_1",
            bash_command="echo 'This is subdag task 1'"
        )

        task_2 = BashOperator(
            task_id="subdag_task_2",
            bash_command="echo 'This is subdag task 2'"
        )

        task_1 >> task_2

    return dag_subdag


with DAG(
    dag_id="parent_dag",
    start_date=datetime(2023, 1, 1),
    schedule=None,
    catchup=False
) as dag:
    start = BashOperator(
        task_id="start",
        bash_command="echo 'Start of parent DAG'"
    )

    sub_dag_task = SubDagOperator(
        task_id="subdag_operator",
        subdag=subdag(
            parent_dag_name="parent_dag",
            child_dag_name="subdag_operator",
            args=dag.default_args
        ),
    )

    end = BashOperator(
        task_id="end",
        bash_command="echo 'End of parent DAG'"
    )

    start >> sub_dag_task >> end
```

In this example:

- subdag is a function that defines the SubDAG. It creates a DAG object with its own tasks (subdag_task_1 and subdag_task_2). The dag_id is crucial; it must be unique and is typically constructed by combining the parent DAG's name and the SubDAG's name.
- SubDagOperator is used in the main DAG (parent_dag) to include the SubDAG. The subdag argument is passed the result of the subdag function, effectively embedding the SubDAG into the parent.
- The schedule argument is set to None because the SubDAG inherits the schedule of the parent DAG.
- The default_args are passed from the parent DAG to the SubDAG to ensure consistency in settings like start_date and retries.

**Advantages of SubDAGs**

- **Code Reusability**: SubDAGs allow you to reuse common task sequences across multiple DAGs.
- **Improved DAG Organization**: They break down complex DAGs into smaller, more manageable units.
- **Simplified DAG Visualization**: The main DAG becomes cleaner and easier to understand.

**Disadvantages of SubDAGs**

- **Increased Complexity**: SubDAGs can add complexity to your Airflow setup, especially when debugging.
- **Performance Overhead**: Each SubDAG runs as a separate DAG instance, which can introduce performance overhead.
- **Limited Flexibility**: SubDAGs can be less flexible than other modularization techniques.
- **Potential for Deadlocks**: If not carefully designed, SubDAGs can lead to deadlocks or other unexpected behavior.

**Best Practices for Using SubDAGs**

- **Keep SubDAGs Small and Focused**: Each SubDAG should perform a specific, well-defined task.
- **Avoid Deeply Nested SubDAGs**: Deeply nested SubDAGs can be difficult to manage and debug.
- **Use Clear and Consistent Naming Conventions**: Use consistent naming conventions for SubDAGs and their tasks.
- **Document Your SubDAGs Thoroughly**: Document the purpose, inputs, and outputs of each SubDAG.
- **Consider Alternatives**: Before using SubDAGs, consider whether TaskGroups or other modularization techniques might be a better fit.

#### <a name="chapter5part1.2"></a>Chapter 5 - Part 1.2: Understanding TaskGroups

TaskGroups provide a way to group related tasks within a DAG, improving organization and readability. Unlike SubDAGs, TaskGroups do not run as separate DAG instances. They are purely a visual and organizational construct within a single DAG.

**Core Concepts of TaskGroups**

- **Grouping**: TaskGroups group related tasks together, making the DAG easier to understand.
- **Visual Organization**: They provide a visual representation of task relationships in the Airflow UI.
- **No Separate Execution**: TaskGroups do not run as separate DAG instances, reducing overhead.
- **Simplified Management**: They simplify the management of related tasks, such as setting dependencies and retries.

**Implementing TaskGroups**

TaskGroups can be implemented using the TaskGroup class. You define a TaskGroup and then add tasks to it.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.utils.task_group import TaskGroup
from datetime import datetime

with DAG(
    dag_id="taskgroup_example",
    start_date=datetime(2023, 1, 1),
    schedule=None,
    catchup=False
) as dag:
    start = BashOperator(
        task_id="start",
        bash_command="echo 'Start of DAG'"
    )

    with TaskGroup("processing_tasks") as processing_tasks:
        task_1 = BashOperator(
            task_id="task_1",
            bash_command="echo 'Processing task 1'"
        )

        task_2 = BashOperator(
            task_id="task_2",
            bash_command="echo 'Processing task 2'"
        )

        task_1 >> task_2

    end = BashOperator(
        task_id="end",
        bash_command="echo 'End of DAG'"
    )

    start >> processing_tasks >> end
```

In this example:

TaskGroup("processing_tasks") creates a TaskGroup named "processing_tasks".
task_1 and task_2 are added to the processing_tasks TaskGroup.
The >> operator is used to define dependencies between tasks within the TaskGroup.
The processing_tasks TaskGroup is treated as a single unit in the main DAG, simplifying the overall DAG structure.

**Advantages of TaskGroups**
- **Improved DAG Readability: TaskGroups make DAGs easier to understand by grouping related tasks.
- **Simplified DAG Visualization: They provide a visual representation of task relationships in the Airflow UI.
- **Reduced Overhead: TaskGroups do not run as separate DAG instances, reducing overhead compared to SubDAGs.
- **Easier Management: They simplify the management of related tasks, such as setting dependencies and retries.

**Disadvantages of TaskGroups**
- **Limited Reusability**: TaskGroups are not as reusable as SubDAGs.
- **No Separate Execution**: TaskGroups do not run as separate DAG instances, which can limit their flexibility in some cases.

- **Best Practices for Using TaskGroups**
- **Group Related Tasks**: Each TaskGroup should contain tasks that are logically related.
- **Use Descriptive Names**: Use descriptive names for TaskGroups to make the DAG easier to understand.
- **Keep TaskGroups Small and Focused**: Each TaskGroup should perform a specific, well-defined task.
- **Avoid Overlapping TaskGroups**: Avoid creating TaskGroups that overlap or contain tasks that belong in other TaskGroups.
- **Use TaskGroups Consistently**: Use TaskGroups consistently throughout your DAGs to maintain a consistent style.

#### <a name="chapter5part1.3"></a>Chapter 5 - Part 1.3: SubDAGs vs. TaskGroups: A Comparison

|Feature	|SubDAGs	|TaskGroups|
| :--: | :--: | :--: |
|Execution	|Runs as a separate DAG instance	|Runs within the same DAG instance|
|Reusability	|Highly reusable	|Limited reusability|
|Overhead	|Higher overhead due to separate execution	|Lower overhead|
|Complexity	|More complex to manage and debug	|Simpler to manage and debug|
|Visualization	|Shows a separate DAG in the UI	|Shows a group of tasks within the same DAG|
|Use Cases	|Reusable task sequences, independent workflows	|Grouping related tasks, improving readability|

**When to Use SubDAGs**
- When you have a reusable sequence of tasks that needs to be executed independently.
- When you want to break down a large DAG into smaller, more manageable units.
- When you need to encapsulate a complex workflow into a self-contained unit.

**When to Use TaskGroups**
- When you want to group related tasks together to improve DAG readability.
- When you want to simplify the management of related tasks, such as setting dependencies and retries.
- When you don't need the overhead of running a separate DAG instance.

#### <a name="chapter5part1.4"></a>Chapter 5 - Part 1.4: Practical Examples and Demonstrations

Let's consider a data pipeline that processes customer data. The pipeline consists of the following steps:

- **Extract**: Extract data from various sources (e.g., databases, APIs, files).
- **Transform**: Transform the data into a consistent format.
- **Load**: Load the transformed data into a data warehouse.

**Using TaskGroups**

We can use TaskGroups to group the tasks within each step:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.utils.task_group import TaskGroup
from datetime import datetime

with DAG(
    dag_id="customer_data_pipeline_taskgroup",
    start_date=datetime(2023, 1, 1),
    schedule=None,
    catchup=False
) as dag:
    with TaskGroup("extract_tasks") as extract_tasks:
        extract_from_db = BashOperator(
            task_id="extract_from_db",
            bash_command="echo 'Extracting data from database'"
        )

        extract_from_api = BashOperator(
            task_id="extract_from_api",
            bash_command="echo 'Extracting data from API'"
        )

        extract_from_file = BashOperator(
            task_id="extract_from_file",
            bash_command="echo 'Extracting data from file'"
        )

    with TaskGroup("transform_tasks") as transform_tasks:
        transform_data = BashOperator(
            task_id="transform_data",
            bash_command="echo 'Transforming data'"
        )

    with TaskGroup("load_tasks") as load_tasks:
        load_to_warehouse = BashOperator(
            task_id="load_to_warehouse",
            bash_command="echo 'Loading data to data warehouse'"
        )

    extract_tasks >> transform_tasks >> load_tasks
```

In this example, we use TaskGroups to group the tasks within each step of the data pipeline. This makes the DAG easier to understand and manage.

**Using SubDAGs**

Now, let's assume that the "transform" step is a complex workflow that can be reused in other DAGs. In this case, we can use a SubDAG:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.operators.subdag import SubDagOperator
from airflow.utils.task_group import TaskGroup
from datetime import datetime

def transform_subdag(parent_dag_name, child_dag_name, args):
    """
    Creates a subdag for the transform tasks.

    :param parent_dag_name: The dag name of parent DAG.
    :param child_dag_name: The dag name of child DAG.
    :param args: The arguments of parent DAG.
    :return: DAG object
    """
    dag_subdag = DAG(
        dag_id=f"{parent_dag_name}.{child_dag_name}",
        default_args=args,
        schedule=None,
    )

    with dag_subdag:
        transform_data_1 = BashOperator(
            task_id="transform_data_1",
            bash_command="echo 'Transforming data step 1'"
        )

        transform_data_2 = BashOperator(
            task_id="transform_data_2",
            bash_command="echo 'Transforming data step 2'"
        )

        transform_data_1 >> transform_data_2

    return dag_subdag


with DAG(
    dag_id="customer_data_pipeline_subdag",
    start_date=datetime(2023, 1, 1),
    schedule=None,
    catchup=False
) as dag:
    with TaskGroup("extract_tasks") as extract_tasks:
        extract_from_db = BashOperator(
            task_id="extract_from_db",
            bash_command="echo 'Extracting data from database'"
        )

        extract_from_api = BashOperator(
            task_id="extract_from_api",
            bash_command="echo 'Extracting data from API'"
        )

        extract_from_file = BashOperator(
            task_id="extract_from_file",
            bash_command="echo 'Extracting data from file'"
        )

    transform_subdag_task = SubDagOperator(
        task_id="transform_subdag",
        subdag=transform_subdag(
            parent_dag_name="customer_data_pipeline_subdag",
            child_dag_name="transform_subdag",
            args=dag.default_args
        ),
    )

    with TaskGroup("load_tasks") as load_tasks:
        load_to_warehouse = BashOperator(
            task_id="load_to_warehouse",
            bash_command="echo 'Loading data to data warehouse'"
        )

    extract_tasks >> transform_subdag_task >> load_tasks
```

In this example, we use a SubDAG to encapsulate the "transform" step. This allows us to reuse the "transform" workflow in other DAGs. We also use TaskGroups to group the tasks within the "extract" and "load" steps.

#### <a name="chapter5part2"></a>Chapter 5 - Part 2: Using BranchPythonOperator for Conditional Logic

The BranchPythonOperator in Apache Airflow is a powerful tool that allows you to introduce conditional logic into your DAGs. Instead of executing tasks in a linear fashion, you can use this operator to dynamically determine which branch of your workflow should be executed based on the outcome of a Python callable. This enables you to create more flexible and intelligent data pipelines that can adapt to different scenarios and data conditions.

#### <a name="chapter5part2.1"></a>Chapter 5 - Part 2.1: Understanding the BranchPythonOperator

The BranchPythonOperator is a specific type of operator in Airflow that executes a Python function (a callable) and uses its return value to determine which downstream task(s) to execute. The callable must return the task_id (or a list of task_ids) of the task(s) you want to run next. This allows you to create branches in your DAG, where different paths are taken based on the result of the Python function.

**Key Concepts**

- **Callable**: The Python function that the BranchPythonOperator executes. This function contains the logic that determines which branch to take.
- **Task ID(s)**: The task_id (or list of task_ids) returned by the callable. Airflow uses this to determine which downstream task(s) to execute.
- **Branching Logic**: The conditional statements within the callable that determine the return value based on specific criteria.
- **Downstream Tasks**: The tasks that are executed after the BranchPythonOperator, based on the branch that was chosen.

**How it Works**

- The BranchPythonOperator executes the provided Python callable.
- The callable performs its logic and returns the task_id (or a list of task_ids) of the task(s) to be executed next.
- Airflow uses the returned task_id(s) to determine which downstream task(s) to run. Only the task(s) specified by the returned task_id(s) will be executed. Other downstream tasks connected to the BranchPythonOperator will be skipped.

**Example 1: Data Quality Check**

Imagine you have a DAG that processes data from an external source. Before processing the data, you want to perform a data quality check to ensure that the data meets certain criteria. If the data quality check fails, you want to send an alert and stop the DAG. If the data quality check passes, you want to proceed with the data processing steps.

```py
from airflow import DAG
from airflow.operators.python import BranchPythonOperator, PythonOperator
from airflow.operators.bash import BashOperator
from datetime import datetime

def check_data_quality():
    """
    This function simulates a data quality check.
    In a real-world scenario, this would involve checking
    for missing values, data type correctness, etc.
    """
    # Simulate a data quality check that sometimes fails
    import random
    if random.random() > 0.5:
        return 'process_data'  # Data quality check passed
    else:
        return 'send_alert'  # Data quality check failed

def send_data_quality_alert():
    """
    This function simulates sending an alert.
    In a real-world scenario, this could involve sending an email
    or posting a message to a Slack channel.
    """
    print("Data quality check failed! Sending alert...")
    return 'Alert sent'

with DAG(
    dag_id='data_quality_check_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example'],
) as dag:
    data_quality_check = BranchPythonOperator(
        task_id='data_quality_check',
        python_callable=check_data_quality,
    )

    process_data = BashOperator(
        task_id='process_data',
        bash_command='echo "Processing data..."',
    )

    send_alert = PythonOperator(
        task_id='send_alert',
        python_callable=send_data_quality_alert,
    )

    data_quality_check >> [process_data, send_alert]
```

In this example:

- check_data_quality is the callable that performs the data quality check. It randomly returns either process_data or send_alert based on a random number.
- process_data is a BashOperator that simulates data processing.
- send_alert is a PythonOperator that simulates sending an alert.
- The data_quality_check task uses the BranchPythonOperator to execute the check_data_quality callable.
- Based on the return value of check_data_quality, either process_data or send_alert will be executed.

**Example 2: A/B Testing**

Let's say you're running an A/B test on a website. You have two versions of a landing page (A and B), and you want to track which version performs better. You can use the BranchPythonOperator to route users to either version A or version B based on a random assignment.

```py
from airflow import DAG
from airflow.operators.python import BranchPythonOperator, PythonOperator
from airflow.operators.bash import BashOperator
from datetime import datetime
import random

def choose_landing_page():
    """
    This function randomly chooses between landing page A and landing page B.
    """
    if random.random() > 0.5:
        return 'landing_page_a'
    else:
        return 'landing_page_b'

def track_landing_page_a():
    """
    This function simulates tracking user interactions on landing page A.
    """
    print("Tracking user interactions on landing page A...")
    return 'Tracked A'

def track_landing_page_b():
    """
    This function simulates tracking user interactions on landing page B.
    """
    print("Tracking user interactions on landing page B...")
    return 'Tracked B'

with DAG(
    dag_id='ab_testing_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example'],
) as dag:
    choose_page = BranchPythonOperator(
        task_id='choose_landing_page',
        python_callable=choose_landing_page,
    )

    landing_page_a = PythonOperator(
        task_id='landing_page_a',
        python_callable=track_landing_page_a,
    )

    landing_page_b = PythonOperator(
        task_id='landing_page_b',
        python_callable=track_landing_page_b,
    )

    choose_page >> [landing_page_a, landing_page_b]
```

In this example:

- choose_landing_page is the callable that randomly selects either landing_page_a or landing_page_b.
- landing_page_a and landing_page_b are PythonOperator tasks that simulate tracking user interactions on each landing page.
- The choose_page task uses the BranchPythonOperator to execute the choose_landing_page callable.
- Based on the return value of choose_landing_page, either landing_page_a or landing_page_b will be executed.

**Example 3: Handling File Types**

Suppose you have a DAG that processes files of different types (e.g., CSV, JSON, Parquet). You can use the BranchPythonOperator to determine the file type and route the file to the appropriate processing task.

```py
from airflow import DAG
from airflow.operators.python import BranchPythonOperator, PythonOperator
from airflow.operators.bash import BashOperator
from datetime import datetime

def determine_file_type():
    """
    This function determines the file type based on the file extension.
    In a real-world scenario, this could involve reading the file header
    or using a library like `filetype` to determine the file type.
    """
    file_name = 'data.csv' # Replace with a dynamic way to get the filename
    if file_name.endswith('.csv'):
        return 'process_csv_file'
    elif file_name.endswith('.json'):
        return 'process_json_file'
    else:
        return 'unsupported_file_type'

def process_csv_file():
    """
    This function simulates processing a CSV file.
    """
    print("Processing CSV file...")
    return 'CSV Processed'

def process_json_file():
    """
    This function simulates processing a JSON file.
    """
    print("Processing JSON file...")
    return 'JSON Processed'

def unsupported_file_type():
    """
    This function handles unsupported file types.
    """
    print("Unsupported file type!")
    return 'Unsupported'

with DAG(
    dag_id='file_type_processing_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    tags=['example'],
) as dag:
    determine_type = BranchPythonOperator(
        task_id='determine_file_type',
        python_callable=determine_file_type,
    )

    process_csv = PythonOperator(
        task_id='process_csv_file',
        python_callable=process_csv_file,
    )

    process_json = PythonOperator(
        task_id='process_json_file',
        python_callable=process_json_file,
    )

    unsupported = PythonOperator(
        task_id='unsupported_file_type',
        python_callable=unsupported_file_type,
    )

    determine_type >> [process_csv, process_json, unsupported]
```

In this example:

- determine_file_type is the callable that determines the file type based on the file extension.
- process_csv_file, process_json_file, and unsupported_file_type are PythonOperator tasks that handle different file types.
- The determine_type task uses the BranchPythonOperator to execute the determine_file_type callable.
- Based on the return value of determine_file_type, the appropriate processing task will be executed.

**Hypothetical Scenario: Fraud Detection**

Imagine you're building a fraud detection system. You can use the BranchPythonOperator to route transactions to different fraud detection models based on the transaction amount. For example, transactions above a certain threshold might be routed to a more sophisticated (and computationally expensive) fraud detection model, while transactions below the threshold are routed to a simpler model.

**Best Practices**

- **Keep the branching logic simple**: The callable in the BranchPythonOperator should be as simple and efficient as possible. Avoid complex computations or I/O operations within the callable. If necessary, delegate complex logic to separate tasks.
- **Handle all possible outcomes**: Ensure that your branching logic covers all possible outcomes and that there is a default branch to handle unexpected situations.
- **Use descriptive task IDs**: Use clear and descriptive task IDs for your downstream tasks to make it easy to understand the branching logic.
- **Document your DAG**: Clearly document the branching logic in your DAG to make it easier for others to understand and maintain.
- **Test your DAG**: Thoroughly test your DAG to ensure that the branching logic works as expected.

#### <a name="chapter5part3"></a>Chapter 5 - Part 3: Dynamic DAG Generation with Python

Dynamic DAG Generation with Python is a powerful technique that allows you to create DAGs programmatically, adapting to changing requirements and data structures. Instead of defining a static DAG in a Python file, you can write code that generates the DAG definition based on external factors like database contents, API responses, or configuration files. This approach is particularly useful when dealing with a large number of similar tasks or when the workflow needs to be highly flexible.

#### <a name="chapter5part3.1"></a>Chapter 5 - Part 3.1: Understanding Dynamic DAG Generation

Dynamic DAG generation involves using Python code to define the structure of your Airflow DAG. This means that the tasks, dependencies, and even the schedule of your DAG can be determined at runtime. This is in contrast to static DAG definitions, where the DAG structure is fixed in the Python file.

**Key Concepts**

- **DAG Factory**: A function or class that generates a DAG object. This factory can take parameters that influence the DAG's structure.
- **Runtime Parameters**: External data or configurations that are used to customize the DAG generation process. These parameters can come from various sources, such as databases, APIs, or configuration files.
- **Templating**: Using templating engines like Jinja2 to dynamically generate task configurations or even entire DAG definitions.
- **Code Reusability**: Dynamic DAG generation promotes code reusability by allowing you to define common task patterns and apply them to different datasets or environments.

**Benefits of Dynamic DAG Generation**

- **Flexibility**: Adapt to changing requirements without modifying the DAG code directly.
- **Scalability**: Easily manage a large number of similar tasks or workflows.
- **Maintainability**: Reduce code duplication and improve code organization.
- **Automation**: Automate the creation of DAGs based on external events or data changes.

#### <a name="chapter5part3.2"></a>Chapter 5 - Part 3.2: Implementing Dynamic DAG Generation

There are several ways to implement dynamic DAG generation in Airflow. Here, we'll explore a few common approaches.

**Using a Loop to Create Tasks**

The simplest form of dynamic DAG generation involves using a loop to create multiple tasks within a DAG. This is useful when you have a set of similar tasks that need to be executed in parallel or sequentially.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='dynamic_dag_loop',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    # Define a list of tasks to create
    task_list = ['task_1', 'task_2', 'task_3']

    # Loop through the task list and create a BashOperator for each task
    for task_id in task_list:
        bash_task = BashOperator(
            task_id=task_id,
            bash_command=f'echo "Running {task_id}"'
        )
```

In this example, we define a list of task IDs and then loop through the list to create a BashOperator for each task. The bash_command is dynamically generated based on the task ID.

**Generating DAGs from a Configuration File**

A more advanced approach involves reading a configuration file (e.g., JSON or YAML) and using the configuration data to generate the DAG. This allows you to define the DAG structure and task parameters in a separate file, making it easier to manage and update the DAG.

```py
import json
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

# Load the DAG configuration from a JSON file
with open('dag_config.json', 'r') as f:
    dag_config = json.load(f)

# Define the DAG
with DAG(
    dag_id=dag_config['dag_id'],
    start_date=datetime(2023, 1, 1),
    schedule_interval=dag_config['schedule_interval'],
    catchup=False
) as dag:
    # Loop through the tasks defined in the configuration
    for task_config in dag_config['tasks']:
        bash_task = BashOperator(
            task_id=task_config['task_id'],
            bash_command=task_config['bash_command']
        )
```

Here's an example of the dag_config.json file:

```json
{
    "dag_id": "dynamic_dag_config",
    "schedule_interval": "@daily",
    "tasks": [
        {
            "task_id": "task_a",
            "bash_command": "echo 'Running task A'"
        },
        {
            "task_id": "task_b",
            "bash_command": "echo 'Running task B'"
        }
    ]
}
```

This approach allows you to modify the DAG structure and task parameters by simply updating the configuration file, without having to modify the DAG code itself.

**Using a Database to Define DAG Structure**

Another powerful technique is to use a database to store the DAG structure and task parameters. This allows you to dynamically generate DAGs based on the data in the database.

```py
import os
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.providers.postgres.hooks.postgres import PostgresHook
from datetime import datetime

def get_tasks_from_db():
    """
    Retrieves task definitions from a PostgreSQL database.
    """
    pg_hook = PostgresHook(postgres_conn_id='postgres_default') # Ensure you have a connection named 'postgres_default'
    sql_query = "SELECT task_id, command FROM tasks_table;" # Replace with your actual table name and schema
    records = pg_hook.get_records(sql_query)
    return records

def create_task(task_id, command):
    """
    Creates a PythonOperator task.
    """
    def execute_command():
        os.system(command) # Executes the command using the system shell
    return PythonOperator(
        task_id=task_id,
        python_callable=execute_command,
        dag=dag, # 'dag' must be defined in the outer scope
    )

with DAG(
    dag_id='dynamic_dag_from_db',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    tasks = get_tasks_from_db()
    for task_id, command in tasks:
        task = create_task(task_id, command)
```

In this example, the get_tasks_from_db function retrieves task definitions from a PostgreSQL database. The create_task function then creates a PythonOperator for each task, using the task ID and command from the database. You'll need to configure a connection named postgres_default in Airflow that points to your PostgreSQL database. Also, you'll need to create a table named tasks_table (or whatever you name it in the SQL query) with columns task_id and command.

**Using Jinja Templating**

Jinja templating can be used to dynamically generate task configurations or even entire DAG definitions. This is particularly useful when you need to pass parameters to tasks or customize the DAG based on external data.

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.utils.dates import days_ago
from datetime import datetime

with DAG(
    dag_id='dynamic_dag_jinja',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    template_searchpath=['/path/to/templates'] # Optional: Specify a directory for Jinja templates
) as dag:
    # Define a Jinja template for the bash command
    bash_command_template = """
    echo "Running task with parameter: {{ params.parameter }}"
    """

    # Create a BashOperator with the Jinja template
    bash_task = BashOperator(
        task_id='bash_task_jinja',
        bash_command=bash_command_template,
        params={'parameter': 'dynamic_value'}
    )
```

In this example, we define a Jinja template for the bash_command. The {{ params.parameter }} placeholder will be replaced with the value of the parameter parameter at runtime. You can also store the Jinja template in a separate file and load it using the template_searchpath parameter of the DAG.

**Best Practices for Dynamic DAG Generation**

- **Keep it Simple**: Avoid overly complex logic in your DAG generation code.
- **Use Configuration Files**: Store DAG configurations in external files to make them easier to manage and update.
- **Test Thoroughly**: Test your dynamic DAG generation code to ensure that it produces the expected DAG structure.
- **Use Logging**: Add logging to your DAG generation code to help debug any issues.
- **Version Control**: Store your DAG generation code in a version control system like Git.
- **Idempotency**: Ensure that your DAG generation code is idempotent, meaning that it produces the same DAG structure regardless of how many times it is executed.
- **Security**: Be careful when using external data to generate DAGs, as this could introduce security vulnerabilities. Sanitize any user-provided data before using it in your DAG generation code.

#### <a name="chapter5part4"></a>Chapter 5 - Part 4: Understanding XComs for Inter-Task Communication

XComs (short for "cross-communication") are a fundamental mechanism in Apache Airflow that allows tasks within a DAG to exchange information. This capability is crucial for building complex workflows where the output of one task needs to be used as input for another. Without XComs, tasks would operate in isolation, severely limiting the types of workflows you could create. This lesson will delve into the intricacies of XComs, exploring how they work, how to use them effectively, and best practices for inter-task communication.

#### <a name="chapter5part4.1"></a>Chapter 5 - Part 4.1: Understanding XComs

XComs are essentially key-value pairs stored in Airflow's metadata database. When a task pushes a value to an XCom, it's stored with a unique key associated with that task instance. Subsequent tasks can then retrieve this value using the same key. This allows for a loosely coupled communication pattern, where tasks don't need to know the specifics of how other tasks are implemented, only the key under which the data is stored.

**How XComs Work**

- **Pushing XComs**: Tasks can push data to XComs using the xcom_push method (implicitly or explicitly). When using the PythonOperator, if a value is returned from the callable, Airflow automatically pushes it to XCom with the key return_value. You can also push multiple XComs with different keys from within a single task.
- **Retrieving XComs**: Tasks can retrieve data from XComs using the xcom_pull method. You need to specify the task_ids of the tasks from which you want to pull the data. You can also filter by key if a task has pushed multiple XComs.
- **Storage**: XComs are stored in Airflow's metadata database. The size of data that can be stored in an XCom is limited by the database configuration. For large data transfers, consider using alternative methods like storing data in a shared file system or object storage (e.g., S3) and passing the path to the data via XComs.
- **Visibility**: XComs are visible within the DAG run in which they are created. They are not persisted across DAG runs unless explicitly handled.

**Implicit vs. Explicit XComs**

- **Implicit XComs**: When using the PythonOperator, any value returned by the Python callable is automatically pushed to an XCom with the key return_value. This is the simplest way to use XComs for basic data transfer.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def my_task_function():
    return "Hello from Task 1!"

with DAG(
    dag_id="implicit_xcom_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    task1 = PythonOperator(
        task_id="task1",
        python_callable=my_task_function
    )

    def task2_function(**kwargs):
        ti = kwargs['ti']
        message = ti.xcom_pull(task_ids='task1', key='return_value')
        print(f"Received message: {message}")
        return message

    task2 = PythonOperator(
        task_id="task2",
        python_callable=task2_function,
        provide_context=True,
    )

    task1 >> task2
```

In this example, task1 implicitly pushes the string "Hello from Task 1!" to XCom. task2 then pulls this value using xcom_pull. The provide_context=True argument is necessary for task2 to access the task instance (ti) and use xcom_pull.

- **Explicit XComs**: You can explicitly push and pull XComs using the ti.xcom_push and ti.xcom_pull methods within your Python callable. This gives you more control over the keys and values being stored.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def push_multiple_xcoms(**kwargs):
    ti = kwargs['ti']
    ti.xcom_push(key='message1', value='This is message 1')
    ti.xcom_push(key='message2', value='This is message 2')

with DAG(
    dag_id="explicit_xcom_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    task1 = PythonOperator(
        task_id="task1",
        python_callable=push_multiple_xcoms,
        provide_context=True,
    )

    def pull_specific_xcom(**kwargs):
        ti = kwargs['ti']
        message1 = ti.xcom_pull(task_ids='task1', key='message1')
        print(f"Received message1: {message1}")
        return message1

    task2 = PythonOperator(
        task_id="task2",
        python_callable=pull_specific_xcom,
        provide_context=True,
    )

    task1 >> task2
```

Here, task1 explicitly pushes two XComs with keys 'message1' and 'message2'. task2 then pulls only 'message1'.

**XCom Data Types**

XComs can store various data types, including:

- Strings
- Numbers (integers, floats)
- Booleans
- Lists
- Dictionaries
- Pickled objects (more complex Python objects)

Airflow automatically serializes and deserializes these data types when pushing and pulling XComs. However, be mindful of the size limitations imposed by the metadata database. For very large or complex objects, consider alternative storage solutions.

**XComs and Task Dependencies**

XComs are often used in conjunction with task dependencies to create complex workflows. By defining dependencies between tasks, you ensure that data is only pulled from an XCom after the task that pushed it has successfully completed.

**Practical Examples and Demonstrations**

**Example 1: Passing a Filename Between Tasks**

Imagine a scenario where one task generates a data file, and a subsequent task needs to process that file.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime
import os

def generate_file():
    filename = "data.txt"
    with open(filename, "w") as f:
        f.write("This is some sample data.")
    return filename

def process_file(filename):
    with open(filename, "r") as f:
        data = f.read()
    print(f"Processing data: {data}")
    # Simulate some processing
    processed_data = data.upper()
    return processed_data

with DAG(
    dag_id="xcom_filename_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    generate_task = PythonOperator(
        task_id="generate_file",
        python_callable=generate_file
    )

    process_task = PythonOperator(
        task_id="process_file",
        python_callable=process_file,
        op_kwargs={'filename': '{{ ti.xcom_pull(task_ids="generate_file") }}'}
    )

    generate_task >> process_task
```

In this example:

- generate_file creates a file named "data.txt" and returns the filename. This filename is implicitly pushed to XCom.
- process_file receives the filename as an argument using Jinja templating: '{{ ti.xcom_pull(task_ids="generate_file") }}'. This pulls the filename from the XCom pushed by generate_file.
- process_file then reads and processes the file.

**Example 2: Passing a List of Values**

Suppose you have a task that retrieves a list of user IDs from a database, and you want to pass this list to another task that sends out emails to those users.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def get_user_ids():
    # Simulate fetching user IDs from a database
    user_ids = [1, 2, 3, 4, 5]
    return user_ids

def send_emails(user_ids):
    for user_id in user_ids:
        print(f"Sending email to user ID: {user_id}")
        # Simulate sending an email
    return f"Emails sent to {len(user_ids)} users"

with DAG(
    dag_id="xcom_list_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    get_ids_task = PythonOperator(
        task_id="get_user_ids",
        python_callable=get_user_ids
    )

    send_emails_task = PythonOperator(
        task_id="send_emails",
        python_callable=send_emails,
        op_kwargs={'user_ids': '{{ ti.xcom_pull(task_ids="get_user_ids") }}'}
    )

    get_ids_task >> send_emails_task
```

Here:

- get_user_ids returns a list of user IDs.
- send_emails receives this list via XCom and iterates through it, simulating sending an email to each user.

**Example 3: Passing a Dictionary**

Let's say you have a task that performs some calculations and returns a dictionary of results.

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def calculate_metrics():
    # Simulate calculating some metrics
    metrics = {
        "revenue": 100000,
        "customers": 500,
        "average_order_value": 200
    }
    return metrics

def store_metrics(metrics):
    print(f"Storing metrics: {metrics}")
    # Simulate storing the metrics in a database or file
    return "Metrics stored successfully"

with DAG(
    dag_id="xcom_dict_example",
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False
) as dag:
    calculate_task = PythonOperator(
        task_id="calculate_metrics",
        python_callable=calculate_metrics
    )

    store_task = PythonOperator(
        task_id="store_metrics",
        python_callable=store_metrics,
        op_kwargs={'metrics': '{{ ti.xcom_pull(task_ids="calculate_metrics") }}'}
    )

    calculate_task >> store_task
```

In this case:

- calculate_metrics returns a dictionary containing calculated metrics.
- store_metrics receives this dictionary and simulates storing it.

**Best Practices for Using XComs**

- **Keep XComs Small**: Avoid storing large amounts of data in XComs, as this can impact performance and strain the metadata database. For large datasets, use external storage solutions like S3 or shared file systems and pass references (e.g., file paths) via XComs.
- **Use Descriptive Keys**: When using explicit XComs, choose descriptive keys that clearly indicate the purpose of the data being stored. This makes it easier for other tasks to understand and use the data.
- **Document XCom Usage**: Clearly document which tasks push and pull XComs, and what data is being exchanged. This improves the maintainability and readability of your DAGs.
- **Consider Alternatives**: For complex data transformations or inter-task communication patterns, consider using alternative approaches like:
  - **Shared File System**: Tasks can read and write data to a shared file system.
  - **Object Storage (e.g., S3)**: Tasks can store and retrieve data from object storage.
  - **Message Queues (e.g., RabbitMQ, Kafka)**: Tasks can exchange messages via a message queue.
- **Be Mindful of Dependencies**: Ensure that tasks pulling XComs have explicit dependencies on the tasks that push them. This guarantees that the data is available when the pulling task runs.
- **Use provide_context=True**: When using PythonOperator and you need to access XComs, remember to set provide_context=True so that the task instance (ti) is available in your callable.
- **Error Handling**: Implement error handling to gracefully handle cases where an XCom is not found or contains unexpected data.

#### <a name="chapter5part5"></a>Chapter 5 - Part 5: Implementing Error Handling and Alerting

Error handling and alerting are crucial components of any robust Airflow deployment. They ensure that you are promptly notified of issues within your DAGs, allowing you to take corrective action and minimize disruptions to your data pipelines. Without proper error handling and alerting, you risk data inconsistencies, missed deadlines, and ultimately, unreliable data. This lesson will cover the essential techniques for implementing effective error handling and alerting in your Airflow DAGs.

#### <a name="chapter5part5.1"></a>Chapter 5 - Part 5.1: Understanding Error Handling in Airflow

Error handling in Airflow involves anticipating potential failures within your tasks and implementing mechanisms to gracefully manage them. This includes retrying failed tasks, providing informative error messages, and preventing cascading failures that can halt your entire DAG.

**Task Retries**

Airflow provides built-in support for task retries. When a task fails, Airflow can automatically retry it a specified number of times. This is particularly useful for handling transient errors, such as temporary network outages or resource limitations.

Example:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

with DAG(
    dag_id='retry_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    default_args={
        'retries': 3,  # Retry each task up to 3 times
        'retry_delay': timedelta(minutes=5),  # Wait 5 minutes between retries
    }
) as dag:
    task1 = BashOperator(
        task_id='failing_task',
        bash_command='exit 1',  # This command will always fail
    )
```

In this example, the failing_task is configured to retry up to 3 times with a 5-minute delay between each retry. If the task fails all 3 times, it will be marked as failed.

**on_failure_callback**

The on_failure_callback is a powerful mechanism for executing a specific function or task when a task instance fails. This allows you to perform actions such as sending an email notification, logging the error, or triggering a rollback procedure.

Example:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.operators.python import PythonOperator
from datetime import datetime, timedelta

def failure_callback(context):
    """
    This function will be executed when a task fails.
    """
    task_instance = context['task_instance']
    log_url = task_instance.log_url
    task_id = task_instance.task_id
    dag_id = task_instance.dag_id

    print(f"Task {task_id} in DAG {dag_id} failed.  See logs at {log_url}")
    # You could also send an email or trigger another process here

with DAG(
    dag_id='failure_callback_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    default_args={
        'retries': 0, # No retries for this example
        'on_failure_callback': failure_callback,
    }
) as dag:
    task1 = BashOperator(
        task_id='failing_task',
        bash_command='exit 1',  # This command will always fail
    )
```

In this example, the failure_callback function is executed when failing_task fails. The function receives a context dictionary containing information about the task instance, including the task ID, DAG ID, and log URL. The example prints a message to the logs, but you could easily modify it to send an email or trigger another process.

**Try-Except Blocks within PythonOperator**

When using the PythonOperator, you can implement more granular error handling using try-except blocks within your Python code. This allows you to catch specific exceptions and handle them accordingly.

Example:

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def my_function():
    try:
        # Code that might raise an exception
        result = 1 / 0  # This will raise a ZeroDivisionError
        return result
    except ZeroDivisionError as e:
        print(f"Caught a ZeroDivisionError: {e}")
        # Handle the exception (e.g., log the error, return a default value)
        return None
    except Exception as e:
        print(f"An unexpected error occurred: {e}")
        # Handle other exceptions
        return None

with DAG(
    dag_id='try_except_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
) as dag:
    task1 = PythonOperator(
        task_id='my_task',
        python_callable=my_function,
    )
```

In this example, the my_function attempts to divide 1 by 0, which will raise a ZeroDivisionError. The try-except block catches this exception, prints an error message, and returns None. This prevents the task from failing and allows the DAG to continue executing. You can have multiple except blocks to handle different types of exceptions.

**Implementing Alerting in Airflow**

Alerting in Airflow involves configuring notifications that are triggered when specific events occur, such as task failures, DAG failures, or SLA misses. This allows you to proactively identify and address issues before they impact your data pipelines.

**Email Alerts**

Airflow provides built-in support for sending email alerts. You can configure email notifications to be sent when tasks fail, DAGs fail, or SLAs are missed.

**Configuration:**

- **Configure SMTP settings**: In your airflow.cfg file, configure the SMTP settings for your email server. This includes the SMTP host, port, username, and password.
- **Set email parameter**: Set the email parameter in your DAG's default_args to a list of email addresses that should receive notifications.
- **Set email_on_failure and email_on_retry parameters**: Set the email_on_failure and email_on_retry parameters in your DAG's default_args to True to enable email notifications for task failures and retries.

Example:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime, timedelta

with DAG(
    dag_id='email_alert_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    default_args={
        'email': ['your_email@example.com'],
        'email_on_failure': True,
        'email_on_retry': False,
        'retries': 1,
        'retry_delay': timedelta(minutes=5),
    }
) as dag:
    task1 = BashOperator(
        task_id='failing_task',
        bash_command='exit 1',  # This command will always fail
    )
```

In this example, email notifications will be sent to your_email@example.com when failing_task fails. Note that email_on_retry is set to False, so no email will be sent when the task is retried.

**Slack Alerts**

Slack is a popular messaging platform that can be integrated with Airflow to send real-time alerts. To send Slack alerts, you can use the SlackWebhookOperator or a custom on_failure_callback function that sends messages to a Slack channel.

**Using SlackWebhookOperator:**

- **Create a Slack App and Webhook**: Create a Slack App and configure an Incoming Webhook for the channel you want to send alerts to.
- **Create an Airflow Connection**: Create an Airflow connection of type "HTTP" to store the Slack Webhook URL.
- **Use SlackWebhookOperator in your DAG**: Use the SlackWebhookOperator to send messages to the Slack channel.

Example:

```py
from airflow import DAG
from airflow.operators.bash import BashOperator
from airflow.providers.slack.operators.slack_webhook import SlackWebhookOperator
from datetime import datetime

SLACK_CONN_ID = 'slack_connection'  # Replace with your Slack connection ID

def task_fail_slack_alert(context):
    """
    Callback function for sending Slack alert on task failure.
    """
    slack_webhook_token = BaseHook.get_connection(SLACK_CONN_ID).password
    slack_msg = """
            :red_circle: Task Failed.
            *Task*: {task}
            *Dag*: {dag}
            *Execution Time*: {exec_date}
            *Log Url*: {log_url}
            """.format(
            task=context.get('task_instance').task_id,
            dag=context.get('task_instance').dag_id,
            exec_date=context.get('execution_date'),
            log_url=context.get('task_instance').log_url,
        )

    slack_alert = SlackWebhookOperator(
        task_id='slack_alert',
        slack_webhook_conn_id=SLACK_CONN_ID,
        message=slack_msg
    )

    return slack_alert.execute(context=context)

with DAG(
    dag_id='slack_alert_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
    default_args={
        'retries': 0,
        'on_failure_callback': task_fail_slack_alert,
    }
) as dag:
    task1 = BashOperator(
        task_id='failing_task',
        bash_command='exit 1',  # This command will always fail
    )
```

In this example, the task_fail_slack_alert function is executed when failing_task fails. The function uses the SlackWebhookOperator to send a message to the Slack channel specified in the slack_connection connection.

**Custom Alerting**

You can also implement custom alerting mechanisms using Python code within your DAGs. This allows you to integrate with other monitoring systems or implement more complex alerting logic.

Example:

```py
from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def custom_alert(ti):
    """
    This function will be executed to send a custom alert.
    """
    task_instance = ti.task_instance
    task_id = task_instance.task_id
    dag_id = task_instance.dag_id
    xcom_value = ti.xcom_pull(task_ids='my_task', key='return_value')

    # Example: Send an alert if the XCom value is above a threshold
    if xcom_value > 100:
        print(f"Alert: XCom value for task {task_id} in DAG {dag_id} is above threshold: {xcom_value}")
        # Add your custom alerting logic here (e.g., send an email, trigger an API call)
    else:
        print(f"XCom value for task {task_id} in DAG {dag_id} is within acceptable range: {xcom_value}")

with DAG(
    dag_id='custom_alert_example',
    start_date=datetime(2023, 1, 1),
    schedule_interval=None,
    catchup=False,
) as dag:
    def my_function(ti):
        # Simulate a task that returns a value to XCom
        ti.xcom_push(key='return_value', value=150)
        return 150

    task1 = PythonOperator(
        task_id='my_task',
        python_callable=my_function,
    )

    task2 = PythonOperator(
        task_id='alert_task',
        python_callable=custom_alert,
        op_kwargs={'ti': task1}
    )

    task1 >> task2
```

In this example, the custom_alert function is executed after my_task. The function retrieves a value from XCom and sends an alert if the value is above a certain threshold. This demonstrates how you can implement custom alerting logic based on the results of your tasks.

**Best Practices for Error Handling and Alerting**

- **Be specific with your error handling**: Catch specific exceptions rather than using a generic except Exception block. This allows you to handle different types of errors in different ways.
- **Provide informative error messages**: Include as much information as possible in your error messages, such as the task ID, DAG ID, execution date, and any relevant input parameters.
- **Use appropriate retry settings**: Configure retry settings based on the type of error and the criticality of the task. Avoid excessive retries, as they can delay your DAG and consume resources.
- **Implement alerting for critical failures**: Configure alerts for critical failures that can impact your data pipelines or business operations.
- **Test your error handling and alerting**: Regularly test your error handling and alerting mechanisms to ensure that they are working as expected.
- **Centralized logging**: Use Airflow's logging capabilities to centralize logs for easier debugging and troubleshooting.
- **Monitor Airflow's health**: Monitor Airflow's health and performance to identify potential issues before they impact your DAGs.

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
