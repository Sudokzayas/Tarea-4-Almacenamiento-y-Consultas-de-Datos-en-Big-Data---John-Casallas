# 📊 Proyecto NoSQL: Análisis de Subsidios de Vivienda (MongoDB)

Este repositorio contiene el desarrollo de un ejercicio práctico de **Bases de Datos NoSQL** utilizando **MongoDB**. El proyecto simula la gestión, limpieza (ETL) y análisis de datos de asignación de subsidios de vivienda en Colombia (Programas CMC y Mi Casa Ya).

## 📋 Descripción del Proyecto

El objetivo principal es migrar datos de un formato plano (CSV) a una base de datos orientada a documentos, para luego realizar operaciones de limpieza, gestión de registros (CRUD) y análisis estadístico mediante tuberías de agregación (*Aggregation Pipelines*).

* **Base de Datos:** `BD_John`
* **Colección:** `Subsidios_2025`
* **Fuente de Datos:** Archivo CSV con registros de asignaciones municipales.

## 🛠 Requisitos Previos

* **MongoDB Server** (v8.0 o superior).
* **MongoDB Shell (`mongosh`)** o **MongoDB Compass**.

## 🚀 Instalación y Configuración

### 1. Importación de Datos
MongoDB no permite importar archivos CSV directamente desde la consola de JavaScript. Debes ejecutar el siguiente comando en tu **terminal del sistema operativo** para cargar los datos iniciales:

```bash
mongoimport --db BD_John --collection Subsidios_2025 --type csv --headerline --file "Subsidios_Mejoramientos_Programas_CMC-MCY_20251122.csv"
