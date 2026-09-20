# Datos utilizados

## Procedencia y alcance

Fuente original de referencia: [Washington DOL — Electric Vehicle Population Data](https://catalog.data.gov/dataset/electric-vehicle-population-data).

El notebook original cargaba una copia desde [Kaggle: electric-vehicle-pop-data](https://www.kaggle.com/datasets/luisdaniel2104/electric-vehicle-pop-data). La revisión técnica utilizó el CSV proporcionado por el autor. No se ha comprobado aquí que la descarga actual de Kaggle sea idéntica a esa copia.
- link de descarga https://github.com/Daniel210492/washington-ev-population-analysis/blob/main/data/datos-washington-ev.zip
- Nombre local esperado: `electric_vehicle_population.csv`.
- Filas originales: 177,866; columnas: 17.
- Universo analizado: 177,477 filas con `State == WA`.
- Año-modelo máximo: 2024.
- SHA-256 de la copia revisada: `ad9ef46a63c0e68d46731dc1ad6dfafb313c0974e39e8eacc0ebdabb1a4a8469`.

## Obtener y colocar el archivo

Utiliza la copia histórica del autor y guárdala en `data/electric_vehicle_population.csv`. La versión pública actual de la fuente puede tener otras filas y resultados. El notebook técnico comprueba la huella para evitar sustituir inadvertidamente la versión analizada.



## Campos principales

| Campo | Interpretación |
|---|---|
| DOL Vehicle ID | Identificador usado para auditar duplicados |
| State / County / City | Ubicación del registro |
| Postal Code / 2020 Census Tract | Códigos, conservados como texto |
| Model Year | Año-modelo; no fecha de venta o registro |
| Make / Model | Marca y modelo |
| Electric Vehicle Type | BEV o PHEV |
| Electric Range | Autonomía eléctrica; ceros excluidos de estadísticas técnicas |
| Base MSRP | Precio base; no precio pagado; ceros excluidos de estadísticas de precio |
| Legislative District | Identificador de distrito; no imputado |

Los valores ausentes se preservan cuando no impiden el análisis. Los filtros de autonomía o precio no eliminan vehículos del universo general.
