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
    - [Chapter 1 - Part 2.4: Real-World Application](#chapter1part2.4)
  - [Chapter 1 - Part 3: Airflow Architecture: Scheduler, Webserver, and Metadata Database](#chapter1part3)
    - [Chapter 1 - Part 3.1: Core Components of Airflow](#chapter1part3.1)
    - [Chapter 1 - Part 3.2: Interaction Between Components](#chapter1part3.2)
    - [Chapter 1 - Part 3.3: Executors](#chapter1part3.3)
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
    - [Chapter 1 - Part 5.4: Practice Activities](#chapter1part5.4)
  
## <a name="chapter1"></a>Chapter 1: Introduction to Apache Airflow

#### <a name="chapter1part1"></a>Chapter 1 - Part 1: What is Apache Airflow and why use it?

#### <a name="chapter1part1.1"></a>Chapter 1 - Part 1.1: What is Apache Airflow?

#### <a name="chapter1part1.2"></a>Chapter 1 - Part 1.2: Why Use Apache Airflow?

#### <a name="chapter1part1.3"></a>Chapter 1 - Part 1.3: Real-World Applications

#### <a name="chapter1part2"></a>Chapter 1 - Part 2: Understanding DAGs, Tasks, and Operators

#### <a name="chapter1part2.1"></a>Chapter 1 - Part 2.1: Directed Acyclic Graphs (DAGs)

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

#### <a name="chapter1part2.2"></a>Chapter 1 - Part 2.2: Tasks

#### <a name="chapter1part2.3"></a>Chapter 1 - Part 2.3: Operators

#### <a name="chapter1part2.4"></a>Chapter 1 - Part 2.4: Real-World Application

#### <a name="chapter1part3"></a>Chapter 1 - Part 3: Airflow Architecture: Scheduler, Webserver, and Metadata Database

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

#### <a name="chapter1part3.1"></a>Chapter 1 - Part 3.1: Core Components of Airflow

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

#### <a name="chapter1part3.2"></a>Chapter 1 - Part 3.2: Interaction Between Components

#### <a name="chapter1part3.3"></a>Chapter 1 - Part 3.3: Executors

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

Before you begin, ensure you have the following installed:

- **Docker**: Docker is the core technology for containerization. You can download and install Docker Desktop from the official Docker website: https://www.docker.com/products/docker-desktop/
- **Docker Compose**: Docker Compose is used to define and manage multi-container applications. Docker Compose is included with Docker Desktop. Verify the installation by running docker-compose --version in your terminal.

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

- **Save the Docker Compose File**: Save the provided docker-compose.yaml file into this directory.

- **Create .env File (Optional)**: You can create a .env file to override the default environment variables. This is useful for setting your own passwords, user IDs, or Airflow image version.

Here’s an example .env file:

```
AIRFLOW_UID=50000
_AIRFLOW_WWW_USER_USERNAME=admin
_AIRFLOW_WWW_USER_PASSWORD=admin
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

#### <a name="chapter1part5.1"></a>Chapter 1 - Part 5.1: Accessing the Airflow UI

#### <a name="chapter1part5.2"></a>Chapter 1 - Part 5.2: Key Components of the Airflow UI

#### <a name="chapter1part5.3"></a>Chapter 1 - Part 5.3: Using the Airflow UI for Monitoring and Troubleshooting

#### <a name="chapter1part5.4"></a>Chapter 1 - Part 5.4: Practice Activities



#### <a name="chapter1part3"></a>Chapter 1 - Part 3: Core Components of Airflow


   
#### <a name="chapter1part4"></a>Chapter 1 - Part 4: Scheduling and executing pipelines


   
#### <a name="chapter1part5"></a>Chapter 1 - Part 5: Core Concepts of Airflow



#### <a name="chapter1part6"></a>Chapter 1 - Part 6: The Different Architectures



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

