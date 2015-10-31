	CREATE TABLE BaseCliente (
	
	ClienteId int primary key identity (1,1),
	Nombre varchar (50) Not null,
	Apellido nvarchar (50) Not null,
	Direccion nvarchar (200) Not null,
	CorreoElectronico nvarchar (50) Not null,
	Edad int Not null,
	FechaNacimiento date,
	FechaInicio  date

	 )

	 CREATE PROCEDURE IngresarBaeCliente
	@pNombre  varchar (50),
	@pApellido nvarchar (50),
	@pDireccion nvarchar (200),
	@pCorreoElectronico nvarchar (50),
	@pEdad int,
	@pFechaInicio date ,
	@pFechaNacimiento date

AS

	INSERT INTO [dbo].[BaseCliente] (Nombre,Apellido,Direccion,CorreoElectronico,Edad,FechaInicio,FechaNacimiento)
	VALUES (@pNombre,@pApellido,@pDireccion,@pCorreoElectronico,@pEdad,GETDATE(),@pFechaNacimiento)
GO

	INSERT INTO  [dbo].[BaseCliente] (Nombre,Apellido,Direccion,CorreoElectronico,Edad,FechaInicio,FechaNacimiento)
	VALUES  ('Jose','Vargas','San Antonio Coronado','vf_jd87@hotmail.com','28',GETDATE(),'27/07/1987');

	INSERT INTO [dbo].[BaseCliente] (Nombre,Apellido,Direccion,CorreoElectronico,Edad,FechaInicio,FechaNacimiento)
	VALUES ('Pablo','Soto','Sabanilla Montes de Oca','soto_pablo@gmail.com','30',GETDATE(), '26/12/1986');

	SELECT * FROM [dbo].[BaseCliente]



	CREATE TABLE BaseEmpleados (

	EmpleadoId int primary key identity (1,1),
	Nombre varchar (50) Not null,
	Apellido nvarchar (50) Not null,
	MarcaVehiculo nvarchar (200) Not null,
	ModeloVehiculo int Not null,
	CorreoElectronico nvarchar (50) Not null,
	FechaInicio  date
	
	)

	AlTER TABLE BaseEmpleados 
	Add NumeroCelular nvarchar (50)

	 CREATE PROCEDURE IngresarBaseEmpleados
	@pNombre  varchar (50),
	@pApellido nvarchar (50),
	@pMarcaVehiculo nvarchar (200),
	@pModeloVehiculo int ,
	@pCorreoElectronico nvarchar (50),
	@pFechaInicio date ,
	@pNumeroCelular nvarchar (50)

AS
	INSERT INTO [dbo].[BaseEmpleados](Nombre,Apellido,MarcaVehiculo,ModeloVehiculo,CorreoElectronico,FechaInicio,NumeroCelular)
	VALUES (@pNombre,@pApellido,@pMarcaVehiculo,@pModeloVehiculo,@pCorreoElectronico,GETDATE(),@pNumeroCelular);
GO

	INSERT INTO [dbo].[BaseEmpleados](Nombre,Apellido,MarcaVehiculo,ModeloVehiculo,CorreoElectronico,FechaInicio,NumeroCelular)
	VALUES ('Homero','Simpson','Toyota','2015','homero_simpson@gmail.com',GETDATE(),'11-11-11-11');

	INSERT INTO [dbo].[BaseEmpleados](Nombre,Apellido,MarcaVehiculo,ModeloVehiculo,CorreoElectronico,FechaInicio,NumeroCelular)
	VALUES ('Bob','Patiño','Nissan','2000','bob-patiño@yahoo.com',GETDATE(),'22-22-22-22');

	SELECT * FROM [dbo].[BaseEmpleados]
	


	