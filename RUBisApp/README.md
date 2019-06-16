### Execute following commands:
  * cd /Your_RUBiS_Directory/database
  * $ mysql -u root –password=’Your password’
  * mysql> source rubis.sql;
  * mysql> source categories.sql;
  * mysql> source regions.sql;
  * mysql> GRANT ALL ON rubis.* TO ‘rubis’@’%’ IDENTIFIED BY ‘password’;
  * mysql> GRANT ALL ON rubis.* TO ‘rubis’@’localhost’ IDENTIFIED BY ‘password’;
  * mysql> GRANT ALL ON rubis.* TO 'root@'localhost' IDENTIFIED BY 'password';
  * Execute files: 'generate_categories.awk' and 'generate_regions.awk'
  * $ ./generate_categories.awk ebay_full_categories.txt
  * $ ./generate_regions.awk ebay_regions.txt

### Emulate Client:
run make emulator
