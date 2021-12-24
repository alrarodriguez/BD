# BD

Pasos para crear la base de datos:

CREATE DATABASE IF NOT EXISTS people_db;
commit;
USE people_db;
commit;

DROP TABLE people_db.people;
CREATE TABLE people_db.people (
	id INT NOT NULL AUTO_INCREMENT,
    fullname VARCHAR(45) NOT NULL,
	identification INT NOT NULL,
	birth VARCHAR(45) NOT NULL,
    PRIMARY KEY(id)
);
commit;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'admin';
flush privileges;

insert into people_db.people (fullname, identification, birth) values ('Alvaro Luis Rodriguez Atunez', 11231323, '29/03/1996');
select * from  people_db.people;
SELECT fullname as fullName, birth, identification FROM people;
truncate table people_db.people;
