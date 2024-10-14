<h1 align="center"> Airflow </h1>

# Content

1. [Chapter 1: Introduction to Airflow](#chapter1)
    - [Chapter 1 - Part 1: What is Apache Airflow](#chapter1part1)
    - [Chapter 1 - Part 2: Benefits of Airflow](#chapter1part2)
    - [Chapter 1 - Part 3: Core Components of Airflow](#chapter1part3)
    - [Chapter 1 - Part 4: Scheduling and executing pipelines](#chapter1part4)
    - [Chapter 1 - Part 5: Core Concepts of Airflow](#chapter1part5)
    - [Chapter 1 - Part 6: The Different Architectures to run Airflow](#chapter1part6)
    - [Chapter 1 - Part 7: Reasons not to choose Airflow](#chapter1part7)
2. [Chapter 2: Development Environment](#chapter2)
    - [Chapter 2 - Part 1: Creating the Development Environment](#chapter2part1)
    - [Chapter 2 - Part 2: Init Apache Airflow with Docker](#chapter2part2)
3. [Chapter 3: Data Pipeline with Airflow](#chapter3)
    - [Chapter 3 - Part 1: The Project](#chapter3part1)

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
   
#### <a name="chapter1part4"></a>Chapter 1 - Part 4: Scheduling and executing pipelines

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
   
#### <a name="chapter1part5"></a>Chapter 1 - Part 5: Core Concepts of Airflow

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

**Operator**

- An operator defines a single, ideally idempotent task in your Dag (Idempotent means that you can run this task, this operator as many times as you want for the same input.)
- Operators allow you to break down your workflow into discrete, manageable pieces of work.
- Airflow has thousands of operators.
  - The PythonOperator to execute a Python script or function.
  - The BashOperator to execute a bash script, or command
  - The SQLExecuteQueryOperator to execute a SQL query to a database
  - The FileSensor to wait for a file
 
**Task/Task Instance**

- A task is a specific instance of an operator. When an operator is assigned to a Dag, it becomes a task.
- Tasks are the actual units of work that get executed when your Dag runs.

**Workflow**

- A workflow is the entire process defined by your Dag, including all tasks and their dependencies.
- It represents your entire data pipeline showing how all the pieces fit together to achieve your goal

<br>

<div align="center"><img src="img/workflow-w812-h762.png" width=812 height=762><br><sub>Example of a Workflow - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>

<br>

When the BashOperator runs, for example, in 1 of janary of 2024, it becomes a Task Instance (TI)

**Tasks vs. operators**

Operators provide the implementation of a piece of work. Airflow has a class called BaseOperator and many subclasses inheriting from the BaseOperator, such as PythonOperator, EmailOperator, and OracleOperator. Tasks in Airflow manage the execution of an operator;
they can be thought of as a small wrapper or manager around an operator that ensures the operator executes correctly. The user can focus on the work to be done by using operators, while Airflow ensures correct execution of the work via tasks.

- Operators define what a task does, while tasks are the actual instances of these actions that get executed within a DAG.
- Operators are reusable templates, whereas tasks are tied to a specific workflow and its execution.

- **Operator**: PythonOperator defines the action of running a Python function.
- **Task**: When you assign the PythonOperator to a DAG, it becomes a task, like process_data_task, and represents the specific step of running that Python function in the workflow.

Scheduling and executing pipelines

#### <a name="chapter1part6"></a>Chapter 1 - Part 6: The Different Architectures

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

#### <a name="chapter1part7"></a>Chapter 1 - Part 7: Reasons not to choose Airflow

- Handling streaming pipelines, as Airflow is primarily designed to run recurring or batch-oriented tasks, rather than streaming workloads.
- Implementing highly dynamic pipelines, in which tasks are added/removed between every pipeline run. Although Airflow can implement this kind of dynamic behavior, the web interface will only show tasks that are still defined in the most recent version of the DAG. As such, Airflow favors pipelines that do not change in structure every time they run.

## <a name="chapter2"></a>Chapter 2: Development Environment

#### <a name="chapter2part1"></a>Chapter 2 - Part 1: Creating the Development Environment with Docker

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

#### <a name="chapter2part2"></a>Chapter 2 - Part 2: Init Apache Airflow with Docker

- Create the project folder (E.g:C:\Workspace\airflow-tutorial)
- Create a python virtual enviroment in this folder (If Windows ```python -m venv venv```, if Linux ```python3 -m venv venv```)
- Active the virtual enviroment (If Windows ```.\venv\Scripts\activate```, if Linux ```source venv/bin/activate````)
- Download the ```docker compose file``` and the ```.env``` file that is in this [folder](https://github.com/vitorstabile/airflow-basics/tree/main/docker-image)
- Save the ```docker compose file``` and the ```.env``` in the project folder
- Go to the project folder, open the cmd or terminal and make ```docker-compose up -d```
- You will see somenthing like this

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

## <a name="chapter3"></a>Chapter 3: Data Pipeline with Airflow

#### <a name="chapter3part1"></a>Chapter 3 - Part 1: The Project

