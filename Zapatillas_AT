Create database Zapatillas_AT

use Zapatillas_AT

CREATE TABLE Sedes (
id_sede INT IDENTITY (1, 1) PRIMARY KEY,
Telefono_Sede VARCHAR (25),
Email_Sede VARCHAR (50),
Ciudad_Sede VARCHAR (50),
Direccion_sede VARCHAR (50) 
);

Insert into Sedes(Telefono_Sede, Email_Sede, Ciudad_Sede, Direccion_sede)
Values ('111111', 'zapatATmed@gmail.com', 'Medellin', 'Cll 1 #11-1'),
('222222', 'zapatATbog@gmail.com', 'Bogota', 'Cll 2 #22-2'),
('333333', 'zapatATbar@gmail.com', 'Barranquilla', 'Cll 3 #33-3'),
('444444', 'zapatATcal@gmail.com', 'Cali', 'Cll 4 #44-4'),
('555555', 'zapatATcar@gmail.com', 'Cartagena', 'Cll 5 #55-5')

Select * from Sedes

CREATE TABLE Personal (
id_gerente INT IDENTITY (1, 1) PRIMARY KEY,
Nombres_Gerente VARCHAR (50) NOT NULL,
Apellidos_Gerente VARCHAR (50) NOT NULL,
Email_Gerente VARCHAR (50) NOT NULL UNIQUE,
Telefono_Gerente VARCHAR (25),
id_sede INT NOT NULL,
FOREIGN KEY (id_sede) 
REFERENCES Sedes (id_sede) ,
);

Insert into Personal (Nombres_Gerente, Apellidos_Gerente, Email_Gerente, Telefono_Gerente, id_sede)
values ('Ivan', 'Alvis Tijaro', 'ivanalvis@gmail.com', '11111', '1'),
('Hector Hernando', 'Alvis Mendez', 'hectoralvis@gmail.com', '22222', '2'),
('Maria Alexandra', 'Tijaro Rivas', 'alexandratijaro@gmail.com', '33333','3'),
('Ana Maria', 'Alvis Tijaro', 'anaalvis@gmail.com', '44444', '4'),
('Jaime', 'Tijaro Rivas', 'jaimetijaro@gmail.com', '55555', '5')

Select * from Personal

CREATE TABLE Categorias (
	id_categoria INT IDENTITY (1, 1) PRIMARY KEY,
	Nombre_Categoria VARCHAR (50) NOT NULL
);

Insert into Categorias (Nombre_Categoria)
Values ('Correr'), ('Lifestyle'), ('Basketbol'), ('Skateboard')

select * from Categorias


CREATE TABLE Marcas (
	id_Marca INT IDENTITY (1, 1) PRIMARY KEY,
	Nombre_Marca VARCHAR (50) NOT NULL
);

Insert into Marcas (Nombre_Marca)
Values ('Nike'), ('Adidas'), ('Jordan'), ('Vans')

Select * from Marcas

CREATE TABLE Productos (
	id_Productos INT IDENTITY (1, 1) PRIMARY KEY,
	Nombre_Producto VARCHAR (255) NOT NULL,
	id_Marca INT NOT NULL,
	id_Categoria INT NOT NULL,
	Precio DECIMAL (10, 3) NOT NULL,
	FOREIGN KEY (id_categoria) 
        REFERENCES Categorias (id_categoria) ,
	FOREIGN KEY (id_marca) 
        REFERENCES Marcas (id_Marca) 
);


Insert into Productos (Nombre_Producto, id_Marca, id_Categoria, Precio)
values 
--------------------- Nike -------------------------------------------------------
('Air Force 1', 1, 2, 309.900), ('Air Max 90', 1, 1, 420.000),
('Cortez', 1, 1, 295.900), ('Daybreak', 1, 1, 290.000),
('Air Vapormax Plus', 1, 1, 350.000), ('Airmax Penny', 1, 3, 720.000), 
----------------------------------------------------------------------------------

-------------------- Adidas ------------------------------------------------------
('Yeezy', 2, 1, 560.000), ('SuperStar', 2, 2, 320.000),
('Stan Smith', 2, 2, 320.000), ('T-Rex', 2, 1, 350.000),
('CrazyChaos', 2, 2, 295.000), ('OzzweeGo', 2, 2, 420.000),
----------------------------------------------------------------------------------

