# Tarea en Clase Semana 8
## Función Count
### Creación de la tabla
```mysql
CREATE TABLE IF NOT EXISTS client (
id SERIAL,
nui VARCHAR(10) NOT NULL,
fullname VARCHAR(100) NOT NULL,
phone VARCHAR(10) NOT NULL,
type_of_client VARCHAR(5) DEFAULT 'BASIC',
city VARCHAR(50),
credit_limit DECIMAL (7,2),
PRIMARY KEY(id)
);
```
<img src="./capturas/1.jpg" alt="sentencia"/>

### Inserción de Datos

```mysql
-- 10 Datos con valores aleatorios
INSERT INTO client (nui, fullname, phone, type_of_client, city, credit_limit) 
VALUES 
('1234567890', 'Juan Pérez', '0912345678', 'BASIC', 'Quito', 1000.00),
('0987654321', 'María García', '0909876543', 'VIP', 'Guayaquil', 1500.00),
('5678901234', 'Luis Rodríguez', '0956789012', 'BASIC', 'Cuenca', 2000.00),
('4567890123', 'Ana Martínez', '0945678901', 'VIP', 'Manta', 1200.00),
('2345678901', 'Pedro López', '0923456789', 'BASIC', 'Quito', 1800.00),
('3456789012', 'Laura González', '0934567890', 'BASIC', 'Guayaquil', 1300.00),
('6789012345', 'Carlos Sánchez', '0967890123', 'VIP', 'Cuenca', 1600.00),
('7890123456', 'Sofía Fernández', '0978901234', 'BASIC', 'Manta', 1400.00),
('8901234567', 'Miguel Pérez', '0989012345', 'BASIC', 'Quito', 1700.00),
('9012345678', 'Elena Ramírez', '0990123456', 'VIP', 'Guayaquil', 1100.00);


-- 5 Datos con valores aleatorios pero sin teléfono
INSERT INTO client (nui, fullname, type_of_client, city, credit_limit) 
VALUES 
('3456789012', 'Laura González', 'BASIC', 'Guayaquil', 1300.00),
('6789012345', 'Carlos Sánchez', 'VIP', 'Cuenca', 1600.00),
('7890123456', 'Sofía Fernández', 'BASIC', 'Manta', 1400.00),
('8901234567', 'Miguel Pérez', 'BASIC', 'Quito', 1700.00),
('9012345678', 'Elena Ramírez', 'VIP', 'Guayaquil', 1100.00);
```
## 1. Contar registros existentes en el campo "fullname"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT ()** pasandole como parametro el campo "*fullname*"
![image](https://github.com/Davidacb1617/Relational_Model_Events/assets/146010796/7a8fcdb5-1e24-4b2f-849f-3ade498da148)
## 2. Contar registros existentes en el campo "phone"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT ()** pasandole como parametro el campo "*phone*"
![image](https://github.com/Davidacb1617/Relational_Model_Events/assets/146010796/b78f95c3-21c9-4c84-b635-05c536186c75)
## 3. Contar registros existentes en el campo "fullname" y "phone"
Para mostrar todos los registros existentes en los campos, usamos la función **COUNT ()** pasandole como parametro los campos "*phone*" y "*fullname*"
![image](https://github.com/Davidacb1617/Relational_Model_Events/assets/146010796/953ac0b9-8d13-4a45-990b-067aef91fd4c)
## 4. Contar registros existentes en el campo "phone", "fullname" y todos los registros de la tabla
Para mostrar todos los registros existentes en los campos, usamos la función **COUNT ()** pasandole como parametro los campos "*phone*", "*fullname*" y "**\***" para obtener todos los registros dentro de la tabla
![image](https://github.com/Davidacb1617/Relational_Model_Events/assets/146010796/32605acd-f088-41ca-93c1-ee293f931d64)
## 5. Contar registros existentes en el campo "city"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT ()** pasandole como parametro el campo "*city*"
![image](https://github.com/Davidacb1617/Relational_Model_Events/assets/146010796/b56bcce5-af27-467d-bcc0-1fcc239d7e6d)
## 6. Contar todas las ciudades existentes en el campo "city"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT (DISTINCT)** pasandole como parametro el campo "*city*". Esto lo hicimos para obtener las ciudades que existen en los registros, para que no se repita la ciudad
![image](https://github.com/Davidacb1617/Relational_Model_Events/assets/146010796/07dcf765-fbfc-475e-b093-f76cee1a574c)


