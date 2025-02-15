# Django Celery Async Tasks

This project demonstrates how to use **Celery** for asynchronous task execution in a Django application. It also integrates **Celery Beat** to schedule periodic tasks.

## Features
- **Celery Worker** for executing background tasks.
- **Celery Beat** for scheduling recurring tasks.
- **Redis** as the message broker.

---
![image](https://github.com/user-attachments/assets/781d2114-8dc1-4bac-a290-0654ec859238)
---

## Running Celery
#### 1. Start Celery Worker
To process asynchronous tasks, run:
  ```
  celery -A django_celery worker --loglevel=info
  ```
#### 2. Start Celery Beat (for periodic tasks)
  ```
  celery -A django_celery beat --loglevel=info
  ```
#### 3. Check Running Tasks Manually
  ```
  from feedback.tasks import print_my_name
  print_my_name.delay()
  ```
#### 4. Monitor Celery:
  ```
  celery -A django_celery flower
  ```

#### Thanks


