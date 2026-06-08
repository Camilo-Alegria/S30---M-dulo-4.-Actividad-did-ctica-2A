# Simulación del Sistema de Parqueaderos - Centro Comercial Supercentro

## Descripción

Este proyecto presenta una simulación de eventos discretos para analizar el funcionamiento del sistema de salida de un parqueadero de un centro comercial. El modelo considera diferentes tipos de usuarios, tiempos de llegada y servicio aleatorios, y una política de atención basada en la cola más corta.

El objetivo principal es evaluar si la configuración actual de tres cajeros es suficiente para atender la demanda y analizar posibles mejoras mediante la comparación con configuraciones de cuatro y cinco cajeros.

---

## Objetivos

### Objetivo General

Analizar el desempeño del sistema de atención del parqueadero mediante simulación, con el fin de determinar si la capacidad actual es suficiente y evaluar posibles alternativas de mejora.

### Objetivos Específicos

* Modelar el sistema utilizando teoría de colas M/M/1.
* Obtener métricas de desempeño del sistema.
* Analizar el comportamiento de los diferentes tipos de usuarios.
* Verificar, calibrar y validar el modelo de simulación.
* Determinar el estado estable y eliminar el período transitorio.
* Comparar configuraciones de tres, cuatro y cinco cajeros.

---

## Herramientas Utilizadas

* Python
* NumPy
* Pandas
* Matplotlib
* SciPy

---

## Modelo Implementado

El sistema está compuesto por tres servidores independientes M/M/1. Los clientes son asignados al cajero que tenga la menor longitud de cola. Tanto los tiempos entre llegadas como los tiempos de servicio siguen distribuciones exponenciales.

Se consideran cuatro tipos de usuarios:

* Rápido
* Normal
* Lento
* Muy lento

---

## Métricas Analizadas

* Tiempo promedio de espera (Wq)
* Tiempo promedio en el sistema (W)
* Tiempo promedio de servicio
* Longitud promedio de cola (Lq)
* Utilización del sistema
* Clientes atendidos por cajero
* Utilización individual de cada cajero
* Tiempos promedio por tipo de usuario

---

## Verificación y Validación

Se realizaron diferentes pruebas para comprobar el correcto funcionamiento del modelo:

* Conservación de clientes.
* Verificación de tiempos no negativos.
* Comparación con los principios teóricos de los sistemas de colas.
* Calibración de parámetros.
* Validación de resultados.

---

## Estado Estable y Eliminación del Transitorio

Se utilizó la técnica del promedio móvil para identificar el período de calentamiento del sistema y determinar el punto de corte del estado transitorio. Posteriormente se recalcularon las métricas utilizando únicamente observaciones pertenecientes al estado estable.

---

## Comparación de Configuraciones

Se evaluaron tres escenarios:

* 3 cajeros
* 4 cajeros
* 5 cajeros

Los resultados muestran que la configuración actual de tres cajeros es suficiente para la demanda analizada y que agregar más servidores no genera mejoras significativas.

---

## Estructura del Proyecto

```
├── codigo_simulacion.ipynb
├── informe_final.docx
├── graficas/
├── resultados/
├── README.md
```

---

## Resultados Principales

* Los tres cajeros son suficientes para la demanda actual.
* La utilización promedio del sistema es baja, por lo que no existe congestión significativa.
* La política de selección de la cola más corta distribuye adecuadamente la carga entre los cajeros.
* El sistema alcanza rápidamente el estado estable.
* Las diferencias entre las métricas con y sin transitorio son pequeñas.

---

## Autor

Jhojanth Camilo Alegría Escobar
Juan Fernado Beltran Lopez



Universidad Autónoma de Occidente

2026
