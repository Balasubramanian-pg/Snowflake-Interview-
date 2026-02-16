# Snowflake-Interview
# Snowflake Interview Questions
### 181 Technical & Practical Questions (Non-SQL) Across 16 Categories

---

## 1. Architecture & Core Concepts

1. Explain Snowflake's multi-cluster shared data architecture and how it differs from traditional data warehouse architectures.
2. What are the three main layers of Snowflake's architecture? Describe each layer's role and responsibilities.
3. How does Snowflake's separation of storage and compute enable independent scaling?
4. What is a Virtual Warehouse in Snowflake? How does it differ from a traditional compute cluster?
5. Explain the concept of 'Snowgrid' and how Snowflake supports multi-cloud deployments.
6. What is the Snowflake Cloud Services layer? What functions does it perform?
7. How does Snowflake handle metadata management and what role does it play in query execution?
8. What is the difference between Standard, Enterprise, Business Critical, and VPS editions?
9. Explain how Snowflake's columnar storage format works and why it is efficient for analytical workloads.
10. What is micro-partitioning in Snowflake? How does it differ from traditional partitioning?

---

## 2. Virtual Warehouses & Compute

11. What are the different sizes of Snowflake Virtual Warehouses and how do they affect performance and cost?
12. Explain the concept of auto-suspend and auto-resume for Virtual Warehouses. When would you configure each?
13. What is a multi-cluster warehouse (MCW) in Snowflake? When would you use it over a standard warehouse?
14. Describe the difference between Maximized and Auto-Scale modes for multi-cluster warehouses.
15. How does Snowflake handle query queuing, and what strategies can reduce queue wait times?
16. What is warehouse credit consumption? How does Snowflake calculate costs for warehouse usage?
17. Explain how warehouse caching works and the difference between local disk cache and result cache.
18. What is a Snowpark-optimized warehouse? When should you use it instead of a standard warehouse?
19. How do you monitor warehouse utilization and identify performance bottlenecks using Snowflake's UI or system views?
20. What best practices do you follow for right-sizing Virtual Warehouses to balance performance and cost?

---

## 3. Data Loading & Ingestion

21. What is a Snowflake Stage and what are the different types available (Internal vs. External)?
22. Explain the COPY INTO command. What options and transformations does it support?
23. What file formats does Snowflake support for data loading, and which format is most efficient?
24. What is Snowpipe and how does it enable continuous, automated data ingestion?
25. How does Snowpipe's event-driven loading work with cloud storage (S3, GCS, Azure Blob)?
26. What is the difference between bulk loading and continuous loading in Snowflake?
27. How do you handle semi-structured data (JSON, Avro, Parquet, ORC) during ingestion?
28. What are file format objects in Snowflake and why should you use them instead of inline options?
29. How do you load data from an external stage without copying it into Snowflake storage?
30. Describe how you would set up an end-to-end pipeline using Snowflake Tasks and Streams for incremental loading.
31. What strategies do you use to maximize throughput when loading large files into Snowflake?
32. How do you monitor load jobs and troubleshoot failed COPY INTO operations?

---

## 4. Data Sharing & Collaboration

33. What is Snowflake Secure Data Sharing and how does it work without copying data?
34. Explain the difference between a Data Provider and a Data Consumer in Snowflake's sharing model.
35. What is the Snowflake Marketplace? How can organizations publish or consume data products?
36. What are Data Exchange and Private Exchange in Snowflake? How do they differ from the public Marketplace?
37. How do you create a Share and grant access to specific databases, schemas, and tables?
38. Can you share data with non-Snowflake users? What limitations apply?
39. What is a Listing in Snowflake's Data Cloud ecosystem?
40. How does cross-cloud and cross-region data sharing work in Snowflake?
41. What security considerations must you account for when setting up data sharing?
42. Explain how Snowflake handles reader accounts and when you would use them.

---

## 5. Security & Access Control

