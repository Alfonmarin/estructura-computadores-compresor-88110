# 🧠 Estructura de Computadores – Compresor y Descompresor en Ensamblador

## 🧩 Descripción general
Proyecto desarrollado en **ensamblador para el procesador Motorola 88110**, dentro de la asignatura **Estructura de Computadores (ETSIINF-UPM)**.  
El objetivo fue implementar un **sistema de compresión y descompresión de texto sin pérdida**, operando directamente en memoria, para comprender en profundidad la arquitectura y funcionamiento de un procesador RISC.

El código gestiona estructuras en memoria, comparaciones, cadenas y punteros, implementando un algoritmo propio basado en la detección de secuencias repetidas y en el uso de un **mapa de bits** para representar los datos comprimidos.

---

## 🎯 Objetivos principales
- Desarrollar un **algoritmo de compresión sin pérdida** en ensamblador.  
- Implementar la **descompresión inversa**, reconstruyendo el texto original.  
- Manipular memoria, direcciones y registros en un entorno **RISC sin sistema operativo**.  
- Comprender la **organización interna del procesador Motorola 88110** y su modelo de ejecución.

---

## 🧱 Estructura del proyecto
| Archivo | Descripción |
|----------|-------------|
| **`CDV24.ens`** | Código ensamblador principal. Implementa las subrutinas de compresión (`Comprime`), descompresión (`Descomprime`) y utilidades auxiliares (`LongCad`, `BuscaCar`, `CoincidenCad`). |
| **`memoria.pdf`** | Memoria del proyecto con diario de trabajo, casos de prueba y observaciones finales. Incluye los resultados obtenidos y explicaciones de cada subrutina. |

---

## ⚙️ Tecnologías y herramientas
- **Lenguaje:** Ensamblador (Motorola 88110)  
- **Arquitectura:** RISC  
- **Entorno:** Simulador del procesador 88110  
- **Pruebas:** Cadenas almacenadas en memoria, ejecución paso a paso con monitor de registros y memoria.  

---

## 🧮 Subrutinas implementadas
| Subrutina | Función principal |
|------------|------------------|
| **LongCad** | Calcula la longitud de una cadena terminada en byte nulo. |
| **BuscaCar** | Busca la posición de un carácter dentro de una cadena. |
| **CoincidenCad** | Compara dos cadenas y devuelve el número de caracteres coincidentes. |
| **Comprime** | Implementa el algoritmo de compresión, generando un bloque con cabecera, mapa de bits y datos comprimidos. |
| **Descomprime** | Reconstruye el texto original a partir del bloque comprimido. |

---

## 🧪 Casos de prueba destacados
| Prueba | Entrada | Resultado |
|---------|----------|-----------|
| **LongCad** | `"tres tristes tigres comen trigo en un trigal\0"` | Longitud = `44` |
| **CoincidenCad** | `"Estoesun1ejemplo\0"` / `"Estoesunejemplo\0"` | Coinciden = `8` caracteres |
| **Comprime** | `"a cuesta le cuesta subir la cuesta..."` | Bloque comprimido generado correctamente |
| **Descomprime** | Bloque hexadecimal del texto anterior | Texto original reconstruido con éxito |

---

## 🕓 Dedicación y desarrollo
> Trabajo realizado en equipo por **Alejandro Becerra Tapia** y **Alfonso Marín Mite**.  
>  
> Tiempo total estimado: **~25-30 horas de desarrollo y pruebas**, repartidas en dos semanas.  
>  
> El proyecto permitió afianzar los conocimientos sobre **representación de datos, gestión de memoria y optimización de código ensamblador**, fundamentales para comprender la arquitectura de un procesador.

