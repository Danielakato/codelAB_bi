<p align="center">
  <img src="https://github.com/Danielakato/codelAB_bi/blob/9005d2e9f06882bcac92256e915831b3c536be56/portada%20Daniela%20Kayerr.png" height= "230"/>
</p>

<div align "center">
<h1 align="center"> Hola, soy Daniela Kayerr Tovar 
  <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="35"> </h1>
<ing src="https://github.com/Danielakato/codelAB_bi/commit/bf2b7c96d2894da5f193319745e47c9c651201ea">  

---

<img src="https://media.giphy.com/media/ObNTw8Uzwy6KQ/giphy.gif" width="30px">&nbsp;***Hablando de temas personales...***
- 🔭 Soy Estudiante de Administración de empresas en la Universidad de la Sabana
  
- 🌱 Actualmente estoy aprendiendo phyton, SQL y cada una de sus funcionalidades, semejanzas y diferencias
  
- 👯 Busco mejorar mis habilidades de programación complementandolas con el diseño
  
- ⚡ Fun fact: Me encanta jugar volleyball, cocinar y la edición de medios audiovisuales

---
***Conectate conmigo...*** <img src='https://raw.githubusercontent.com/ShahriarShafin/ShahriarShafin/main/Assets/handshake.gif' width="100px">

<div align=left>
<a href="https://www.linkedin.com/in/daniela-kayerr" target="_blank">
<img src=https://img.shields.io/badge/linkedin-%2300acee.svg?color=405DE6&style=for-the-badge&logo=linkedin&logoColor=white alt=linkedin style="margin-bottom: 5px;" />

---

# Codelab_BI: Generación y Almacenamiento de Datos Financieros en una Base de Datos SQLite3
Este proyecto genera datos financieros ficticios utilizando la biblioteca Faker y la API randomuser.me, y almacena estos datos en una base de datos SQLite3. Los datos incluyen información de clientes, sucursales, tipos de transacciones y transacciones, incluidas las fraudulentas. A continuación se describen los pasos y procesos implementados.

## 1. Configuración inicial y creación de la base de datos
- Bibliotecas Importadas: Utilizamos Python con bibliotecas como sqlite3, pandas, requests, uuid, Faker, numpy, y shutil.
- Conexión a SQLite3: Se estableció una conexión a una base de datos SQLite3 llamada financial_data.db2.
- Tablas Creadas:
    customers: Almacena información de clientes.
    branches: Almacena información sobre sucursales bancarias.
    transaction_types: Almacena los diferentes tipos de transacciones.
    transactions: Registra las transacciones, incluyendo si son fraudulentas.
  
## 2. Generación y Almacenamiento de Datos de Clientes
- API Utilizada: Los datos de los clientes se obtuvieron utilizando la API randomuser.me, que proporciona información de usuarios ficticios.
- Datos Incluidos: ID de cliente, nombre, dirección, número de teléfono y correo electrónico.
- Almacenamiento: Los datos de clientes se guardaron en la tabla customers de SQLite3.

## 3. Generación y Almacenamiento de Datos de Sucursales
- Datos Generados: Usando Faker, se generaron datos para las sucursales, incluyendo ID de sucursal, ubicación, nombre del gerente y número de contacto.
- Almacenamiento: Los datos de sucursales se guardaron en la tabla branches.

## 4. Generación y Almacenamiento de Tipos de Transacciones
- Datos Incluidos: Se crearon dos tipos de transacciones: "online" y "in-store", cada una con una descripción asociada.
- Almacenamiento: Los datos se guardaron en la tabla transaction_types.

## 5. Generación y Almacenamiento de Transacciones
- Datos Generados: Transacciones con ID, ID de cliente, fecha, monto, ubicación, tipo de transacción, e ID de sucursal.
- Se identificaron algunas transacciones como fraudulentas.
- Almacenamiento: Los datos se guardaron en la tabla transactions.

## 6. Verificación y Guardado Final
- Verificación: Se verificó que todas las tablas se crearon correctamente en la base de datos.
- Guardado: Finalmente, la base de datos se guardó en Google Drive para su almacenamiento a largo plazo.
