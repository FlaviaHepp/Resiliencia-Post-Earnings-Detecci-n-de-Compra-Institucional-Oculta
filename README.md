# 📊Resiliencia Post-Earnings: Detección de Compra Institucional Oculta

## 🧠Descripción general

Este proyecto identifica acciones que muestran fortaleza estructural tras un reporte de Ganancias negativo, incluso cuando el mercado reacciona inicialmente con un gap bajista.

La lógica central busca señales de absorción institucional: situaciones donde, pese a una mala noticia aparente, el precio logra recuperarse intradía y el momentum se mantiene saludable.

Este patrón es conocido como “Glass Box Resilience” o absorción silenciosa, y suele preceder movimientos alcistas posteriores.

## 🎯Objetivo del análisis

Detectar empresas que cumplen simultáneamente con:
- Gap bajista en la apertura tras el anuncio de Ganancias
- Recuperación intradía significativa (cierre en la parte superior del rango diario)
- Momentum positivo sostenido (RSI > 50)

👉 Interpretación: el mercado minorista vende por pánico, mientras “manos fuertes” compran agresivamente.

## 📈Insight de negocio

- Identificar oportunidades de compra institucional oculta detrás de noticias aparentemente negativas.

Este tipo de configuración suele anticipar:

- Suelos de corto/medio plazo
- Reversiones alcistas inesperadas
- Acumulación previa a revalorizaciones
- Es especialmente útil para:
- Trading de swing
- Confirmación de setups fundamentales
- Detección temprana de “false negatives” del mercado

## 🧩Lógica del modelo

La consulta filtra acciones que cumplen:
- Evento corporativo
- Tipo: Ganancias
- Gap bajista
- Precio de apertura menor al cierre del día anterior
- Recuperación intradía
- El cierre se ubica en el 30% superior del rango diario

Métrica usada:

(Close - Low) / (High - Low) > 0.7


- Momentum saludable

RSI de 14 períodos mayor a 50

## 🗂️ Tablas utilizadas

- eventos_corporativos
- precios_diarios
- indicadores_tecnicos
- tickers

## 📤Salida del modelo

El resultado devuelve:
- ticker_id → Acción identificada
- fecha_reporte → Fecha del anuncio de Ganancias
- posicion_cierre_rango → Qué tan fuerte cerró dentro del rango diario
- rsi_14 → Estado del momentum tras el evento

Estas acciones representan candidatos de alta convicción para análisis posterior.

## ⚠️Consideraciones

- No implica una señal automática de compra

Debe combinarse con:
- Contexto de mercado
- Liquidez
- Tendencia de marco temporal superior
- Funciona mejor en mercados líquidos y con cobertura institucional

## 🔮Extensiones posibles

- Medir rendimiento a 5, 10 y 20 días post-evento
- Cruzar con volumen anómalo (confirmación institucional)
- Analizar por sector o país
- Integrar con detección de divergencias RSI–precio

## 🧠Conclusión

Este proyecto transforma un evento negativo en una ventana de oportunidad informacional, revelando cuándo el mercado “dice una cosa” pero el capital inteligente hace otra.

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
