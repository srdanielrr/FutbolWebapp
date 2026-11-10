# FutbolWebApp

Aplicación web desarrollada con DataFlex 25.0 y MySQL para gestionar
ligas, equipos, jugadores, entrenadores y posiciones.

## Funcionalidades

- Dashboard con cinco tarjetas de navegación.
- Vistas Select para listar los registros de cada tabla.
- Vistas Zoom para consultar los detalles de un registro.
- Conexión con MySQL mediante ODBC.

## Requisitos

- DataFlex 25.0 y Web Application Server.
- MySQL Server.
- MySQL Connector/ODBC de 64 bits.
- Si se ejecuta una versión de 32 bits, controlador y DSN de 32 bits.

## Preparación de la base de datos

1. Iniciar MySQL Server.
2. Abrir MySQL Workbench y conectarse al servidor.
3. Abrir y ejecutar el script `sql/football.sql`.
4. Comprobar que se han creado las tablas y sus datos.

## Configuración de la conexión

1. Abrir el Administrador de orígenes de datos ODBC de 64 bits.
2. Crear un DSN de sistema llamado `FootballMySQL` con el controlador
   MySQL ODBC Unicode.
3. Indicar el servidor, puerto, usuario, contraseña y base de datos
   correspondientes a la instalación local.
4. Abrir el workspace y configurar su conexión ODBC para utilizar ese DSN.
5. Comprobar la conexión desde DataFlex.

Las credenciales deben configurarse en cada equipo.

## Ejecución

1. Abrir `FutbolWebapp.sws` en DataFlex Studio.
2. Comprobar que el servicio Web Application Server está iniciado.
3. Verificar la configuración de la aplicación web local en IIS.
4. Compilar y ejecutar con F5.
5. Desde el Dashboard, seleccionar una tarjeta para abrir su lista.
6. Seleccionar un registro para consultar su ficha Zoom.

## Estructura

- `AppSrc`: código de la aplicación, Dashboard y vistas.
- `DDSrc`: Data Dictionaries.
- `AppHtml`: archivos de la interfaz web.
- `Data`: archivos de datos y configuración del workspace.
- `sql`: script de creación y carga de la base de datos.

## Organización del desarrollo

- `main`: versión final de la práctica.
- `develop`: integración de funcionalidades.
- `feature/...`: desarrollo de funcionalidades.