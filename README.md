# BD

Pasos para crear la base de datos:

CREATE DATABASE IF NOT EXISTS personas_db;
commit;
USE personas_db;
commit;

DROP TABLE persona;
CREATE TABLE persona (
	id INT NOT NULL AUTO_INCREMENT,
    nombres VARCHAR(45) NOT NULL,
    apellidos VARCHAR(45) NOT NULL,
	identificacion INT NOT NULL,
	edad VARCHAR(45) NOT NULL,
	birth VARCHAR(45) NOT NULL,
    PRIMARY KEY(id)
);
commit;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'admin';
flush privileges;

insert into personas_db.persona (nombres, apellidos, identificacion, edad, birth) values ('Alvaro Luis', 'Rodriguez Atunez', 11231323, '26', '29/03/1996');
select * from  personas_db.persona;