43. Explain Snowflake's Role-Based Access Control (RBAC) model and how roles are structured hierarchically.
44. What is the difference between Discretionary Access Control (DAC) and RBAC in Snowflake?
45. What are system-defined roles in Snowflake (ACCOUNTADMIN, SYSADMIN, SECURITYADMIN, USERADMIN, PUBLIC)? When would you use each?
46. How do you implement column-level security in Snowflake?
47. What are Dynamic Data Masking policies and how do you apply them to sensitive columns?
48. What is Row Access Policy in Snowflake? Provide an example use case.
49. How does Snowflake support multi-factor authentication (MFA)?
50. Explain OAuth and SAML 2.0 integration in Snowflake for federated authentication.
51. What is a network policy in Snowflake and how do you restrict access by IP address?
52. How does Snowflake encrypt data at rest and in transit?
53. What is Tri-Secret Secure (TSS) and how does it provide an additional layer of encryption control?
54. How do you audit user activity in Snowflake and what system views provide access control information?

---

## 6. Performance Optimization & Query Tuning

55. What is the Snowflake Query Profile and how do you use it to diagnose slow queries?
56. Explain the concept of pruning in Snowflake and how it improves query performance.
57. What are Clustering Keys in Snowflake? When should you add them to a table?
58. What is Automatic Clustering? How does it differ from manually-defined clustering?
59. How does the Result Cache work in Snowflake? What conditions must be met for it to be used?
60. What is the Local Disk Cache (Warehouse Cache) and how long does it persist?
61. How do you detect and resolve data skew in Snowflake?
62. What is the difference between UNION and UNION ALL in terms of performance in Snowflake?
63. How does Snowflake handle join optimization? What types of joins perform best?
64. Describe strategies for optimizing Snowpipe throughput and reducing latency.
65. How do you use EXPLAIN or system functions to analyze query execution plans?
66. What is the impact of file size on data loading and query performance? What is the optimal file size?

---

## 7. Streams & Tasks

67. What is a Snowflake Stream and how does it implement Change Data Capture (CDC)?
68. What are the different types of Streams in Snowflake (Standard, Append-Only, Insert-Only)?
69. Explain the concept of offset and staleness in Snowflake Streams.
70. How does a Task interact with a Stream to process incremental changes?
71. What is a Task Tree (DAG) in Snowflake and how do you build multi-step pipelines?
72. What scheduling options are available for Snowflake Tasks?
73. How do you handle errors and implement retry logic in Snowflake Tasks?
74. What system views can you query to monitor Task run history and Stream metadata?
75. What happens to a Stream if it is not consumed before the data retention period expires?
76. How do Streams work with Materialized Views versus regular views?

---

## 8. Time Travel & Fail-Safe

77. What is Snowflake Time Travel? How many days of time travel are supported across different editions?
78. How do you query historical data using the AT and BEFORE clauses in Snowflake?
79. How can you use Time Travel to restore a dropped or modified table?
80. What is the UNDROP command and what objects does it support?
81. What is the difference between Time Travel and Fail-Safe in Snowflake?
82. How do Time Travel and Fail-Safe affect storage costs?
83. How do you clone a table at a historical point in time using Time Travel?
84. What are the limitations of Time Travel in Snowflake (e.g., temporary tables, transient tables)?
85. How do you set the Time Travel retention period at the database, schema, or table level?
86. What happens to Time Travel data when a table is dropped? How do you prevent accidental loss?

---

## 9. Semi-Structured & Unstructured Data

87. What is the VARIANT data type in Snowflake and what formats does it support?
88. How do you query nested JSON data stored in a VARIANT column using dot notation and bracket notation?
89. What is the FLATTEN function in Snowflake and how do you use it to expand arrays?
90. How do you use LATERAL JOIN with FLATTEN to unnest arrays within VARIANT columns?
91. What are OBJECT_CONSTRUCT and ARRAY_CONSTRUCT functions? Provide an example.
92. How does Snowflake store and index semi-structured data for efficient querying?
93. What is the difference between PARSE_JSON, TRY_PARSE_JSON, and PARSE_XML?
94. How do you load and query Parquet or ORC files as external tables?
95. What are the limitations of the VARIANT data type in terms of size and nesting depth?
96. How can you optimize queries on VARIANT columns using schema detection or virtual columns?

---

