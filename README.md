# SistemasGerencialesCubo
BikeStore Data Science
---
Welcome to the SistemasGerencialesCubo!

Primeramente se tiene que crear el proyecto de multidimensional de mineria de datos en VSTUDIO.

![image](https://user-images.githubusercontent.com/82064182/198863202-35ba6a90-dfe8-49ee-b7bb-6f545bce1ef3.png)

Si no te aparece nada de esto es porque quizas no esten instaldos las Extensiones necesarias para poder hacer DataWarehouses o similares, para ello tienes que instalar 2 extensiones desde VStudio que son las Siguientes:
* Analisis Services
* Integration Services
Esto ayudara que podamos manipular estos tipos de proyectos.

![image](https://user-images.githubusercontent.com/82064182/198863253-9485cbdf-e74b-4018-ba93-146d4315745d.png)

Tambien debes verificar si Sql Server esta habilitado para podes ejecutar Analisis Services, para ello prueba abrir este modo en SQL.

![image](https://user-images.githubusercontent.com/82064182/198863294-31376668-8393-4c39-9e51-97136eafd7e9.png)

Si no lo tienes tendras que modificar la instancia de instalacion de Sql para poder instalar este servicio, para ello tendras que hacer una modificacion a la instancia actual, ahi tendras que activar Analisis Services e Integration Services, añadiendo un usuario correspondiente para que sql pueda dar permisos a ese usuario.

![image](https://user-images.githubusercontent.com/82064182/198863375-194c1af9-ec45-4269-81fa-1d9d6da71919.png)

Posteriormente tendras que añadir un Usuario universal para que este pueda acceder a los servicios OLAP 

**NT SERVICE\MSSQLServerOLAPService**
Este seria el usuario a agregar a la base de datos a manipular, posteriormente deberas darle la propiedad de DataReader para que solo nos pueda leer informacion pero jamas modificarla.

Teniendo todo esto deberas crear la conexion del cubo a la base de datos.
Posterior a eso deberas crear las vistas de tu proyecto, pasando los parametros que se deberan leer en el cubo (nunca pasar los diagramas y tablas que no sean escenciales en este apartado).
Una vez teniendo estas dos partes, vamos a crear las dimensiones que conformaran a nuestro cubo, para ello deberemos crear una por una, asi nos aseguramos de que nuestras dimensiones lleven los datos que se estan solicitando.
Posteriormente crearemos el cubo para que pueda leer nuestras dimensiones, procesamos el cubo y luego ejecutamos (aqui pueden surgir muchos errores de ejecucion o de procesamiento, para ello dejare un video donde se explicara paso a paso desde la solucion de errores mas comunes hasta los errores de usuario).

[Configuraciones de errores SQL Server Analysis Services y Reporting Service](https://youtu.be/QJfDG95jDbI) Creditos a: Luciano Gutierrez


[Install SQL Server Analysis Services](https://learn.microsoft.com/en-us/analysis-services/instances/install-windows/install-analysis-services?view=asallproducts-allversions) Microsoft Docs

  
