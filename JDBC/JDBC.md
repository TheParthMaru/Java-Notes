# JDBC

- Stands for Java Database Connectivity.
- JDBC API is used to connect a java program with wide ranges of databases.
- JDBC API contains a set of classes and interfaces to query database through Java.
- A JDBC driver is a concrete implementation of the JDBC API.

## ODBC

- Stands for Open Database Connectivity.
- Standard API for accessing DBMS.
- Aim was to make it independent of any DBMS and OS.
- The ODBC driver is platform dependent which depends on the native libraries of the underlying OS on which the JVM is running.

## Types of drivers

### 1. Type-1 Driver (JDBC-ODBC Bridge Driver)

- It uses ODBC driver to connect to the DB.
- It converts JDBC method calls into ODBC function calls.
- Also called as Universal Driver because it can connect to any DB.

**Advantages**

- We can access any DB for which the ODBC driver is installed.

**Disadvantages**

- ODBC driver needs to be installed on client's machine.
- Performance is slow because calls go through the JDBC bridge to the ODBC driver and then to the native database connectivity interface.
- No support for Java 8 version.
- The data transferred through this driver is not secured.
- Portability issue because we cannot access specific database functionalities.

### 2. Type-2 Driver (Native-API Driver)

- It uses the client-side libraries of the database.
- It converts JDBC method calls into native machine calls of the database API.
- Not entirely written in Java.

**Advantages**

- Better performance than Type-1 driver.

**Disadvantages**

- Driver needs to be installed on each client machine.
- Vendor client library also needs to be installed on each client machine.
- Not all databases have client-side library.
- Platform dependent driver.

### 3. Type-3 Driver (Network protocol driver)

- Uses middleware (application server) that converts JDBC calls directly or indirectly into vendor specific DB protocol.
- Fully written in Java.

**Advantages**

- No client side library is required.
- Communication between client and middleware server is database independent.
- A single driver can handle any database, provided the middleware supports it.

**Disadvantage**

- Network support is required on client machine.
- Requires database specific coding to be done in the middle tier which results in costly maintenance of network protocol.

#### 4. Type-4 Driver (Thin Driver)

- Converts JDBC calls directly into the vendor specific database protocol.
- Fully written in Java to achieve platform independence.

**Advantages**

- Better performance than all other drivers.
- No software required in client or server side.

**Disadvantages**

- Drivers are DB specific.