## 10. Cloning & Zero-Copy Cloning

97. What is Zero-Copy Cloning in Snowflake? How does it work under the hood?
98. What objects can be cloned in Snowflake (tables, schemas, databases, etc.)?
99. What are the storage cost implications of Zero-Copy Cloning?
100. How do clones behave when the source data is modified? Explain the copy-on-write mechanism.
101. How can Zero-Copy Cloning be used for dev/test/staging environments?
102. Can you clone a clone in Snowflake? What are the implications?
103. What is the difference between cloning a table with and without Time Travel?
104. How do privileges and grants behave when a database or schema is cloned?
105. What are the limitations of cloning in Snowflake (e.g., external tables, pipes)?
106. How would you use cloning in a CI/CD pipeline for data engineering?

---

## 11. Snowpark & Developer Features

107. What is Snowpark and what programming languages does it currently support?
108. How does Snowpark differ from using Snowflake's SQL interface?
109. What is a Snowpark DataFrame and how does it compare to a pandas DataFrame?
110. Explain the concept of lazy evaluation in Snowpark DataFrames.
111. What are User-Defined Functions (UDFs) in Snowflake? What languages can you write UDFs in?
112. What is a Vectorized UDF and when would you use it over a scalar UDF?
113. What are User-Defined Table Functions (UDTFs) and how do they differ from scalar UDFs?
114. What are Stored Procedures in Snowflake? What languages are supported for writing them?
115. What is the caller's rights vs. owner's rights model for Stored Procedures?
116. What are External Functions in Snowflake and when would you use them?
117. How does Snowflake support machine learning workflows through Snowpark ML?
118. What is Streamlit in Snowflake (SiS) and how does it integrate with Snowflake data?

---

## 12. Governance, Compliance & Data Management

119. What is Snowflake Horizon and what governance capabilities does it provide?
120. What are Tags in Snowflake? How do you use them for data governance?
121. How does Snowflake implement data lineage tracking?
122. What is the Access History feature in Snowflake and what use cases does it address?
123. How do you implement PII (Personally Identifiable Information) protection in Snowflake?
124. What is the Object Dependencies view in Snowflake and how is it useful?
125. How do Snowflake Policies (Masking, Row Access) support compliance with GDPR and HIPAA?
126. What is a Classification Policy in Snowflake and how does it automate sensitive data detection?
127. How does Snowflake support data quality monitoring through built-in features?
128. What is the INFORMATION_SCHEMA in Snowflake and what types of metadata can you retrieve from it?

---

## 13. Cost Management & Billing

129. What are Snowflake Credits and how are they consumed by different Snowflake services?
130. What is the difference between compute cost and storage cost in Snowflake?
131. How do you set up Resource Monitors to control credit consumption?
132. What actions can a Resource Monitor trigger when thresholds are hit (Notify, Suspend, Suspend Immediately)?
133. How do Budgets in Snowflake differ from Resource Monitors?
134. What tools and views does Snowflake provide for analyzing cost and usage?
135. How does Snowflake price on-demand vs. pre-purchased capacity?
136. How can you reduce Snowflake costs through warehouse optimization strategies?
137. What is the impact of Time Travel retention settings on storage costs?
138. How do you estimate and project Snowflake spending for a growing workload?
139. What is the Cost Management UI in Snowflake and what reports does it provide?

---

## 14. Replication & Disaster Recovery

140. What is Snowflake database replication? How does it differ from data sharing?
141. What is a Replication Group and what objects does it support for replication?
142. What is a Failover Group and how does it support business continuity?
143. Explain the concepts of primary and secondary databases in Snowflake replication.
144. What is the RPO (Recovery Point Objective) and RTO (Recovery Time Objective) for Snowflake failover?
145. How do you promote a secondary database to primary in a failover scenario?
146. What are the cost implications of Snowflake database replication?
147. How does cross-region and cross-cloud replication differ in terms of latency and cost?
148. What objects and features are NOT supported by Snowflake replication?
149. How do you monitor replication lag and ensure secondary databases are up to date?

---

## 15. External Tables & Data Lake Integration

