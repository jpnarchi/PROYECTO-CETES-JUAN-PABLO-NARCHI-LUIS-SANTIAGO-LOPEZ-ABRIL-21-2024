Juan Pablo Narchi, 2024-04-21 para continuar con el proyecto, es importante que detalles en este documento el propósito de cada documento así como los pasos esenciales que sigue el programa a través de sus módulos para la lectura, descomposición, y la recomposición de nuevos documentos a través de las librerías y funciones de Python. Explica la función que cumple cada librería en cada uno de los módulos de python para la conversión de los documentos iniciales a los finales. 

Ver documento diagrama_de_flujo.png para entender mejor el flujo del programa. 


**1. REPORTE - copia (4).xlsm:** Archivo general. Este archivo contiene todas las hojas que queremos replicar.
**2. Resumen_de_Mercado.xls:** INPUT Este archivo es la hoja llamada “Arch. Cierre Mdo” que está en el “REPORTE - copia (4).xlsm”. Saque la hoja del archivo, porque Memo (al que le estamos haciendo esto) va a poner ese archivo en la carpeta y de ahí seguirán los procesos.
**3. Resumen_de_Mercado_Memo.xlsx:** OUTPUT del archivo “Resumen_de_Mercado.xls” ya con los formatos establecidos.
**4. Carpeta Excels:** Es una carpeta donde se guardan todos los dataframes extraídos del archivo “Resumen_de_Mercado.xls” para posteriormente ser ordenados.
**5. main_df.py:** Programa que separa todas las tablas existentes en el archivo “Resumen_de_Mercado.xls” para posteriormente guardar cada data frame en la carpeta “Exceles/”
**6. main_writer.py:** Programa que pone todos los excels de la carpeta Exceles/ dentro de una hoja de excel en la misma estructura que en el archivo REPORTE - copia (4).xlsm (le da formatos de color e inserta todos los archivos en partes especificas de la hoja de excel).
**7. PIP.xls:** Archivo que MEMO descarga todos los días con las actualizaciones de tazas. Este archivo el lo pega en la hoja PIP del “REPORTE - copia (4).xlsm”.
**8. PipViejo.xls:** Es el mismo archivo al PIP.xls solo que con los datos de un día anterior (en el archivo del REPORTE se puede ver como la página PIP T-1)
**9. VectorAnaltico24h.xls:** Archivo que MEMO descarga todos los días con las actualizaciones de tazas. Este archivo lo pega en la hoja VALMER del “REPORTE - copia (4).xlsm”.
**10. VectorViejo.xls:** Es el mismo archivo al VectorAnaltico24h.xls solo que con los datos de un día anterior (en el archivo del REPORTE se puede ver como la página VALMER T-1)
**11. PEMEX_CFE_Resumen_Mercado.py:** Programa que separa todas las tazas de los archivos: “VectorAnaltico24h”, “VectorViejo.xls”, “PIP.xls” y “PipViejo.xls”, solo de las emisoras CFE y PEMEX, y en base a eso crea un dataframe para cada una de las dos emisoras y los guarda en la carpeta Exceles/ para que el “main_writer.py” los inserte también en la hoja.
