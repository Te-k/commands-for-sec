# Airflow

**Run the web server:**
```
airflow webserver -p 8080
```

**Test a task from a DAG:**
```
airflow test DAG TASK 2017-03-18T18:00:00.0
```

**List DAGs:**
```
airflow list_dags
```

**Run a DAG:**
```
airflow trigger_dag DAG
```
