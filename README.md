# DJcity SQL Style Guide
Table of Contents
1. Naming Conventions
2. Locking
3. Selecting
4. Permissions

#### Naming Conventions
- TBD

#### Locks
- Instead of using “with nolock” on each table, you can just put this in the beginning of the stored procedure and it applies nolock to all tables in that proc:
set transaction isolation level read uncommitted

#### Selecting
- Please don’t use “select * from …“.  Always specify the column names “select rid, title, name from …“.

#### Permisions
- Please don’t give any select permission to users on tables.  Users should only have permission on execute for stored procedures and if necessary, some functions.
