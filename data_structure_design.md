# Datastore systems
- [Operational](https://en.wikipedia.org/wiki/Operational_database): the system that is used to process the day-to-day transactions of an organization. *Speed* and *integrity* ([ACID](https://en.wikipedia.org/wiki/ACID)) are key characteristics. 
- [Warehouse](https://en.wikipedia.org/wiki/Data_warehouse): the system used for reporting and data analysis, and is considered a core component of business intelligence. The data stored in the warehouse is uploaded from the operational systems.

# Data models
- Relational (a.k.a. normalized) model: focuses on the business transactions

- Dimensional model: focuses on the business effect of a sets of transactions 
  - Fact: represents a measurement.
    - Generally *numeric* data.
    - In a data cube, facts are values corresponding to the coordinates.
  - Dimension: reference information that gives context to the facts.
    - Generally *categorical* data.
    - In a data cube, dimensions are the categorical coordinates in a multi-dimensional cube.
  
  
