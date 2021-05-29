+++
title = "Using apscheduler for scheduling periodic tasks"
date = 2021-04-18
[taxonomies]
tags = ["python"]
+++

There are multiple options out there to run scheduled or recurring jobs in python. In my case I needed something that was simple and easy to use for my [project](https://github.com/neelabalan/keystrokestat) where I periodically need to write to SQLite DB in the background. 

<!-- more -->

[![workflow.png](https://i.postimg.cc/d0HkwKn4/workflow.png)](https://postimg.cc/wtNTQZCm)

I could go with either [schedule](https://schedule.readthedocs.io/en/stable/) or [apscheduler](https://apscheduler.readthedocs.io/) for my project. I wanted to try my hands on apscheduler because I saw a lot of features it had like 
- Job stores to store the scheduled jobs so the next job executes even when the process is restarted
- Option to check each missed execution time
- Scheduler events to monitor the successful execution of the job
- Number of workers can be assigned to execute the task

I've used some of these features in my side projects but not all in *keystrokestat*


[**code snippet**](https://github.com/neelabalan/keystrokestat/blob/master/script/keystroke.py)
```python
from apscheduler.schedulers.background import BackgroundScheduler
scheduler = BackgroundScheduler(daemon=True)

SCHEDULER_INTERVAL = 5

def workflow(buffer):
    sqlite_connection = engine.connect()
    # do some work ...
    # Write records stored in a DataFrame to a SQLite
    df.to_sql("keystroke", sqlite_connection, if_exists="append")
    sqlite_connection.close()


def run():
    scheduler.add_job(
        # runs workflow every 5 seconds
        workflow, trigger="interval", seconds=SCHEDULER_INTERVAL, args=(echos,)
    )
    scheduler.start()
```


### Other interesting projects using apscheduler

- [diffido](https://github.com/alberanid/diffido)
    Alerts when there are changes in webpages
- [lightning](https://github.com/anitejb/lightning)
    Real time monitoring of Rutgers Schedule of Classes
- [scrapyweb](https://github.com/igaotang/scrapyweb)
    Web app for Scrapyd cluster management
