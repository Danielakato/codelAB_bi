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

## 1. Configuración Inicial y Creación de la Base de Datos
Este primer bloque se enfoca en la configuración inicial y la creación de la conexión con la base de datos SQLite.
- Instalación de librerías: El código inicia instalando la librería faker, que se utiliza para generar datos ficticios. Esto se realiza a través de la línea !pip install faker.
- Importación de módulos: Luego, se importan las bibliotecas necesarias como sqlite3, pandas, requests, random, uuid, Faker, numpy y shutil. Estos módulos permiten la manipulación de datos, la creación de tablas y la gestión de conexiones con la base de datos.
- Montar Google Drive: Este paso permite acceder a Google Drive desde el entorno, usando el comando drive.mount('/content/drive').
- Conexión a SQLite: Aquí, conectas a la base de datos SQLite utilizando sqlite3.connect, especificando la ruta en Google Drive *(/content/drive/MyDrive/sources/financial_data.db)*. Esto permite interactuar con la base de datos.
- Lectura de tablas con Pandas: Para verificar que la conexión y las tablas funcionan correctamente, usas un comando SQL dentro de pd.read_sql_query para leer datos de la tabla tbl_customers. Luego, se imprime el contenido de esa tabla para su inspección.

## 2. Consulta SQL para Visualizar Registros
- Prompt generado por IA: Ver los primeros 10 registros de la tabla tbl_customers, y el script generado ejecuta esta consulta y la muestra en pantalla.
#### df=pd.read_sql_query("SELECT * FROM tbl_corrected_transactions LIMIT 10", conn)
El código conecta a la base de datos y luego ejecuta la consulta SQL que obtiene los primeros 10 registros de la tabla *tbl_corrected_transactions*. 
Después, los resultados se imprimen como un DataFrame.

<img src="https://private-user-images.githubusercontent.com/179054771/366516221-c85a3881-c12d-479a-8c3b-2bd001f72392.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjYwNjc5NzYsIm5iZiI6MTcyNjA2NzY3NiwicGF0aCI6Ii8xNzkwNTQ3NzEvMzY2NTE2MjIxLWM4NWEzODgxLWMxMmQtNDc5YS04YzNiLTJiZDAwMWY3MjM5Mi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwOTExJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDkxMVQxNTE0MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02OWJlMTQyZWM2ZWE3ZmViNmMwMDQ1YTM3YmVjMGFmOGY2Yzk0ZjYxZmM1MTMwODNkYTAyY2RlZDczNWRmNGYyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.ierNEiaIAJbKgZzR3uhLUZxlP0Fj6nLiSDjBpzwjmvo">
<img src="https://github.com/Danielakato/codelAB_bi/blob/main/codigo%202.png">
<img src="https://github.com/Danielakato/codelAB_bi/blob/main/codigo%203.png">
<img src="https://github.com/Danielakato/codelAB_bi/blob/main/codigo%204.png">


## 3. Análisis Exploratorio de Datos (EDA)
- Prompt generado por IA: Análisis exploratorio de datos (EDA) sobre las tablas de la base de datos, y se generó un script para ello.
- EDA básico: El código primero identifica todas las tablas de la base de datos a través de una consulta SQL que obtiene los nombres de las tablas.
- Para cada tabla:
  1. Se imprime la información general del DataFrame (df.info()), que incluye el número de entradas, tipos de datos y memoria utilizada.

      <img src="https://github.com/Danielakato/codelAB_bi/blob/main/codigo%205.png">
     
  2. Se muestran estadísticas descriptivas con el método df.describe() para obtener datos como la media, desviación estándar, entre otros.

      <img src="https://github.com/Danielakato/codelAB_bi/blob/main/codigo%206.png">
     
  3. También se verifica la existencia de valores faltantes con df.isnull().sum().

     <img src="https://github.com/Danielakato/codelAB_bi/blob/main/codigo%207.png">
     
  4. Visualizaciones: Para las columnas numéricas, se generan gráficos de histograma usando seaborn. Además, se genera una matriz de correlación si hay más de una columna numérica en la tabla, visualizada con un mapa de calor.
     
     <img src="https://github.com/Danielakato/codelAB_bi/blob/main/histograma%201.png">
     <img src="https://github.com/Danielakato/codelAB_bi/blob/main/histograma%202.png">
     <img src="https://github.com/Danielakato/codelAB_bi/blob/main/histograma%203.png">
     
## 4. Creación de Tablas en SQLite
Creación de varias tablas en la base de datos. El código generado por la IA crea las siguientes tablas en SQLite:
  1. Tabla de clientes:
      - API randomuser.me, que proporciona información de usuarios ficticios.
      - Datos Incluidos: ID de cliente, nombre, dirección, número de teléfono y correo electrónico.
      - Almacenamiento: Los datos de clientes se guardaron en la tabla customers de SQLite3.
        
      <img src="https://github.com/Danielakato/codelAB_bi/blob/main/tabla%20customers.png">
  
  2. Tabla de sucursales:
     - Usando Faker
     - Datos incluidos: ID de sucursal, ubicación, nombre del gerente y número de contacto.
     - Almacenamiento: Los datos de sucursales se guardaron en la tabla branches.
       
      <img src="https://github.com/Danielakato/codelAB_bi/blob/main/tabla%20sucursales.png">
       
  3. Tabla de tipos de transacciones:
      - Usando Faker
      - Datos incluidos: Se crearon dos tipos de transacciones: "online" y "in-store", cada una con una descripción asociada
      - Almacenamiento: Los datos se guardaron en la tabla transaction_types.
        
  4. Tabla de generación y almaenamiento de transacciones:
      - Se identificaron algunas transacciones como fraudulentas.
      - Datos incluidos: Transacciones con ID, ID de cliente, fecha, monto, ubicación, tipo de transacción, e ID de sucursal.
      - Almacenamiento: Los datos se guardaron en la tabla transactions.



## 5. Verificación y Guardado Final
- Verificación: Se verificó que todas las tablas se crearon correctamente en la base de datos.
- Guardado: Finalmente, la base de datos se guardó en Google Drive para su almacenamiento a largo plazo.

## 6. Guardar la Base de Datos en Google Drive
Usar la librería shutil para copiar la base de datos generada a Google Drive, permitiendo acceder a ella posteriormente desde el entorno de Drive.
python
