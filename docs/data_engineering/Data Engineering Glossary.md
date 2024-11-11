- ETL
- Conformed Dimensions
- Conformed Facts

### D
- Data Anomalies
	- outliers (or) exceptions လို့လဲ သုံးနှုန်းကြပါတယ်။
	-  Database ထဲမှာ သိမ်းထားတဲ့ ဒေတာတွေ အကြား style အရ ၊ type အရ (သို့) formatting အရ မတူညီ ခြားနားမှုတွေကို ဆိုလိုတာပါ။
	- ဒါတွေက Data Ingestion လုပ်တဲ့အချိန်နဲ့ Data Update လုပ်တဲ့အချိန်မှာ အရေးကြီးပါတယ်။
	- မတိကျတဲ့ ၊ မှားယွင်းနေတဲ့ ဒေတာ (သို့) reporting မဖြစ်ရအောင် Anomalies တွေကို သေသေချာချာ စီစစ်ဖို့ လိုပါတယ်။


|   |   |
|---|---|
|ACID|Database properties includes Atomicity, Consistency, Isolation, Durability designed on the foundations of relational algebra|
|CRUD|Create, Retrieve, Update, and Delete for transactional data management systems|
|Data Architecture|It is a discipline of rules, policies, and models that define what data to collect, how to use it, where to store it, and how to integrate distributed and heterogeneous systems separated in silos|
|Data artifacts|Data Dictionary, Data Model, Data Flows, Data Stewardship, Dimensional Model, Data Sharing Agreement|
|Data dictionary|A data dictionary contains information (metadata) about the elements, names, attributes, and definition related to the data in a database|
|Data flow diagram|Represent a flow of data through a subcomponent of, or the entirety of, a process or a system.|
|Data tuple|Related data elements such as a record in a database|
|DDL|Data Definition Language, such as creating database objects|
|Dimension table|table that is descriptive key information, which contains nontransactional data used in OLAP system|
|Dimensional modeling|Using star schema or snowflake schemas, create a relationship among dimension and fact tables|
|Logical models|Represent business concepts within a relationship diagram|
|Meta database|At the highest of levels, it is a database model for metadata management.|
|Metadata|Data about data. Information related to the contents, format, location, size, etc|
|OLAP|Online Analytical Processing used for understanding the patterns|
|OLTP|Online Transaction Processing built on sound relational database systems|
|Reporting|Accessing and querying the data to find insights, trends, analysis, and other information|
|Row-based storage|The entire ROW of data is stored as one chunk. The first column of a given row will be next to the last column of the previous row|
|Silo|physical or logical separation of data without any relationship with other data sets|
|Single Version of Truth|Some business terms and rules have multiple meanings when there is a data dictionary. With a standard dictionary, business vocabulary can have a single version, hence data can have a single version, no matter who looks at it.|
|Stewardship|Accountability and responsibility for data assets and processes that ensure effective control and access.|
|Tribal knowledge|Undocumented information or knowledge that is known to people, who are experienced doing a particular task with any written documentation|


|Ad Hoc loading|In emergency situations, when automation is not available, use this technique|
|---|---|
|Bulk Ingestion|Ingesting large amounts of data at intervals|
|Business Rules|Rules that are in place to manage access, ingestion, reporting, and updating of data|
|Continuous ingestion|Ingesting data in an ongoing manner, such as in real-time|
|Ingestion|Absorbing the incoming data at any speed at any volume|
|Metadata Schema|Data about data. Describes tables, columns, and business rules of all schemas|
|One Source Once Schema|In the staging area, it is easy to manage with one scheme for one source system.|
|Pull|In batch processing systems, data is being pulled on scheduled times|
|Push|In real-time streaming systems, data being pushed to downstream systems as and when it is available.|
|Schema|Logically group of tables, views, functions, stored procedures, and security roles|
|Separation of Concerns|Divide and conquer makes us think and solve data problems in a smaller context|
|Staging|An intermediate storage area before transforming and cleansing of data|
|Yottabyte|1000 Zettabytes|
|Zettabyte|1000 exabytes|

**ODS**: An Operational Data Store is a centralized database that provides a current/recent "snapshot" of the data from all ingested transactional systems. It is especially used for operational reporting. It allows organizations to combine data from the original format, even if different, from various external and internal sources into a single centralized location, which provides access for business reporting.

**Data dictionary**: Table(s) of names, definitions, characteristics, and attributes about all data elements that are being ingested or used in a database,

**Data flow**: Shows the transfer(flow) of information from one system to another system. Could also be between components of the same system.

Metadata: "Data about data." Data and descriptions about data that provide meaningful information about all data in a system. It is used to summarize the source, descriptions, use, and any other information about data.

**Normalization**: "Organizing data in a database." This can include creating tables with relationships between those tables based on encoded rules. These rules protect data and eliminate(reduce) redundancy and inconsistency.

**Data anomaly:** Inconsistencies in the data stored in a database. These are especially important on the initial data ingestion and during updates. Anomalies must be addressed to avoid inconsistency or incorrect data or reporting.

**Ad-hoc** SQL custom queries Queries that are created on the fly to obtain very specific data by combining multiple tables of data into one (usually large) query. Can we one-time usage.

**Historical data lineage:** Information that includes data (source)origin, what happens to it during ingestion or upstream conversions or transformations., and finally where it moves over time as part of the system. It is metadata. S**standard** queries: Common queries that are typically used over and over.

**Bulk loading:** The act of loading large amounts of (usually transactional) data into a database in a short period of time, in many cases by inserting rows one at a time.

**Ingestion**: The process of bringing data from another source into a new location, either internally or externally. This can be at the initial data upload or ongoing updates.

Use a **calculated column** when you want to evaluate each single row

Use a **measure** when you want to aggregate multiple rows of data