-------------------- Jordan ------------------------------------------------------
('Air Jordan 1', 3, 3, 430.000), ('Air Jordan VIII', 3, 3, 520.000),
('Air Jordan VI', 3, 3, 520.000), ('Air Jordan XI', 3, 3, 630.000),
('Air Jordan V', 3, 3, 480.000), ('Air Jordan VII', 3, 3, 510.000),
----------------------------------------------------------------------------------

--------------------- Vans -------------------------------------------------------
('Authentic', 4, 4, 310.000), ('Old Skool',4, 4, 330.000),
('Slip On', 4, 2, 350.000), ('Era', 4, 4, 310.000),
('Sk8 Hi',4, 4, 340.000), ('Skull', 4, 4, 315.000)
----------------------------------------------------------------------------------

Select * from Productos  

CREATE TABLE Clientes (
	id_Cliente INT IDENTITY (1, 1) PRIMARY KEY,
	Nombre_Cliente VARCHAR (50) NOT NULL,
	Apellidos_Cliente VARCHAR (50) NOT NULL,
	Telefono_Cliente VARCHAR (25),
	Email_Cliente VARCHAR (50) NOT NULL,
	Ciudad_Cliente VARCHAR (50),
);    


Insert into Clientes (Nombre_Cliente, Apellidos_Cliente, Telefono_Cliente, Email_Cliente, Ciudad_Cliente)
Values ('Jose', 'Gomez Gonzales', 1212323, 'joseg@gmail.com', 'Medellin'),
('Danna', 'Sepulveda Toro', 4215235, 'danna@gmail.com', 'Cali'),
('Estefania', 'Ballesteros Saldarriaga', 554852, 'estefab@gmail.com', 'Medellin'),
('Brayan', 'Ciro Correa', 425341, 'brayanc@gmail.com', 'Bogota'),
('Maria jose', 'Mejia Estrada', 652452, 'majoe@gmail.com', 'Cartagena'),
('Maximiliano', 'Machado varon', 521238, 'maxmv@gmail.com', 'Cartagena'),
('Daniel', 'Ruiz Bernal', 742525, 'danru@gmail.com', 'Barranquilla'),
('Alejandra', 'Jimenez Rios', 1254238, 'alejar@gmail.com', 'Cali'),
('Sofia', 'Lopez Vanegas', 2514624, 'sofial@gmail.com', 'Bogota'),
('Luis Miguel', 'Octaviano Zapata', 3245614, 'luismi@gmail.com', 'Bogota'),
('Brandon', 'Noreña Echavarria', 514263, 'brandonnor@gmail.com', 'Cartagena'),
('Darvis', 'Suarez Fernandez', 3254123, 'Darvisf@gmail.com', 'Barranquilla'),
('John David', 'Lopera Valencia', 854262, 'johnl@gmail.com', 'Barranquilla'),
('Santiago', 'Moreno Vasquez', 2435152, 'santiagom@gmail.com', 'Cali'),
('Martha Lucia', 'Chavarria Loza', 541252,'martac@gmail.com', 'Medellin'),
('David', 'Alvarez Merchan', 4251362, 'davidal@gmail.com', 'Medellin' ),
('Sebastian', 'Alzate Velasquez', 8452362, 'Sebasal@gmail.com', 'Bogota'),
('Bruno', 'Palacio Ortega', 758425, 'brunopa@gmail.com', 'Cali')

Select * from Clientes

CREATE TABLE Pedidos (
	id_Pedido INT IDENTITY (1, 1) PRIMARY KEY,
	id_Cliente INT,
	Estado_Orden tinyint NOT NULL,
	-- Estado: 1 (Pendiente); 2 (En proceso); 3 (Rechazada); 4 (Completado) --
	Fecha_Orden DATE NOT NULL,
	Fecha_Envio DATE,
	Fecha_Entrega DATE,
	id_Sede INT NOT NULL,
	id_personal INT NOT NULL,
	FOREIGN KEY (id_Cliente) 
        REFERENCES Clientes (id_Cliente),
	FOREIGN KEY (id_Sede) 
        REFERENCES Sedes (id_sede) ,
	FOREIGN KEY (id_personal) 
        REFERENCES Personal (id_gerente)     
);

