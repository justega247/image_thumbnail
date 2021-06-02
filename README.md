Asynchronous Tasks in Django with Redis and Celery


Celery is a Python based task queuing software package that enables execution of asynchronous computational workloads driven by information contained in messages that are produced in application code (Django in this example) destined for a Celery task queue. Celery can also be used to execute repeatable, period (ie, scheduled).

Celery is best used in conjunction with a storage solution that is often referred to as a message broker. A common message broker that is used with celery is Redis which is a performant, in memory, key-value data store. Specifically, Redis is used to store messages produced by the application code describing the work to be done in the Celery task queue. Redis also serves as storage of results coming off the celery queues which are then retrieved by consumers of the queue.
