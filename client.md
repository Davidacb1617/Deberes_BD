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
<img src="./capturas/TC1.jfif" alt="sentencia1"/>
## 2. Contar registros existentes en el campo "phone"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT ()** pasandole como parametro el campo "*phone*"
<img src="./capturas/TC2.jfif" alt="sentencia2"/>
## 3. Contar registros existentes en los campos "fullname" y "phone"
Para mostrar todos los registros existentes en los campos, usamos la función **COUNT ()** pasandole como parametro los campos "*phone*" y "*fullname*"
<img src="./capturas/TC3.jfif" alt="sentencia3"/>
## 4. Contar registros existentes en los campos "phone", "fullname" y todos los registros de la tabla
Para mostrar todos los registros existentes en los campos, usamos la función **COUNT ()** pasandole como parametro los campos "*phone*", "*fullname*" y "**\***" para obtener todos los registros dentro de la tabla
<img src="./capturas/TC4.jfif" alt="sentencia4"/>
## 5. Contar registros existentes en el campo "city"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT ()** pasandole como parametro el campo "*city*"
<img src="./capturas/TC5.jfif" alt="sentencia5"/>
## 6. Contar todas las ciudades existentes en el campo "city"
Para mostrar todos los registros existentes en este campo, usamos la función **COUNT (DISTINCT)** pasandole como parametro el campo "*city*". Esto lo hicimos para obtener las ciudades que existen en los registros, para que no se repita la ciudad
<img src="./capturas/TC6.jfif" alt="sentencia6"/>


