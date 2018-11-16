# Oracle DBA
## I. Managing Tablespaces And Datafiles
### Create tablespace using commandline on windows:
  1. login to sql-plus
  2. using command line:
```markdown
create tablespace ica_lmts datafile 'E:\u02\oracle\ica\ica.dbf' size 50m extent management local autoallocate;
```
