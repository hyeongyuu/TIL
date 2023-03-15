# Airflow tutorial

<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/f4828eed22350524b098063a5c11afad2f212c8b/images/airflow/airflow.png height="100px" width="250px"></p>

## Airflow
Apache Airflow is an open-source platform for developing, scheduling, and monitoring batch-oriented workflows.  
-> Apache Airflow는 배치 지향 워크플로우를 개발, 스케줄링 및 모니터링하기 
위한 오픈 소스 플랫폼

<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/main/images/airflow/airflow_architecture.png></p>

- Airflow workflow는 DAG(Directed Acyclic Graph)로 나타내며 개별 Task를 포함, DAG는 각 Task의 dependency와 data flow를 고려하여 작성
- Scheduler로 workflow를 트리거하여 실행할 Task를 Worker로 전달, Excuter는 Worker가 전달받은 Task를 실행하는 주체
- Webserver. 편리한 inspect, trigger, debug를 위한 웹 UI 서버
- Metadata Database. Scheduler, Executor, Webserver 상태 저장을 위한 database


## Quick Start Airflow
### Install airflow
``` zsh
python3 -m virtualenv env_airflow --python=python3.8.16


mkdir ~/airflow
export AIRFLOW_HOME=~/airflow

AIRFLOW_VERSION=2.5.1
PYTHON_VERSION="$(python --version | cut -d " " -f 2 | cut -d "." -f 1-2)"
CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-${PYTHON_VERSION}.txt"

pip install "apache-airflow==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"


airflow version
```
### Manage users
```zsh
airflow users list
id | username | email             | first_name | last_name | roles
===+==========+===================+============+===========+======
1  | admin    | admin@example.com | Admin      | User      | Admin

airflow users create -f Moon -l Hyeongyu -u hyeongyu -e hyeongyu.moon@gmail.com -r Admin -p 123123

airflow users list
id | username | email                   | first_name | last_name | roles
===+==========+=========================+============+===========+======
1  | admin    | admin@example.com       | Admin      | User      | Admin
2  | hyeongyu | hyeongyu.moon@gmail.com | Moon       | Hyeongyu  | Admin

# role. Admin, Public, Viewer, User, Op
airflow users add-role -u admin -r Admin
airflow users remove-role -u admin -r Admin
airflow users delete -u admin
```

###
```zsh
airflow webserver --port 8080
airflow dags list
```

## Reference
https://airflow.apache.org/  
https://www.bucketplace.com/post/2021-04-13-버킷플레이스-airflow-도입기/