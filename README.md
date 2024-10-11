<h1 align="center"> Airflow </h1>

# Content

1. [Chapter 1: Introduction to Airflow](#chapter1)
    - [Chapter 1 - Part 1: What is Apache Airflow](#chapter1part1)
    - [Chapter 1 - Part 2: Benefits of Airflow](#chapter1part2)
    - [Chapter 1 - Part 3: Core Components of Airflow](#chapter1part3)
    - [Chapter 1 - Part 4: Core Concepts of Airflow](#chapter1part4)
2. [Chapter 2: Development Environment](#chapter2)
    - [Chapter 2 - Part 1: Creating the Development Environment with Docker](#chapter2part1)

## <a name="chapter1"></a>Chapter 1: Introduction to Airflow

#### <a name="chapter1part1"></a>Chapter 1 - Part 1: What is Apache Airflow

Airflow is an open source platform to programmatically author, schedule, and monitor workflows.

Airflow is a tool that helps you create, organize, and keep track of your data tasks automatically

 It was initially developed by Airbnb in 2014 to manage complex workflows and data pipelines. Since then, it has become one of the most popular tools for orchestrating workflows, particularly in data engineering and machine learning.

Airflow provides a flexible and scalable way to define and automate workflows, making it easy to manage tasks, track progress, and handle dependencies between various stages of a workflow. It is designed to scale horizontally, making it ideal for large-scale data engineering projects or any environment where automation and reliability are crucial.

**Key Features of Apache Airflow**

- **Workflow as Code**: Airflow allows you to define workflows using standard Python code. This approach offers flexibility, as you can use Python’s programming features (functions, loops, conditionals, etc.) to create dynamic and reusable workflows.

- **DAG (Directed Acyclic Graph) Structure**: Workflows in Airflow are represented as DAGs. A DAG is a collection of tasks with dependencies between them, where each task represents a unit of work (e.g., running a script, querying a database, or sending a notification). The acyclic nature ensures that tasks do not create circular dependencies.

- **Scheduling**: Airflow has a powerful scheduler that triggers workflows based on time intervals or external events. You can schedule workflows to run daily, hourly, or at any custom interval, ensuring that data pipelines are always up-to-date.

- **Task Dependencies and Management**: Airflow allows you to define complex dependencies between tasks, ensuring that they are executed in the right order. You can also set up retries, define timeouts, and handle task failures gracefully.

- **UI for Monitoring**: Airflow comes with an intuitive web-based user interface where you can monitor, trigger, and debug workflows. The UI provides a visual representation of DAGs, showing task status, logs, and execution times, making it easy to manage and troubleshoot workflows.

- **Extensibility with Operators**: Airflow provides a wide variety of built-in operators to interact with different services (e.g., AWS S3, Google Cloud, databases, and more). You can also create custom operators to extend its functionality or to handle specific tasks.

- **Scalability**: Airflow is built to scale. It supports parallelism and distributed task execution, allowing you to scale out your workflows across multiple worker nodes. This makes Airflow suitable for environments ranging from small-scale to enterprise-level data pipelines.

**Common Use Cases for Airflow**

- **ETL Pipelines (Extract, Transform, Load)**: Airflow is frequently used to orchestrate data pipelines that extract data from various sources, transform it, and load it into target systems like data warehouses.

- **Data Engineering and Analytics**: Teams use Airflow to automate data processing workflows, such as running scheduled queries on databases or orchestrating machine learning model training pipelines.

- **Data Integration**: Airflow can manage workflows that integrate data from multiple APIs, databases, and cloud storage services, allowing organizations to build robust data ecosystems.

- **Machine Learning Pipelines**: Airflow can be used to automate and orchestrate complex machine learning workflows, from data preprocessing to model training and evaluation.

#### <a name="chapter1part2"></a>Chapter 1 - Part 2: Benefits of Airflow

**Dynamic**

- Airflow can adapt and change based on what is happening.
  - Python Based: You can write your workflows in Python, since Python is more easy to use
  - Dynamic tasks: Generate tasks based on dynamic inputs.
  - Dynamic workflows: Generate workflows based on static inputs.
  - Branching: Execute a different set of tasks based on a condition or result
 
**Scalability**

- Airflow is built to scale.
- It supports parallelism and distributed task execution, allowing you to scale out your workflows across multiple worker nodes.
- This makes Airflow suitable for environments ranging from small-scale to enterprise-level data pipelines.

**Fully Functional User Interface**

- Airflow has a visual dashboard where you can see and control your tasks and workflows
  - can monitor and troubleshoot your workflows.
  - can highlight relationships between workflows and tasks.
  - identify bottlenecks with performance metrics
  - manage users and roles of your airflow instance
 
**Extensibility**

- Add a new features or connect airflow to other tools easily.
  - Many providers: package with functions to interact with the tool or service, such as AWS, snowflake and so on
  - Customizablw user interface
  - Possibility to custom existing functions

#### <a name="chapter1part3"></a>Chapter 1 - Part 3: Core Components of Airflow

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
   
#### <a name="chapter1part4"></a>Chapter 1 - Part 4: Core Concepts of Airflow

TODO

## <a name="chapter1"></a>Chapter 2: Development Environment

#### <a name="chapter1part1"></a>Chapter 1 - Part 1: Creating the Development Environment with Docker
