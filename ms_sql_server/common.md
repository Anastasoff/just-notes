### Fast rows count
```sql
SELECT [Rows_Count] = SUM(st.row_count)
FROM sys.dm_db_partition_stats st
WHERE object_id = OBJECT_ID('[<SCHEMA>].[<TABLE_NAME>]') AND index_id < 2
```
#### References:
[MSDN - sys.dm_db_partition_stats](https://docs.microsoft.com/en-us/sql/relational-databases/system-dynamic-management-views/sys-dm-db-partition-stats-transact-sql)

### Rename table
```sql
EXEC sp_rename '<SCHEMA>.<TABLE_NAME>', '<NEW_TABLE_NAME>'
```
#### References:
[MSDN - sp_rename](https://docs.microsoft.com/en-us/sql/relational-databases/system-stored-procedures/sp-rename-transact-sql)
