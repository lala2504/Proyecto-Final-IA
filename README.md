# Agente de finanzas personales

Proyecto final de la asignatura Inteligencia Artificial.

## Integrantes

- Santiago Bedoya Posada
- Alejandro Gutierrez Muñoz
- Laura Franco Berrío

## Problema

Las personas suelen tener registros de ingresos y gastos, pero no siempre cuentan con una forma sencilla de interpretarlos. Este proyecto desarrollará un agente que consulte movimientos financieros mensuales, realice cálculos verificables y explique los resultados en lenguaje natural.

El prototipo está dirigido a personas que dispongan de un archivo mensual con la estructura utilizada por los datos sintéticos del proyecto.

## Alternativa elegida

**Opción B: agente con herramientas.**

El agente utilizará funciones implementadas con pandas. El modelo de lenguaje decidirá qué herramienta necesita, proporcionará sus argumentos y explicará el resultado. Los cálculos no serán realizados directamente por el modelo.

## Herramientas previstas

1. `resumen_mensual(mes)`: calcula ingresos, gastos, ahorro o inversión, balance e indicadores del mes solicitado.
2. `analizar_gastos(mes, categoria=None)`: analiza totales, porcentajes, frecuencia y principales categorías o transacciones.
3. `detectar_alertas(mes)`: identifica gastos superiores a los ingresos, ahorro bajo y movimientos atípicos.

Las herramientas serán de solo lectura. No modificarán el archivo de datos ni realizarán operaciones sobre cuentas financieras.

## Alcance

- Análisis mes a mes.
- Consultas sobre los datos sintéticos suministrados.
- Cálculos determinísticos con pandas.
- Respuestas explicadas en español.
- Máximo de tres llamadas a herramientas por consulta.

## Fuera del alcance

- Actualización de datos en tiempo real.
- Modificación de información financiera.
- Acceso o manipulación de cuentas bancarias.
- Envío de notificaciones.
- Análisis de finanzas grupales.
- Simulación de reducción de gastos o ahorro potencial.
- Monitoreo en periodos diferentes al mensual.

## Estructura

```text
Proyecto Final/
├── README.md
├── agente_financiero.ipynb
├── requirements.txt
├── .env.example
├── data/
│   └── finanzas_personales_sinteticas.xlsx
├── ejemplos clase/
├── src/
├── tests/
└── resultados/
```

- `agente_financiero.ipynb`: desarrollo y demostración principal.
- `data/`: datos de entrada. El prototipo los consulta sin modificarlos.
- `ejemplos clase/`: notebooks de referencia suministrados en clase.
- `src/`: módulos reutilizables cuando el código del notebook se estabilice.
- `tests/`: definición y evidencia de los cinco casos de prueba.
- `resultados/`: salidas de pruebas que sea necesario conservar.

## Instalación inicial

1. Crear y activar un entorno virtual.
2. Instalar las dependencias:

```bash
pip install -r requirements.txt
```

3. Copiar `.env.example` como `.env` y configurar la clave del proveedor elegido.
4. Abrir `agente_financiero.ipynb` y ejecutar las celdas en orden.

No se deben publicar claves de API ni archivos `.env` en el repositorio.

## Estado actual

- [X] Problema y alcance definidos.
- [X] Datos sintéticos disponibles.
- [X] Estructura inicial creada.
- [X] Carga y validación de datos.
- [X] Implementación y pruebas unitarias de las herramientas.
- [X] Construcción del agente con LangGraph.
- [X] Límite de llamadas a herramientas.
- [X] Cinco casos de prueba y análisis de resultados.
