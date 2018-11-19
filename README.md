# Oracle DBA
## I. Managing Tablespaces And Datafiles
### Create tablespace using commandline on windows:
  1. login to sql-plus
  2. using command line:
```markdown
create tablespace ica_lmts 
datafile 'E:\u02\oracle\ica\ica.dbf' 
size 50m 
extent management local autoallocate;
```
  - MANAGEMENT LOCAL: track all extent information in the tablespace itself by using bitmaps
  - AUTOALLOCATE: the tablespace to be system managed with a minimum extent size of 64K
  - UNIFORM: The alternative to AUTOALLOCATE is UNIFORM. You can specify that size in the SIZE clause of UNIFORM. If you omit SIZE, then    the default size is 1M. 
 ```markdown
CREATE TABLESPACE ica_lmt 
DATAFILE 'E:\u02\oracle\ica\ica.dbf' 
SIZE 50M 
EXTENT MANAGEMENT LOCAL UNIFORM SIZE 256K; 
```
Create Dictionary Managed Tablespace
 ```markdown
CREATE TABLESPACE ica_lmt 
DATAFILE 'E:\u02\oracle\ica\ica.dbf' 
SIZE 50M 
EXTENT MANAGEMENT DICTIONARY;
```
### Create big tablespace:
```markdown
CREATE BIGFILE TABLESPACE ica_bigtbs  
DATAFILE 'E:\u02\oracle\ica\ica.dbf' 
SIZE 50G;
```
