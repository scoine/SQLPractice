
## 1. SSIS (SQL Server Integration Services) Roadmap

### Overview
SSIS is a platform for building enterprise-level data integration and transformation solutions, primarily used for Extract, Transform, and Load (ETL) processes.

### Roadmap

#### 1.1 Basic Concepts
- **Overview of SSIS**: What is SSIS? Why is it used?
- **SSIS Architecture**: Package, Task, Container, Data Flow, Control Flow
- **Control Flow vs Data Flow**: Difference between the two.
- **SSIS Package Execution**: How to run, deploy, and schedule packages.
- **SSIS Design Tools**: SQL Server Data Tools (SSDT).

#### 1.2 Data Flow and Control Flow
- **Control Flow Tasks**: Execute SQL Task, File System Task, Data Flow Task.
- **Data Flow Components**: Sources, Destinations, Transformations.
- **Connections**: Creating connections to various sources (SQL Server, flat files, Excel, etc.).
- **Transformations**: Lookup, Merge Join, Data Conversion, Conditional Split, Derived Column, etc.

#### 1.3 Advanced Data Flow Concepts
- **Data Flow Pipeline**: How data flows from Source to Destination.
- **Error Handling**: Using error outputs and logging.
- **Data Quality**: Implementing data validation and cleaning.
- **Package Configurations**: Using XML, SQL Server, environment variables for dynamic configuration.

#### 1.4 SSIS Control Flow Tasks
- **For Loop / For Each Loop**: Iterating over collections.
- **Execute SQL Task**: Running SQL commands.
- **Script Task**: Writing custom logic in C# or VB.
- **File System Task**: File management (copy, delete, move).
- **Send Mail Task**: Sending emails based on conditions.

#### 1.5 SSIS Performance Tuning
- **Data Flow Optimization**: Buffer size, transformations.
- **Parallelism**: Configuring multiple threads for performance.
- **Minimizing Blocking Operations**: Reduce memory usage.
- **Monitoring SSIS Packages**: Using SSISDB, performance counters.

#### 1.6 SSIS Deployment & Scheduling
- **Deploying Packages to MSDB and SSISDB**.
- **SQL Server Agent**: Automating SSIS Package execution.
- **Logging & Error Handling**: Capturing package execution logs.
- **Custom Logging**: Use of custom log providers.

### Problem Statements/Questions for SSIS:
1. How do you handle errors in SSIS while loading data from a flat file into SQL Server?
2. Create an SSIS package to read data from a source (Excel file) and load it into a destination (SQL Server table). Implement error handling and logging.
3. Implement a slowly changing dimension (SCD) type 2 in SSIS.
4. Design an SSIS package to send an email alert if a data load fails.
5. What are the different ways to pass parameters to an SSIS package during execution?
6. Optimize a data flow in SSIS where large datasets are being transferred.
7. Use a lookup transformation to match data from a source to a reference table and apply logic based on matched and unmatched data.

---
