# Wordle y teoría de la información de Shannon

## Descripción del proyecto

Este proyecto explora cómo utilizar la teoría de la información de Claude Shannon para mejorar la selección de palabras en el juego Wordle.

La idea principal es utilizar la entropía y la información mutua para elegir intentos que permitan reducir la incertidumbre sobre la palabra secreta y descartar la mayor cantidad posible de palabras.

El proyecto se desarrolló en Python utilizando Google Colab y un conjunto de 2.309 palabras posibles. Se implementó una estrategia basada en Shannon y se comparó su desempeño con dos alternativas: elegir palabras al azar y comenzar con CRANE para después elegir candidatas al azar.

## Objetivo

Aplicar conceptos de la teoría de la información para diseñar una estrategia de selección de palabras en Wordle y evaluar su desempeño mediante simulaciones.

## Fundamento teórico

El desarrollo utiliza los siguientes conceptos:

- **Información de un evento:** permite medir cuánta información aporta un resultado.
- **Entropía:** representa la incertidumbre que existe sobre la palabra secreta.
- **Entropía condicional:** mide la incertidumbre que permanece después de recibir una pista.
- **Información mutua:** permite medir cuánto se reduce la incertidumbre gracias al resultado de un intento.

## Metodología

El proyecto se desarrolló en las siguientes etapas:

1. Se obtuvo una lista de 2.309 palabras posibles de Wordle.
2. Se programó la comparación entre palabras para generar los patrones de colores verde, amarillo y gris.
3. Se calculó la entropía de los posibles patrones para seleccionar la palabra que proporciona mayor información esperada.
4. Se actualizaron las palabras candidatas después de cada intento.
5. Se realizaron simulaciones para comparar las estrategias.
6. Se analizaron los resultados mediante promedios, porcentajes de victoria y número máximo de intentos.

## Resultados principales

Las simulaciones mostraron los siguientes resultados:

| Estrategia | Promedio de intentos | Victorias |
|---|---:|---:|
| Shannon | 3,51 | 100 % |
| CRANE + candidata al azar | 3,85 | 98,4 % |
| Candidata al azar | 4,07 | 98,1 % |

En las simulaciones, la estrategia basada en Shannon obtuvo el menor promedio de intentos y resolvió todas las palabras dentro del límite de seis intentos.

Las otras estrategias también se evaluaron más allá del sexto intento para conocer cuántas jugadas adicionales podían necesitar. Esos casos se consideran derrotas bajo las reglas oficiales de Wordle.

## Herramientas utilizadas

- Python.
- Google Colab.
- NumPy.
- Matemáticas y teoría de la información.
- Conjunto de palabras de Wordle del repositorio de 3Blue1Brown.

## Fuente de los datos

Lista de palabras utilizada:

[3Blue1Brown – Wordle possible words](https://github.com/3b1b/videos/blob/master/_2022/wordle/data/possible_words.txt)

## Integrantes

- Dayana Marcela Narváez.
- Ian Alejandro Hernández.

**Asignatura:** Comunicaciones Digitales  
**Universidad:** Universidad del Cauca

## Uso de inteligencia artificial

Se utilizó inteligencia artificial como apoyo en la elaboración inicial de algunas explicaciones y en el desarrollo del código. Los resultados fueron revisados mediante la ejecución de las simulaciones en Google Colab y la comprobación de los cálculos principales.

La interpretación de los resultados y las decisiones del proyecto fueron revisadas por los integrantes.