150. What is an External Table in Snowflake and when would you use it over a standard table?
151. How do External Tables access data stored in cloud storage (S3, GCS, Azure)?
152. What is a directory table and how does it provide metadata about files in a stage?
153. How do you refresh metadata for an External Table?
154. What are Iceberg Tables in Snowflake and how do they support open table formats?
155. What is the difference between Snowflake-managed Iceberg tables and externally managed ones?
156. How do External Tables perform compared to native Snowflake tables and when is each appropriate?
157. What is schema detection (INFER_SCHEMA) and how does it help when loading external data?
158. How do you partition External Tables to improve query pruning?
159. What is a Hive Metastore-compatible External Table in Snowflake?

---

## 16. Real-World Scenarios & Best Practices

160. Describe a situation where you optimized a poorly performing Snowflake pipeline. What steps did you take?
161. How would you design a multi-tenant Snowflake environment to isolate workloads and control costs?
162. What is your approach for migrating an on-premises data warehouse to Snowflake?
163. How do you handle schema evolution (adding/removing columns) in a Snowflake pipeline?
164. What strategies do you use to implement a medallion architecture (Bronze/Silver/Gold) in Snowflake?
165. How would you design a near-real-time data pipeline using Snowpipe and Streams?
166. Describe how you would implement idempotent data loading in Snowflake to avoid duplicates.
167. How would you implement a role hierarchy and access control model for a large enterprise Snowflake deployment?
168. What is your approach for capacity planning and forecasting Snowflake credit consumption?
169. How do you integrate Snowflake with dbt (data build tool) in a modern data stack?
170. Describe how you would handle slowly changing dimensions (SCDs) using Snowflake features.
171. What is your testing and validation strategy for Snowflake data transformations?
172. How do you approach monitoring and alerting for Snowflake pipelines in production?
173. How would you set up a dev/test/prod environment separation in Snowflake?
174. Describe how you would troubleshoot a sudden spike in Snowflake credit consumption.
175. How do you handle late-arriving data in a Snowflake-based data pipeline?
176. What is your strategy for implementing data versioning and rollback in Snowflake?
177. How would you architect a Snowflake solution for a company with strict data residency requirements?
178. Describe your approach for performance testing a Snowflake data platform before going live.
179. How would you implement a data mesh architecture using Snowflake as the underlying platform?
180. What governance policies and standards do you enforce when onboarding a new team to Snowflake?
181. How do you document Snowflake data assets and ensure discoverability for analysts?
# Snowflake Interview Questions — Set 2
### 180 New Technical & Practical Questions (Non-SQL, Non-Duplicate)

---

## 1. Account & Organization Management

1. What is a Snowflake Organization and how does it differ from a Snowflake Account?
2. How do you manage multiple Snowflake accounts under a single Organization?
3. What is ORGADMIN role and what privileges does it grant?
4. How do you move a Snowflake account between cloud providers or regions within an Organization?
5. What is account-level vs. organization-level billing in Snowflake?
6. How do you enable and manage cross-account features using the Organization object?
7. What is the purpose of the SHOW ORGANIZATION ACCOUNTS command?
8. How does Snowflake handle account identifiers — what formats are supported?
9. What is a locator-based vs. account name-based connection URL in Snowflake?
10. How do you set organization-wide policies and enforce them across multiple accounts?

---

## 2. Connectivity & Drivers

11. What client drivers and connectors does Snowflake officially support?
12. How does the Snowflake JDBC driver differ from the ODBC driver in terms of use cases?
13. What is the Snowflake Python connector and how does it handle connection pooling?
14. What is the SnowSQL CLI and what are its primary use cases compared to the web UI?
15. How do you configure a Snowflake connection using a private key for key-pair authentication?
16. What is the Snowflake Go driver and when would you use it?
17. How do you connect Snowflake to BI tools like Tableau, Power BI, or Looker?
18. What are the connection parameters you must configure when setting up an ODBC/JDBC connection?
19. How does Snowflake handle connection timeouts and session expiration?
20. What is the Snowflake REST API and what operations does it support?

---

## 3. Snowflake Native App Framework

