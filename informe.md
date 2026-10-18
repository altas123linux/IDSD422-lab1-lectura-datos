# Informe técnico — Consolidación de reportes de ventas

**Para:** Gerencia de RetailAndina S.A. · **De:** Equipo de Business Intelligence
**Fecha:** ___/___/2026 · **Asunto:** Primer análisis de los reportes de ventas (semana 39)

> **Formato de entrega:** este documento organiza el contenido del informe. El entregable es su versión final en **PDF** según la **plantilla del curso** (aula virtual), con el enlace de tu repositorio en la carátula; el PDF se incluye en `informes/` de tu fork.

---

## Resumen ejecutivo

*Escribe 3–4 líneas para gerencia: qué reportes recibiste, qué confirmaste y qué recomienda el equipo.*

## 1. ¿Los tres formatos contienen la misma información?

*Carga los tres archivos (CSV, JSON y Excel) en Python y en R, y compara dimensiones y estructura. Completa la tabla:*

| Formato | Origen | Filas | Columnas | Lectura en código |
|---|---|---|---|---|
| CSV | ERP de sucursales |5 |4 |ventas = pd.read_csv("data/ventas.csv") / ventas <- read_csv("data/ventas.csv")
| JSON | API de fidelización |5 | 4| datos= json.load(f)+ventas=pd.json_normalize(datos)  / ventas<- fromJSON("data/ventas.json")
| Excel | Consolidado de finanzas |5 | 4| ventas = pd.read_excel("data/ventas.xlsx", sheet_name="ventas")  /  ventas <- read_excel("data/ventas.xlsx", sheet="ventas")

*Responde: ¿la estructura interna del archivo (texto plano, anidada, binaria) cambia el contenido?*

No, la estructura interna del archivo no cambia el contenido. Durante la consolidacion  de los reportes de ventas se evidenció que todos los formatos contienen 5 observaciones y 4 variables.

## 2. Tipos de datos y calidad

*Inspecciona los tipos que infiere cada lenguaje. Completa la tabla y comenta si los tipos son los esperados para cada variable:*

| Variable | Tipo inferido (Python) | Tipo inferido (R) | Interpretación |
|---|---|---|---|
| `ventas` |int64 | | |
| `clientes` |int64 | | |
| `sucursal` | | | |
| `region` | | | |

*¿Qué habría indicado un dato sucio si, por ejemplo, `ventas` llegara como texto?*

## 3. Particularidades técnicas encontradas

*Anota qué encontraste al leer cada formato (una nota por formato): ¿el JSON llegó como tabla? ¿hubo que indicar una hoja en el Excel? ¿cómo se expresan las categóricas en cada lenguaje?*

## 4. Indicadores para la reunión del lunes

*Calcula los indicadores con los datos consolidados y completa la tabla:*

| Indicador | Valor |
|---|---|
| Venta promedio por sucursal | |
| Ticket promedio (ventas ÷ clientes) | |
| Sucursal con mayor venta | |
| Sucursal con menor venta | |
| Región con mayor venta total | |

## 5. Conclusiones y recomendación

1.
2.
3.
