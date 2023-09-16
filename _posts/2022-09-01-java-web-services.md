---
layout: post
title:  "Java Web Services"
date:   2022-09-01
category: Java
permalink: /java/:title
---

# What is a web service

Service available over web. The main objective of a web service is to serve data to applications in different platforms such as mobile application, desktop or web applications. Web services are for application consumption and they are language independent. 


# What is an API?

API stands for Application Programming Interface. It is a bridge between applications. It can be referred as an end-point. For example, `http://localhost:8080/employees/1`. The same URL can be used for different types of HTTP request such as GET, POST, DELETE, PUT etc. 

Best practice: End-points are structured in directory structure

# What are the types of web services?

## SOAP (Simple Object Access Protocol) based web services (API)

- Heavy-weight - SOAP services required to follow some protocol which leads to the consumption of more resources
- Always return the response in XML format, thus requiring XML parser and some other additional resources as well
- These web services use WSDL (Web Service Description Language) files (XML file).
- WSDL files describes the details of web service that include (name, type of operations, datatypes, location etc.)


## RESTful Web Services (API)

REST stands for Representationsl State Transfer. These services are not protocol based, they are just designed based on the architechtureal pattern.

Key Characterstics
- Light-weight - RESTful services consume less resources
- These web services can serve data in multiple formats such as XML, JSON (JavaScript Object Notation) etc. JSON provide data in key-value pairs.


# Spring Data JPA (Java/Jakarta Persitence API)

Add an additional abstraction by providing various "Java interfaces" such as

- Repository
- CrudRepository
- PagingAndSortingRepository (used to implement pagination)
- JpaRepository

All the above interfaces are referred as `Repositories`. Implementation classes are provided so there is no need to wrtie the implementation.  




# API Client

`Postman` is a popular API client to test end-points. This tool is also available online. Postman facilitates with publishing API documentation which saves time for the API consumers.


