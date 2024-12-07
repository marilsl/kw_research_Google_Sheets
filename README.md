# README

Este repositorio contiene un script en Google Apps Script que permite transformar datos JSON obtenidos de la API de Authoritas en una hoja de Google Sheets. El script organiza la información en columnas predefinidas, resalta ciertas celdas según su contenido y ajusta el ancho de columnas para mejorar la legibilidad.

## Descripción

Este script está diseñado para:
- Leer datos JSON (almacenados en la variable `jsonData`) con información de palabras clave, volúmenes de búsqueda, CPC, URLs y métricas de visibilidad.
- Mapear las propiedades del JSON a columnas específicas en una hoja de cálculo de Google Sheets.
- Añadir encabezados a la primera fila.
- Insertar filas con datos, reemplazando valores nulos o indefinidos por 0.
- Marcar en verde aquellas celdas de la columna "Palabra_clave" que contengan más de cuatro palabras.
- Ajustar el ancho de las columnas destinadas a las métricas de visibilidad para una mejor presentación.

## Uso

1. Abre un documento de Google Sheets y accede al editor de Apps Script (`Extensiones > Apps Script`).
2. Copia y pega el código del script en el editor.
3. Ajusta la fuente de datos JSON dentro de la variable `jsonData`:
   ```javascript
   const jsonData = {
     // AQUI TODO EL CONTENIDO obtenido de la API
   };
