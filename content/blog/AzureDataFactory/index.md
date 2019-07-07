---

title: Azure Data Factory_The lake of Storage
date: "2019-07-07T20:26:33.962Z"
---

# Why Azure Data Factory
Suppose you are running a huge company which has a huge database on-premise. Now to keep that data secure and safe you need to need to keep it somewhere where no one can harm it. So, if you are thinking to keep your database on cloud then you are thinking correct. But it isn't that easy. You have to manage your database properly before uploading it to cloud.

Azure Data Factory will help you to automate this stuff or I should say orchestrate these tasks into a easy way.

## Data Factory
In layman language data factory is a service which will help you to store data then make that data ready for processing by managing and manipulating it.
Alternatively, it collects the data then transform it into various schemas and then makes it ready for publishing and monitoring.

## Data Factory Concepts

- pipelines
Considering the above example suppose your company has pushed the data into a cloud and its performing some activity on that data which is done in a pipeline.

- datasets
Your companies data will be stored in a data structure which is known as datasets.

- linked services
Now suppose your company have to push data to cloud and this obviously cannot be done with help of some magic. You will need a medium or an external service to upload that data to cloud. These tools are called linked service.

- activities
Performing some action on data stored is known as activity.

## Data Lakes
Data Lakes perform two-in-one task. It lets you to store data from all sources of any size and type and then help you to analyze that data with the help of various analytics tools.

## Data Warehouse
Data is written in a structured format or in a particular form. You have to read that data in the form it is written. It uses SQl to query your data.