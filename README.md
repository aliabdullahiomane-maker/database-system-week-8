# DATABASE WEEK 8 — MySQL Database Backup

## Student Information

- Name: Ali Abdullahi
- GitHub Username: aliabdullahiomane-maker
- Repository: DATABASE-WEEK-8
- Date: 19 November 2026

## Assignment Overview

This assignment demonstrates how to back up all databases on a MySQL server using the `mysqldump` command-line utility.

## Command Used

```cmd
"C:\Program Files\MySQL\MySQL Server 8.0\bin\mysqldump.exe" --all-databases --user=root --password > all_databases_backup.sql
```

## Command Explanation

| Option | Purpose |
|---|---|
| `mysqldump` | MySQL command-line tool used to create a logical database backup |
| `--all-databases` | Exports all databases on the MySQL server |
| `--user=root` | Connects to MySQL using the `root` username |
| `--password` | Prompts the user to enter the MySQL password securely |
| `> all_databases_backup.sql` | Saves the backup output in a file named `all_databases_backup.sql` |

## Backup File

The backup file is:

```text
all_databases_backup.sql
```

It contains SQL statements that can be used to recreate the databases, tables, and data on another MySQL server.

## Why Backing Up All Databases Is Important

Backing up all databases before migrating to another server is important because it creates a complete copy of every database’s structure and data. If the migration fails, the new server is misconfigured, or data is lost, the backup can be used to restore the original databases.

The backup also ensures that no database is accidentally left behind during migration. The `all_databases_backup.sql` file contains SQL commands that can recreate the databases and reload their data on the destination server.

## How to Restore the Backup

To restore the backup on another MySQL server, use a command such as:

```cmd
mysql --user=root --password < all_databases_backup.sql
```

MySQL will prompt for the `root` password and restore the databases contained in the backup file.

## Conclusion

The MySQL backup was successfully created using `mysqldump`. The backup file, `all_databases_backup.sql`, is included in this repository as evidence that all databases were backed
