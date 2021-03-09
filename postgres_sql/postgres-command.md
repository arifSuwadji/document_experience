# Command Postgres
```
login postgre sql
	psql -U postgres
	
show database
	\l
create database
	CREATE DATABASE namadatabase
connect database
	\c database
show tables
	\dt
show structur tables
	\d table
create type
	create type nama_tipe
check type
	\dT or \dT+
create table
	CREATE TABLE nama_table
query schema
	select column_name, data_type from information_schema.columns where table_name = 'umum';
rename type
	ALTER TYPE electronic_mail RENAME TO email;
dump database only data
	pg_dump -U postgres --data-only --column-inserts spdmlk > data_spdmkl.sql
	
get primary key
	SELECT               
  pg_attribute.attname, 
  format_type(pg_attribute.atttypid, pg_attribute.atttypmod) 
FROM pg_index, pg_class, pg_attribute, pg_namespace 
WHERE 
  pg_class.oid = 'cabang'::regclass AND 
  indrelid = pg_class.oid AND 
  nspname = 'public' AND 
  pg_class.relnamespace = pg_namespace.oid AND 
  pg_attribute.attrelid = pg_class.oid AND 
  pg_attribute.attnum = any(pg_index.indkey)
 AND indisprimary
 
if null mysql
select coalesce(max(no),0) as nomor_selanjutnya from surat;

DROP TABLE nomor_penjemputan;
DROP TABLE nomor_mejatimbang;

CREATE EXTENSION IF NOT EXISTS pgcrypto;

ALTER TABLE table_name 
RENAME COLUMN column_name TO new_column_name;

ALTER TABLE assets 
ALTER COLUMN name TYPE VARCHAR;

CREATE TABLE detail_biaya_kirim (
    id_suratpengiriman integer NOT NULL REFERENCES surat_pengiriman (id),
    kategori integer NOT NULL REFERENCES kategori_kiriman (id),
    additional_data jsonb NOT NULL
);


\pset pager off

pg_dump -t table -s
```