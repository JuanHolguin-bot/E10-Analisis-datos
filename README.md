# E10-Analisis-datos
Equipo E10 · Análisis de Datos Intermedio · Estud-IA (Capa 2)

## Brief v1

| Campo | Respuesta |
|---|---|
| Usuario y decisión | ¿Quién decide qué, y cada cuánto? |
| Pregunta | ¿Qué tipos de vehículos e infracciones concentran el mayor volumen de comparendos y cartera morosa por punto de atención y periodo, para focalizar tanto los operativos de control en vía como las estrategias de recaudo? |
| Fuente con API | Enlace al endpoint [https://www.datos.gov.co/resource/6mhs-bztv.json] |
| Qué representa una fila | Contiene datos de los comparendos que han sido impuestos en los municipios incluidos en convenios interadministrativos con la Gerencia de Seguridad Vial de Antioquia, a partir del año 2021 |
| Campo que la identifica | fecha_comparendo, tipo_comparendo, tipo_veh_culo, estado_comparendo, valor_comparendo, punto_atenci_n, c_digo_infracci_n, descripci_n_infracci_n  |
| Cada cuánto se actualiza | Anualmente |
| Dato a confirmar | Según la información el valor _comparendo es numerico, sin embargo el json lo retorna texto, se debe hacer la conversión  |
| Tres indicadores | 1. Tasa de Morosidad sobre Cartera Total: Medir la efectividad del recaudo y justificar campañas de amnistía o descuentos por pronto pago. 2.Índice de Concentración de Infracciones: Enfocar los operativos en vía hacia las conductas que generan siniestros graves y no solo en multas administrativas. 3. Cantidad de infracciones por tipo de vehículo:Focalizar y especializar los operativos de control y prevención en el tipo de vehículo con mayor participación en infracciones críticas |
| Terminó bien si… | Terminó bien si el total de comparendos cargados es igual al conteo total de registros de la API en datos.gov.co (100% de los registros del periodo consultado), no existen registros duplicados y el campo tipo_veh_culo no tiene valores nulos o vacíos. Terminó bien si la suma de comparendos agrupados por tipo_veh_culo es exactamente igual al total de registros descargados, valor_comparendo está convertido a formato numérico sin errores y todas las fechas (fecha_comparendo) tienen un formato válido.|
| No vamos a construir | Predicción de comparendos por cada tipo de vehículo |

## Contrato de datos

- Una fila es:
- La identifica:
- Si llega una fila repetida:
- Si falta un campo:

## Bitácora de decisiones

| Fecha | Decisión | Por qué |
|---|---|---|
| | | |

## Reglas del repositorio

- Es público: nada de datos personales, contraseñas, tokens ni llaves.
- Las credenciales van en un archivo `.env`, que Git ignora (ver `.gitignore`). `.env.example` muestra qué variables hacen falta, sin valores.
- Cada commit explica en su mensaje qué se decidió y por qué.