21. What is the Snowflake Native App Framework and what problem does it solve?
22. How does a Native App differ from a regular Snowflake application or stored procedure?
23. What are the components of a Native App (manifest, setup script, etc.)?
24. How do you publish a Native App to the Snowflake Marketplace?
25. What are the security and permission model constraints when building a Native App?
26. How does a consumer install and configure a Native App in their own Snowflake account?
27. What is the role of the APPLICATION object in the Native App Framework?
28. How do you version and update a Native App without disrupting consumers?
29. What types of Snowflake objects can a Native App create inside a consumer's account?
30. What are the limitations of Native Apps compared to building a full external SaaS product?

---

## 4. Snowflake Cortex AI Features

31. What is Snowflake Cortex and what AI/ML capabilities does it provide natively?
32. What are Cortex LLM Functions (e.g., COMPLETE, SUMMARIZE, SENTIMENT) and how do you invoke them?
33. How does Cortex Search work and what types of queries does it support?
34. What is Cortex Analyst and how does it enable natural language querying of Snowflake data?
35. How do you use the EMBED_TEXT function in Snowflake Cortex for vector embeddings?
36. What is a Cortex Fine-tuning job and when would you use it over a pre-built LLM function?
37. How does Snowflake handle data privacy when using Cortex LLM features?
38. What is the difference between Cortex and Snowpark ML in terms of AI/ML capabilities?
39. How do you build a Retrieval-Augmented Generation (RAG) pipeline using Snowflake Cortex?
40. What are the credit costs associated with Cortex LLM function calls?

---

## 5. Snowflake Marketplace & Data Products

41. What is a Data Product in the context of Snowflake's Data Cloud?
42. How do you create and publish a monetized listing on the Snowflake Marketplace?
43. What are the different listing types on the Snowflake Marketplace (free, paid, personalized)?
44. How does Snowflake handle revenue sharing and billing for paid Marketplace listings?
45. What is a Provider Studio in Snowflake and what tools does it offer data providers?
46. How do you restrict a Marketplace listing to specific consumers or regions?
47. What is a sample dataset and how can it be attached to a Marketplace listing?
48. How do you track usage analytics for your published Marketplace listings?
49. What compliance and legal considerations apply when publishing data to the Marketplace?
50. How do you handle versioning and updates to a published Marketplace data product?

---

## 6. Alerts & Notifications

51. What are Snowflake Alerts and how do they differ from Tasks?
52. How do you create an Alert in Snowflake and what triggers can be configured?
53. What notification integrations does Snowflake support for sending alerts (email, SNS, etc.)?
54. How do you set up an email notification integration in Snowflake?
55. What is the difference between a serverless Alert and a warehouse-powered Alert?
56. How do you chain Alerts with Tasks for complex event-driven workflows?
57. What system views can you query to see Alert execution history and status?
58. How do you implement a data freshness alert using Snowflake's native alerting?
59. What are the limitations of Snowflake Alerts compared to external monitoring tools?
60. How do you use Alerts to detect and notify on data quality issues?

---

## 7. Dynamic Tables

61. What are Dynamic Tables in Snowflake and how do they differ from Materialized Views?
62. How does the target lag parameter control refresh frequency for Dynamic Tables?
63. What is the difference between user-defined lag and downstream lag for Dynamic Tables?
64. How do Dynamic Tables handle incremental refresh vs. full refresh?
65. Can Dynamic Tables depend on other Dynamic Tables? How does Snowflake manage the refresh DAG?
66. What types of transformations are supported in Dynamic Table definitions?
67. How do you monitor Dynamic Table refresh history and identify refresh failures?
68. What are the compute costs associated with Dynamic Tables?
69. When would you choose a Dynamic Table over a Stream+Task pipeline?
70. What are the current limitations of Dynamic Tables (e.g., unsupported features, object types)?

---

## 8. Serverless Features & Compute Models

