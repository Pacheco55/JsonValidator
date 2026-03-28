<div align="center">

<!-- HERO BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:021C1E,50:2C7873,100:6FB98F&height=220&section=header&text=JSON%20Validator%20Pro&fontSize=52&fontColor=CFEAE4&fontAlignY=38&desc=Analizador%20Sintáctico%20JSON%20—%20RFC%208259%20Compliant&descAlignY=60&descSize=18&descColor=A5D5CB&animation=fadeIn" />

<br/>

[![Python](https://img.shields.io/badge/Python-3.9%2B-6FB98F?style=for-the-badge&logo=python&logoColor=CFEAE4&labelColor=021C1E)](https://python.org)
[![RFC 8259](https://img.shields.io/badge/RFC-8259%20Compliant-2C7873?style=for-the-badge&labelColor=021C1E)](https://datatracker.ietf.org/doc/html/rfc8259)
[![PyInstaller](https://img.shields.io/badge/PyInstaller-Ready-4CA88B?style=for-the-badge&logo=python&logoColor=white&labelColor=021C1E)](https://pyinstaller.org)
[![License](https://img.shields.io/badge/License-MIT-6FB98F?style=for-the-badge&labelColor=021C1E)](LICENSE)
[![Version](https://img.shields.io/badge/Version-2.0.0-A5D5CB?style=for-the-badge&labelColor=021C1E)](#)
[![Studio](https://img.shields.io/badge/PIXELBITS-Studio-2C7873?style=for-the-badge&labelColor=021C1E)](https://github.com/Pacheco55)

<br/>

```
⬡  Valida · Analiza · Formatea · Exporta — todo en un solo ejecutable
```

</div>

---

## ¿Qué es JSON Validator Pro?

**JSON Validator Pro** es una herramienta de escritorio de código abierto que actúa como un **analizador sintáctico (parser) visual** para el formato JSON. Va más allá de un simple validador: descompone el documento byte a byte, identifica la causa raíz de cada error, reporta estadísticas estructurales y emite advertencias de calidad conforme al estándar internacional **RFC 8259**.

Diseñada para **programadores, ingenieros en software, testers y arquitectos de sistemas**, convierte el tedioso proceso de depurar un JSON malformado en una experiencia guiada con retroalimentación inmediata, sin necesidad de conexión a internet ni de instalar dependencias adicionales.

> _"Si tu API falla en producción a las 3 AM por un JSON mal formado, JSON Validator Pro lo hubiera atrapado antes."_

---

## Por qué un analizador sintáctico y no solo un validador

Un validador convencional te dice **si** el JSON es válido. Un **analizador sintáctico** te dice **por qué**, **dónde** y **cómo corregirlo**.

| Capacidad | Validador simple | JSON Validator Pro |
|---|:---:|:---:|
| Detecta JSON inválido | ✅ | ✅ |
| Indica línea y columna exactas del error | ❌ | ✅ |
| Sugiere corrección contextual | ❌ | ✅ |
| Detecta claves duplicadas | ❌ | ✅ |
| Analiza profundidad de anidamiento | ❌ | ✅ |
| Reporta estadísticas de tipos de datos | ❌ | ✅ |
| Verifica codificación UTF-8 y BOM | ❌ | ✅ |
| Alerta sobre pérdida de precisión numérica | ❌ | ✅ |
| Funciona 100 % offline | ⚠️ | ✅ |
| Ejecutable independiente (sin instalar Python) | ❌ | ✅ |

---

## Instalación y ejecución rápida

### Ejecutable compilado (recomendada)

Descarga el binario desde [Releases](../../releases) y ejecútalo directamente:

```
JSONValidatorPro.exe    ←  Windows (doble clic)
JSONValidatorPro        ←  Linux   (./JSONValidatorPro)
JSONValidatorPro.app    ←  macOS   (doble clic)
```

> No requiere Python. No requiere instalación. No requiere conexión.

---

## Modo de uso detallado

### 1. Cargar un archivo JSON

Existen tres formas de introducir contenido en la herramienta:

| Método | Cómo hacerlo |
|---|---|
| **Drag & Drop** | Arrastra un archivo `.json` directamente sobre el editor |
| **Abrir archivo** | Botón `📂 Abrir JSON` o atajo `Ctrl+O` |
| **Pegar desde portapapeles** | `Ctrl+V` — valida el contenido automáticamente |

El análisis sintáctico comienza **600 ms después del último cambio** para no interrumpir mientras escribes.

---

### 2. Leer el panel de resultados

El panel derecho muestra el reporte completo del análisis:

```
🔍  ANÁLISIS JSON  ·  2026-02-15  14:32:07
──────────────────────────────────────────────────────────
   Herramienta:  JSON Validator Pro v2.0.0
   Creado por:   Pacheco Rojas Julio Cesar  ·  PIXELBITS Studio
──────────────────────────────────────────────────────────

✅  ESTADO: JSON VÁLIDO

📊  ESTADÍSTICAS:
   Tamaño:   1 842 caracteres  (1 842 bytes)
   Líneas:   67
   Elementos:
      🏢 Objetos:    12
      📋 Arrays:      4
      📝 Strings:    38
      🔢 Números:     9
      ✅ Booleanos:   3

🏗️  ESTRUCTURA:
   Tipo raíz:       dict
   Profundidad máx: 4
   Claves (8):      id, name, email, roles, metadata …

📋  CUMPLIMIENTO RFC 8259:
   ✅ Sintaxis válida
   ✅ Caracteres estructurales correctos
   ✅ Tipos de datos permitidos
```

---

### 3. Interpretar los errores

Cuando el JSON es inválido, el analizador localiza el problema con precisión:

```
❌  ESTADO: JSON INVÁLIDO

🚨  ERRORES:
   ❌  Error de sintaxis: Expecting ',' delimiter
       📍 Línea 23, columna 14
       📄 Línea: "active": true

ℹ️  INFORMACIÓN:
   💡 Verifica que los valores sean válidos
      (string, number, boolean, null, object, array)

⚠️  ADVERTENCIAS:
   ⚠️  Claves duplicadas encontradas: ['userId']
```

---

### 4. Formatear (pretty-print)

El botón `✨ Formatear` re-indenta el JSON con 2 espacios preservando caracteres Unicode:

```json
{"id":1,"name":"Julio","active":true,"roles":["admin","dev"]}
```

```json
{
  "id": 1,
  "name": "Julio",
  "active": true,
  "roles": [
    "admin",
    "dev"
  ]
}
```

---

### 5. Exportar el reporte

`💾 Exportar` (`Ctrl+S`) guarda un reporte `.txt` completo con:

- Metadatos de sesión (fecha, autor, versión, estudio)
- Vista previa del JSON analizado (primeros 2 000 caracteres)
- Todos los errores, advertencias e información
- Estadísticas completas por tipo de dato

---

### Atajos de teclado

| Atajo | Acción |
|---|---|
| `Ctrl + O` | Abrir archivo JSON |
| `Ctrl + V` | Pegar y validar desde el portapapeles |
| `Ctrl + S` | Exportar reporte de validación |
| `F5` | Forzar re-validación manual |

---

## Arquitectura del analizador sintáctico

JSON Validator Pro implementa un pipeline de análisis en capas, análogo al frontend de un compilador:

```
Entrada (texto crudo)
        │
        ▼
┌─────────────────────────┐
│  Pre-análisis léxico    │  ← Verifica UTF-8, BOM, primer token estructural
└─────────────────────────┘
        │
        ▼
┌─────────────────────────┐
│  Análisis estructural   │  ← Balanceo de delimitadores con pila — O(n)
└─────────────────────────┘
        │
        ▼
┌─────────────────────────┐
│  Parser RFC 8259        │  ← json.JSONDecoder de CPython (implementación en C)
└─────────────────────────┘
        │
        ▼
┌─────────────────────────┐
│  Análisis semántico     │  ← Duplicados, precisión numérica, profundidad
└─────────────────────────┘
        │
        ▼
┌─────────────────────────┐
│  Generación de reporte  │  ← Estadísticas, sugerencias, conformidad RFC
└─────────────────────────┘
```

Este diseño permite reportar **múltiples problemas en una sola pasada** y generar **sugerencias contextuales** basadas en el tipo de error detectado, en lugar de detenerse en el primer fallo como hacen los parsers clásicos de compiladores.

---

## Estándar RFC 8259

[RFC 8259](https://datatracker.ietf.org/doc/html/rfc8259) es el estándar IETF que define formalmente el formato JSON. JSON Validator Pro verifica los puntos críticos del estándar:

| Regla RFC 8259 | Sección | Verificación |
|---|:---:|:---:|
| Codificación UTF-8 obligatoria para transmisión | §8.1 | ✅ |
| BOM no recomendado | §8.1 | ✅ |
| Valores: string, number, object, array, true, false, null | §3 | ✅ |
| Strings delimitadas por comillas dobles | §7 | ✅ |
| Caracteres de control escapados en strings | §7 | ✅ |
| Estructura bien formada (tokens balanceados) | §2 | ✅ |
| Claves duplicadas (permitidas pero no recomendadas) | §4 | ⚠️ advertencia |

---

## Licencia

Distribuido bajo la **Licencia MIT**. Consulta el archivo [`LICENSE`](LICENSE) para más detalles.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6FB98F,50:2C7873,100:021C1E&height=120&section=footer" />

**Hecho con 💚 por [Pacheco Rojas Julio Cesar](https://github.com/Pacheco55)**

[PIXELBITS Studio](https://github.com/Pacheco55) &nbsp;·&nbsp; [studiospixelbits@gmail.com](mailto:studiospixelbits@gmail.com)

[![GitHub](https://img.shields.io/badge/GitHub-Pacheco55-6FB98F?style=flat-square&logo=github&labelColor=021C1E)](https://github.com/Pacheco55)
[![Email](https://img.shields.io/badge/Email-studiospixelbits%40gmail.com-2C7873?style=flat-square&logo=gmail&logoColor=white&labelColor=021C1E)](mailto:studiospixelbits@gmail.com)

<sub>JSON Validator Pro v2.0.0 &nbsp;·&nbsp; RFC 8259 Compliant &nbsp;·&nbsp; PIXELBITS Studio © 2026</sub>

</div>