insert into Pedidos(id_Cliente,Estado_Orden, Fecha_Orden, Fecha_Envio, Fecha_Entrega, id_Sede ,id_personal)
values (1,4, '02-03-2020','05-03-2020','06-03-2020', 1, 1 ),
(2,4, '02-03-2020','05-03-2020','08-03-2001', 4, 4 ),
(3,2, '04-03-2020','07-03-2020',NULL, 1, 1 ),
(4,4, '15-03-2020','18-03-2020','20-03-2020', 2, 2 ),
(5,3, '15-03-2020',NULL,NULL, 5, 5 ),
(6,4, '15-03-2020','18-03-2020','22-03-2020', 5, 5 ),--1(Pendiente);2(En proceso);3(Rechazada);4(Completado)--
(7,3, '17-03-2020',NULL,NULL, 3, 3 ),
(8,4, '17-03-2020','22-03-2020','25-03-2020', 4, 4 ),
(9,4, '17-03-2020','22-03-2020','24-03-2020', 2, 2 ),
(10,4, '17-03-2020','22-03-2020','24-03-2020', 2, 2 ),
(11,3, '20-03-2020',NULL,NULL, 5, 5 ),
(12,4, '20-03-2020','24-03-2020','27-03-2020', 3, 3 ),
(13,4, '20-03-2020','24-03-2020','26-03-2020', 3, 3 ),
(14,4, '20-03-2020','24-03-2020','27-03-2020', 4, 4 ),
(15,2, '20-03-2020','24-03-2020',NULL, 1, 1 ),
(16,4, '22-03-2020','23-03-2020','26-03-2020', 1, 1 ),
(17,1, '24-03-2020',NULL,NULL, 2, 2 ),
(18,1, '24-03-2020',NULL,NULL, 4, 4 )

Select * from Pedidos

CREATE TABLE Productos_Pedido(
	id_Pedido INT,
	id_Producto INT NOT NULL,
	Cantidad INT NOT NULL,
	Total DECIMAL (10, 3) NOT NULL,
	PRIMARY KEY (id_Pedido),
	FOREIGN KEY (id_Pedido) 
        REFERENCES Pedidos (id_Pedido),
	FOREIGN KEY (id_Producto) 
        REFERENCES Productos (id_Productos)
);


Insert into Productos_Pedido(id_Pedido,id_Producto,Cantidad,Total)
Values 
(1,3,2,591.800),(2,16,1,630.000),
(3,7,1,560.000),(4,24,2,630.000),
(5,13,2,860.000),(6,19,1,310.000),
(7,4,3,870.000),(8,10,2,700.000),
(9,21,1,350.000),(10,11,1,295.000),
(11,2,2,840.000),(12,17,1,480.000),
(13,6,1,720.000),(14,15,1,520.000),
(15,8,2,640.000),(16,14,1,520.000),
(17,1,2,619.800),(18,5,2,700.000)

Select * from Productos_Pedido

CREATE TABLE Existencias_Producto (
	id_sede INT NOT NULL,
	id_producto INT NOT NULL,
	Existencias INT NOT NULL,
	PRIMARY KEY (id_sede, id_producto),
	FOREIGN KEY (id_sede) 
        REFERENCES Sedes (id_sede),
	FOREIGN KEY (id_producto) 
        REFERENCES Productos (id_Productos)
);