71. What are Snowflake serverless features and how do they differ from Virtual Warehouse compute?
72. Which Snowflake features use serverless compute (e.g., Snowpipe, Tasks, Alerts, Dynamic Tables)?
73. How are serverless compute credits billed compared to Virtual Warehouse credits?
74. What is the advantage of serverless Tasks over warehouse-powered Tasks?
75. How does Snowflake automatically scale serverless compute resources?
76. What are the trade-offs between serverless and warehouse-based compute for batch workloads?
77. How do you estimate costs for serverless feature usage in Snowflake?
78. What is Snowpark Container Services and how does it extend Snowflake's compute model?
79. How do containers in Snowpark Container Services communicate with Snowflake data?
80. What types of workloads are best suited for Snowpark Container Services?

---

## 9. Search Optimization Service

81. What is the Search Optimization Service (SOS) in Snowflake and what query patterns does it accelerate?
82. How does the SOS differ from clustering keys in terms of use case and implementation?
83. What types of predicates benefit from the Search Optimization Service?
84. How do you enable the Search Optimization Service on a table or specific columns?
85. What are the storage and compute cost implications of enabling SOS?
86. How does SOS handle VARIANT and semi-structured column searches?
87. What is the difference between full-text search and point lookup optimization in SOS?
88. How do you verify whether the SOS is being used for a specific query?
89. When would you NOT use the Search Optimization Service?
90. How do you monitor and manage SOS maintenance overhead?

---

## 10. Materialized Views

91. What is a Materialized View in Snowflake and how does it differ from a regular view?
92. How does Snowflake automatically maintain and refresh Materialized Views?
93. What are the restrictions on queries that can be used to define a Materialized View?
94. How does a query planner decide to use a Materialized View vs. the base table?
95. What happens to a Materialized View when the underlying base table is modified?
96. What are the cost implications of using Materialized Views in Snowflake?
97. How do Materialized Views interact with clustering keys on the base table?
98. Can Materialized Views be defined on external tables or Dynamic Tables?
99. How do you monitor the freshness and maintenance status of a Materialized View?
100. When should you prefer a Dynamic Table over a Materialized View?

---

## 11. Data Quality & Observability

101. What built-in capabilities does Snowflake offer for data observability?
102. How do you implement row count and null-check monitoring natively in Snowflake?
103. What is the DATA_METRIC_FUNCTION object in Snowflake and how does it support data quality?
104. How do you schedule data quality metric evaluations using Snowflake's native features?
105. What system views track data metric function results over time?
106. How does Snowflake's Access History view help with data observability?
107. How do you detect schema drift in incoming data using Snowflake-native approaches?
108. What third-party observability tools integrate natively with Snowflake?
109. How do you implement SLA monitoring for data pipelines using Snowflake Tasks and Alerts?
110. What is the QUERY_HISTORY view and what observability insights can you derive from it?

---

## 12. Table Types & Design

111. What are the four table types in Snowflake (Permanent, Transient, Temporary, External) and when do you use each?
112. How does a Transient table differ from a Permanent table in terms of Fail-Safe and Time Travel?
113. What is a Temporary table in Snowflake and what is its scope and lifecycle?
114. How do table types affect storage costs in Snowflake?
115. What is a hybrid table in Snowflake and what workloads is it optimized for?
116. How does Snowflake Unistore combine transactional and analytical workloads using hybrid tables?
117. What indexing mechanisms do hybrid tables support that regular Snowflake tables do not?
118. How do you design a table schema for optimal pruning and clustering in Snowflake?
119. What are the considerations for choosing between wide tables vs. normalized schemas in Snowflake?
120. How does Snowflake handle NULL values in storage and how do they affect compression?

---

## 13. Integration & Ecosystem

121. How does Snowflake integrate with Apache Kafka using the Kafka Connector?
122. What is the Snowflake Connector for Python and how does it differ from the Snowpark library?
123. How do you integrate Snowflake with Apache Spark using the Snowflake Spark Connector?
124. What is the Snowflake connector for dbt Cloud and how does it manage model execution?
125. How do you integrate Snowflake with Fivetran or Airbyte for ELT pipelines?
126. What is the Snowflake Connector for ServiceNow and what data does it sync?
127. How does the Snowflake Connector for Google Analytics work?
128. How do you use Terraform to manage Snowflake infrastructure as code?
129. What Snowflake-native features support GitOps and version-controlled deployments?
130. How do you integrate Snowflake with orchestration tools like Apache Airflow or Prefect?

