# Airflow Basic

## Setting
**Set config**
```bash
# /airflow/airflow.cfg

dags_folder = /airflow/dags 
default_timezone = Asia/Seoul 
default_ui_timezone = Asia/Seoul 
load_example = False # remove example
load_default_connections = False
```
Airflow 초기 세팅을 위한 config 파일 수정
- dags 디렉토리 설정
- scheduler, webserver 타임존 설정
- 예제 파일 삭제(파일 삭제 반영을 위해 db 초기화)

**Airflow DB 초기화**
```zsh
rm -rf airflow.db # Remove example
airflow db init
```
**Start Airflow**
```zsh
airflow webserver # start webserver
airflow scheduler # start scheduler
```
웹 서버, 스케줄러는 분리되어 있음
- 웹 서버. Airflow DAG 및 Task 관리
- 스케줄러. Airflow DAG 및 Task 실행

<br>

## DAGs
A DAG (Directed Acyclic Graph) is the core concept of Airflow, collecting Tasks together, organized with dependencies and relationships to say how they should run.  
-> DAG(Directed Acyclic Graph)는 Airflow의 핵심으로, 작업이 어떻게 실행되는지를 작업간의 종속성, 관계를 반영하여 나타낸다.

<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/main/images/airflow/airflow_dag.png></p>

A, B, C, D의 네 가지 Task를 정의하고 실행 순서와 각 Task 간의 관계를 설정합니다. 또한 DAG를 실행하는 시점과 빈도도 설정 가능합니다. DAG는 작업 내부에서 어떤 일이 발생하는지에 대해 신경 쓰지 않고, 작업 실행 순서, 실행 횟수, 시간 초과가 발생한 경우 등과 같은 작업 실행에만 집중합니다.

### Declare DAG
**Default**
```python
 import datetime
 from airflow import DAG
 from airflow.operators.empty import EmptyOperator

 with DAG(
     dag_id="my_dag_name",
     start_date=datetime.datetime(2021, 1, 1),
     schedule="@daily",
 ):
     EmptyOperator(task_id="task")
```
**Decorator를 활용하여 dag argment 선언**
```python
import datetime
from airflow.decorators import dag
from airflow.operators.empty import EmptyOperator

@dag(start_date=datetime.datetime(2021, 1, 1), schedule="@daily")
def generate_dag():
    EmptyOperator(task_id="task")

generate_dag()
```


### Task Dependencies
Task 의존성은 아래와 같이 operator를 사용하여 선언할 수 있지만, 단순 표현식인 ">>" 선호
```python
from airflow.models.baseoperator import cross_downstream

# Replaces
# [op1, op2] >> op3
# [op1, op2] >> op4
cross_downstream([op1, op2], [op3, op4])
```
---
## Reference
https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/dags.html