Insert into Existencias_Producto (id_sede, id_producto, Existencias)
Values 
-------------------------------Tienda 1 (MEDELLIN)------------------------------------------------
(1,1,60), 
(1,2,60),
(1,3,60),
(1,4,60),
(1,5,60),
(1,6,60),
(1,7,70),
(1,8,70),
(1,9,70),
(1,10,70),
(1,11,70),
(1,12,70),
(1,13,30),
(1,14,30),
(1,15,30),
(1,16,30),
(1,17,30),
(1,18,30),
(1,19,50),
(1,20,50),
(1,21,50),
(1,22,50),
(1,23,50),
(1,24,50),
-----------------------------Tienda 2 (BOGOTA)--------------------------------------------------
(2,1,80), 
(2,2,80),
(2,3,80),
(2,4,80),
(2,5,80),
(2,6,80),
(2,7,80),
(2,8,80),
(2,9,80),
(2,10,80),
(2,11,80),
(2,12,80),
(2,13,60),
(2,14,60),
(2,15,60),
(2,16,60),
(2,17,60),
(2,18,60),
(2,19,90),
(2,20,90),
(2,21,90),
(2,22,90),
(2,23,90),
(2,24,90),
---------------------------Tienda 3 (BARRANQUILLA)-------------------------------------------------
(3,1,50), 
(3,2,50),
(3,3,50),
(3,4,50),
(3,5,50),
(3,6,50),
(3,7,60),
(3,8,60),
(3,9,60),
(3,10,60),
(3,11,60),
(3,12,60),
(3,13,20),
(3,14,20),
(3,15,20),
(3,16,20),
(3,17,20),
(3,18,20),
(3,19,60),
(3,20,60),
(3,21,60),
(3,22,60),
(3,23,60),
(3,24,60),
-----------------------------Tienda 4 (CALI)-----------------------------------------------------
(4,1,60), 
(4,2,60),
(4,3,60),
(4,4,60),
(4,5,60),
(4,6,60),
(4,7,70),
(4,8,70),
(4,9,70),
(4,10,70),
(4,11,70),
(4,12,70),
(4,13,40),
(4,14,40),
(4,15,40),
(4,16,40),
(4,17,40),
(4,18,40),
(4,19,80),
(4,20,80),
(4,21,80),
(4,22,80),
(4,23,80),
(4,24,80),
---------------------------------Tienda 5 (CARTAGENA)--------------------------------------------
(5,1,60), 
(5,2,60),
(5,3,60),
(5,4,60),
(5,5,60),
(5,6,60),
(5,7,80),
(5,8,80),
(5,9,80),
(5,10,80),
(5,11,80),
(5,12,80),
(5,13,30),
(5,14,30),
(5,15,30),
(5,16,30),
(5,17,30),
(5,18,30),
(5,19,60),
(5,20,60),
(5,21,60),
(5,22,60),
(5,23,60),
(5,24,60)


----------------------------------- CONSULTAS ----------------------------------------------------

-----------------------------------INNER JOIN ---------------------------------------------------
select Estado_Orden,
Fecha_Orden,
Fecha_Envio,
Fecha_Entrega,
Nombre_Cliente,
Apellidos_Cliente,
Nombres_Gerente,
Apellidos_Gerente,
Ciudad_Sede,
Telefono_Sede,
Cantidad,
Total

from Pedidos
inner join Clientes ON Pedidos.id_Cliente = Clientes.id_Cliente
inner join Personal ON Pedidos.id_personal = Personal.id_gerente
inner join Sedes ON Pedidos.id_Sede = Sedes.id_sede
inner join Productos_Pedido ON Pedidos.id_Pedido = Productos_Pedido.id_Pedido
where Total >= 500.000 
--------------------------------------------------------------------------------------------------

---------------------------------------- PROCEDIMIENTOS ALMACENADOS ------------------------------
create proc Iner_Client
@nom_cli Varchar (50) ,
@Apellidos_Cli varchar (50) , 
@Telef Varchar (50) ,
@Email varchar (50) ,
@Ciudad varchar (50) 

AS
Insert into Clientes (Nombre_Cliente, Apellidos_Cliente, Telefono_Cliente, Email_Cliente,Ciudad_Cliente)
values (@nom_cli, @Apellidos_Cli, @Telef, @Email, @Ciudad)

execute Iner_Client 'Rosalba', 'Montoya Giraldo', '5215252', 'Ros54@gmail.com', 'Medellin'

select * from Clientes
where id_Cliente = 19

--------------------------------------------------------------------------------------------------

-------------------------------------- RECUPERACION DE DATOS -------------------------------------
update Clientes
set Nombre_Cliente = 'Jose', Apellidos_Cliente = 'Hernandez E' ,Telefono_Cliente = '55555',
Ciudad_Cliente = 'Bogota'
where Nombre_Cliente= 'Rosalba'

select * from Clientes
where id_Cliente = 19
--------------------------------------------------------------------------------------------------
