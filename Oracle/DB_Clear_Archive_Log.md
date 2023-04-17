# Oracle DB: Clear Archive Log

## Using RMAN

Before deleteing the archive log, we may first want to know the below information.

Archive Log Location:

    DBHost$ sqlplus / as sysdba
    SQLPLUS> archive log list;

To proper delete the archive log, we would connect to the target DB through the Oracle Service Name, which can be find in the Database with the query:

    SELECT * FROM GLOBAL_NAME;

> All the below commands also required DB storage device to have available volume as audit log and trails need to be created using RMAN

Connect to the target DB with the either one of the following command:

    // Using Operating System Authentication
    rman target /

Crosscheck the archive log:

    RMAN> crosscheck archivelog all;
    
Expired archive log can be checked using the following:
    
    RMAN> list expired archivelog all;

To delete the expired archive log:

    RMAN> delete noprompt expired archivelog all;

## Rerference
1. https://dba.stackexchange.com/questions/118686/right-way-to-delete-the-archive-oracle
2. http://raafat.tawasol.net/how-to-delete-archivelog-using-rman-in-oracle/
3. https://stackoverflow.com/questions/22399766/how-to-find-oracle-service-name
4. https://docs.oracle.com/cd/A97630_01/server.920/a96566/rcmcnctg.htm#443912