---

## 14. Logging, Tracing & Telemetry

131. What is the Snowflake event table and what types of telemetry data does it store?
132. How do you enable logging for Stored Procedures and UDFs in Snowflake?
133. What log levels are supported in Snowflake's logging framework?
134. How do you emit custom trace events from Snowpark code?
135. What is the relationship between an event table and the Snowflake telemetry system?
136. How do you query logs and traces stored in the event table for debugging?
137. How do you set up log and trace data retention policies for event tables?
138. What is the SYSTEM$LOG function and how does it differ from Python's logging module in Snowpark?
139. How do you integrate Snowflake telemetry with external observability platforms like Datadog?
140. What are best practices for structured logging in Snowflake Stored Procedures?

---

## 15. Snowflake on Different Cloud Platforms

141. What are the differences in Snowflake's feature availability across AWS, Azure, and GCP?
142. How does Snowflake leverage cloud-native storage services (S3, Azure Blob, GCS) under the hood?
143. What is PrivateLink in Snowflake and how does it improve network security on each cloud?
144. How do you configure AWS PrivateLink for a Snowflake account?
145. What is the difference between a Snowflake Business Critical account and a standard account in terms of cloud networking?
146. How does Snowflake handle cloud provider outages and what is its SLA?
147. What cloud IAM roles and permissions are required to connect Snowflake to S3 or Azure Blob?
148. How does Snowflake's pricing differ across AWS, Azure, and GCP?
149. What is Snowflake's approach to data sovereignty and compliance certifications (SOC 2, ISO 27001, FedRAMP)?
150. How do you migrate a Snowflake account from one cloud provider to another?

---

## 16. Advanced Performance & Internals

151. How does Snowflake's query optimizer work at a high level?
152. What is the role of statistics in Snowflake's query planning and how are they maintained?
153. How does Snowflake handle spilling to disk and remote storage during query execution?
154. What is the impact of spilling on query performance and how do you reduce it?
155. How does Snowflake implement vectorized execution for analytical queries?
156. What is the difference between compile time and execution time in Snowflake query processing?
157. How does Snowflake handle concurrent read and write operations on the same table?
158. What is optimistic concurrency control in Snowflake and how does it handle write conflicts?
159. How does Snowflake's file pruning work at the micro-partition level during query execution?
160. What are partition overlaps and how do they degrade pruning efficiency?
161. How does Snowflake's columnar compression work and what encoding schemes does it use?
162. What is the purpose of the SYSTEM$CLUSTERING_INFORMATION function?
163. How do you interpret clustering depth and overlap statistics to assess table health?
164. What is adaptive query execution in Snowflake and how does it improve runtime performance?
165. How do you use the QUERY_ACCELERATION_HISTORY view to assess the value of the Query Acceleration Service?

---

## 17. Query Acceleration Service & Specialized Features

166. What is the Query Acceleration Service (QAS) in Snowflake and what query patterns does it target?
167. How does QAS differ from simply increasing warehouse size for performance?
168. How do you enable QAS on a warehouse and what scale factor options are available?
169. How are QAS credits billed and what is the cost model?
170. What types of queries are ineligible for query acceleration?
171. What is the RESULT_SCAN function in Snowflake and how can it be used practically?
172. What is the purpose of the GENERATOR table function in Snowflake?
173. How does Snowflake handle recursive CTEs and what are the depth limitations?
174. What is the TABLESAMPLE feature in Snowflake and when would you use it?
175. How does Snowflake's automatic query rewrites work for Materialized Views?
176. What is the purpose of the SYSTEM$ESTIMATE_QUERY_ACCELERATION function?
177. How do you use the EXPLAIN command output to manually identify inefficiencies?
178. What are the differences between scalar subqueries and correlated subqueries in terms of Snowflake performance?
179. How do window functions perform in Snowflake compared to GROUP BY aggregations for the same result?
180. What is the role of the pruning ratio metric in assessing the efficiency of a Snowflake query?

