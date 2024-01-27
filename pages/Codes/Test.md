---
title: Codes
last_updated: January 27, 2024
summary: "This section contains Codes from the workshop and other sources."
sidebar: mydoc_sidebar
permalink: Test.html
folder: Codes
---

This code uses a thread pool created with **`**concurrent.futures.ThreadPoolExecutor**`** to run two worker tasks concurrently. The main thread waits for the worker threads to finish using **`**pool.shutdown(wait=True)**`**. This allows for efficient parallel processing of tasks in a multi-threaded environment.

-   Python3

`import` `concurrent.futures`

`def` `worker():`

`print``(``"Worker thread running"``)`

`pool` `=` `concurrent.futures.ThreadPoolExecutor(max_workers``=``2``)`

`pool.submit(worker)`

`pool.submit(worker)`

`pool.shutdown(wait``=``True``)`

`print``(``"Main thread continuing to run"``)`

**Output**

```
Worker thread running
Worker thread running
Main thread continuing to run



```