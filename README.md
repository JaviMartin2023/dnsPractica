# Comprobaciones del Servidor DNS

Este documento detalla el proceso de verificación del funcionamiento de los servidores DNS configurados en la red `sistema.test`, incluyendo las comprobaciones de registros A, registros inversos, alias, servidores NS, registros MX y transferencia de zona entre el servidor maestro y el esclavo.

## Tabla de Contenidos

1. [Introducción](#introducción)
2. [Requisitos](#requisitos)
3. [Comprobaciones](#comprobaciones)
   - [Registros tipo A](#registros-tipo-a)
   - [Resolución inversa](#resolución-inversa)
   - [Alias (CNAME)](#alias-cname)
   - [Servidores NS](#servidores-ns)
   - [Registros MX](#registros-mx)
   - [Transferencia de zona (AXFR)](#transferencia-de-zona-axfr)
   - [Consistencia entre servidores](#consistencia-entre-servidores)

## Introducción

Este documento describe los pasos realizados para verificar la correcta configuración y funcionamiento de los servidores DNS en la red `sistema.test`, asegurando que se cumplan los requisitos establecidos.

## Requisitos

- Tener acceso a las máquinas virtuales Vagrant que actúan como servidor maestro (`tierra.sistema.test`) y esclavo (`venus.sistema.test`).
- Herramientas de consulta DNS como `dig` o `nslookup`. En mi caso, será con dig.

## Comprobaciones

### Registros tipo A

![image](https://github.com/user-attachments/assets/41a8950c-bc4a-493a-ad2d-2c0b025d336d)

### Resolución inversa

![image](https://github.com/user-attachments/assets/c014ebbd-3f0b-4f2d-9d47-04faa83d9a9e)

### Alias

![image](https://github.com/user-attachments/assets/aa1d2e3c-584d-4b34-8771-e6a8176e92aa)

![image](https://github.com/user-attachments/assets/2cb242a8-5783-45b2-835f-74360c51d89c)

### Servidores NS

![image](https://github.com/user-attachments/assets/b0c006f7-caa9-4b13-8109-c1f030bb41d3)

### Registros MX

![image](https://github.com/user-attachments/assets/3d51ca09-36fb-4dd4-9ba1-db736d262728)

### AXFR

Lo comprobaremos desde venus

![image](https://github.com/user-attachments/assets/9cfa6712-e88a-4ece-9e97-b26c8cf81d29)

### Consistencia entre servidores

Desde tierra primero:

![image](https://github.com/user-attachments/assets/0f875bf3-2922-49ff-b79f-2dc38c9dd6ef)


Ahora desde venus:

![image](https://github.com/user-attachments/assets/3644c1e3-ef63-4391-b1ca-732ec7989622)

