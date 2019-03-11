Query table's partitions:
```sql
SELECT o.name, p.partition_number, p.rows, p.*
FROM sys.partitions p
INNER JOIN sys.objects o ON p.object_id = o.object_id
WHERE o.name = '<TABLE_NAME>'
ORDER BY o.name, p.partition_number
```
