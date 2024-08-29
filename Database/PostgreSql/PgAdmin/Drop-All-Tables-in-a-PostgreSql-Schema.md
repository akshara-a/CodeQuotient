# Drop all tables in a PostgreSQL schema

``` sql
DO $$
DECLARE
    r RECORD;
BEGIN
    FOR r IN (SELECT tablename FROM pg_tables WHERE schemaname = 'public') LOOP
        EXECUTE 'DROP TABLE IF EXISTS public."' || r.tablename || '" CASCADE';
    END LOOP;
END $$;
```

Notes- 
- Database: This is the highest level in the hierarchy. A database is a collection of data organized in a structured way. It can contain multiple schemas and is essentially a container for the data.
- Schema: A schema is a subset within a database. It provides a way to logically group tables and other database objects like views, indexes, and procedures. Schemas help manage and organize database objects within a database, often used to separate different areas of data or to control access.
- Table: A table is a basic unit within a schema. It stores data in rows and columns and is where the actual data is kept. Tables are organized within schemas, and schemas are organized within databases.
- Database is the superset of Schema.
- Schema is the superset of Table.
