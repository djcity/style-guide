# DJcity SQL Style Guide
Table of Contents
1. Naming Conventions
2. Locking
3. Selecting
4. Permissions

#### Naming Conventions
- example: usp_API_RecordListGet
type:
- usp (user stored proc)
- udf (user definted function)
app:
- API
- SSIS
- AM (admin)
- DJC (djcity.com)
function (What the function is for and what the function does.  see below examples)
- RecordListGet
- RecordDetailUpdate
- RecordDetailGet
- RecordDetailInsert
- CustomerAPIPasswordGet
- etc...

#### Locks
- Instead of using “with nolock” on each table, you can just put this in the beginning of the stored procedure and it applies nolock to all tables in that proc:
set transaction isolation level read uncommitted

#### Selecting
- Please don’t use “select * from …“.  Always specify the column names “select rid, title, name from …“.

#### Permisions
- Please don’t give any select permission to users on tables.  Users should only have permission on execute for stored procedures and if necessary, some functions.
