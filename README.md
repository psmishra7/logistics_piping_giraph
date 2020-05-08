Sparkling Warehouse
===

Sparkling Warehouse is a set of scripts that builds complex workflow of batch jobs for analysing logistics raw data by using spark. It handles data preprocessing (`pipeline`), data modeling/instantiation (`nozzle`), workflow management (`valve`), visualization (`tank`), and much more.

The idea of the Warehouse is to address an unwieldy memory issue typically associated with long-running batch processes when dealing with massive data in local force-dynamics projects. By dint of much trying, I started thinking to decompose the analytical problem into tasks that can be executed in parallel & series, and make every component be memory-friendly.

Basically, all the feature service logic for the Warehouse that requires high frequency R&W manipulations on the large raw dataset by were rewritten. Clearly, by deploying computation on Spark, the Warehouse makes the workflow easy to design without concern about insufficient memory, and it also greatly improves computational performance.

Ideally, you can assemble pretty much any `pipelines` of tasks you want and manage them by `valves`, but the warehouse still comes with some one-button pipeline templates that you can use. It includes support for running ...

Change Log
---
***Dec 21, 2017*** Bulid first pipeline for testing workflow which was newly refactored on Spark.
