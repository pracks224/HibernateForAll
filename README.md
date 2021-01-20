   Hibernate Tutorial
* Hibernate is an open source Java persistence framework project. 
* It performs powerful object-relational mapping and query databases using HQL and SQL. 
* Hibernate is a great tool for ORM mappings in Java. 
* It can cut down a lot of complexity and thus defects as well from your application, which may otherwise find a way to exist. 
* This is specially boon for developers with limited knowledge of SQL. 
* Initially started as an ORM framework, Hibernate has spun off into many projects, such as Hibernate Search, Hibernate Validator, Hibernate OGM (for NoSQL databases), and so on.
* ORM Tool
An ORM tool simplifies the data creation, data manipulation and data access. It is a programming technique that maps the object to the data stored in the database.


The ORM tool internally uses the JDBC API to interact with the database.
What is JPA?
Java Persistence API (JPA) is a Java specification that provides certain functionality and standard to ORM tools. The javax.persistence package contains the JPA classes and interfaces.
Advantages of Hibernate Framework
Following are the advantages of hibernate framework:
1) Open Source and Lightweight
Hibernate framework is open source under the LGPL license and lightweight.
2) Fast Performance
The performance of hibernate framework is fast because cache is internally used in hibernate framework. There are two types of cache in hibernate framework first level cache and second level cache. First level cache is enabled by default.
3) Database Independent Query
HQL (Hibernate Query Language) is the object-oriented version of SQL. It generates the database independent queries. So you don't need to write database specific queries. Before Hibernate, if database is changed for the project, we need to change the SQL query as well that leads to the maintenance problem.
4) Automatic Table Creation
Hibernate framework provides the facility to create the tables of the database automatically. So there is no need to create tables in the database manually.
5) Simplifies Complex Join
Fetching data from multiple tables is easy in hibernate framework.
6) Provides Query Statistics and Database Status
Hibernate supports Query cache and provide statistics about query and database status.

Hibernate Architecture
The Hibernate architecture includes many objects such as persistent object, session factory, transaction factory, connection factory, session, transaction etc.

The Hibernate architecture is categorized in four layers.
o Java application layer
o Hibernate framework layer
o Backhand api layer
o Database layer
Let's see the diagram of hibernate architecture:

This is the high level architecture of Hibernate with mapping file and configuration file.


Hibernate framework uses many objects such as session factory, session, transaction etc. along with existing Java API such as JDBC (Java Database Connectivity), JTA (Java Transaction API) and JNDI (Java Naming Directory Interface).

Elements of Hibernate Architecture
For creating the first hibernate application, we must know the elements of Hibernate architecture. They are as follows:SessionFactory
The SessionFactory is a factory of session and client of ConnectionProvider. It holds second level cache (optional) of data. The org.hibernate.SessionFactory interface provides factory method to get the object of Session.
Session
The session object provides an interface between the application and data stored in the database. It is a short-lived object and wraps the JDBC connection. It is factory of Transaction, Query and Criteria. It holds a first-level cache (mandatory) of data. The org.hibernate.Session interface provides methods to insert, update and delete the object. It also provides factory methods for Transaction, Query and Criteria.
Transaction
The transaction object specifies the atomic unit of work. It is optional. The org.hibernate.Transaction interface provides methods for transaction management.
ConnectionProvider
It is a factory of JDBC connections. It abstracts the application from DriverManager or DataSource. It is optional.
TransactionFactory
It is a factory of Transaction. It is optional.

