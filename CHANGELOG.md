# Changelog

Todos los cambios notables de este proyecto serán documentados en este archivo.

El formato está basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y este proyecto adhiere a [Semantic Versioning](https://semver.org/lang/es/).

## [2.0.1] - 2026-04-14

### Fixed
- 🐛 Corregido bug al editar posiciones que causaba error de validación de ticker
- 🐛 Mejorada validación de API para no re-validar ticker cuando no cambia

### Changed
- 📝 Mejorada documentación en README.md
- 📝 Agregados archivos para GitHub (LICENSE, CONTRIBUTING, etc.)

## [2.0.0] - 2026-04-14

### Added
- ✨ **Integración con Yahoo Finance API** para datos reales en tiempo real
- ✨ **Análisis técnico completo**: RSI, MACD, Moving Averages (50 y 200)
- ✨ **Sistema de recomendaciones automáticas** basado en indicadores técnicos
- ✨ **Detección de Golden Cross y Death Cross**
- ✨ **Sharpe Ratio** calculado automáticamente
- ✨ **Análisis de riesgo** por tipo de activo
- ✨ **Alertas de concentración** y apalancamiento excesivo
- ✨ **Auto-actualización** cada 5 minutos (configurable)
- ✨ **Indicador de estado de API** (conectada/error)
- ✨ **Gráfico de riesgo** por tipo de activo
- ✨ **Métricas avanzadas**: % en apalancados 3x, mejor posición, etc.
- 📊 **Tabla expandida** con RSI, MACD, MA50/200, señales de trading
- 🎨 **Badges de métricas** con colores según valores (verde/rojo/gris)

### Changed
- 🔄 Mejorado algoritmo de señales de trading (5 niveles: strong-buy, buy, hold, sell, strong-sell)
- 🔄 Optimizado cálculo de indicadores técnicos
- 🎨 Mejorada interfaz de usuario con más información visible
- 📱 Mejor responsive design para móviles

### Technical
- 📦 Agregado sistema de caché para datos de API
- ⚡ Optimizado performance de cálculos técnicos
- 🛡️ Mejorada gestión de errores de API

## [1.0.0] - 2026-04-14

### Added - Versión Inicial
- ✨ CRUD completo de posiciones
- ✨ Almacenamiento local en localStorage
- ✨ Gráfico de distribución del portfolio (pie chart)
- ✨ Gráfico de evolución histórica (line chart)
- ✨ Exportar/Importar datos en JSON
- ✨ Simulación de precios
- ✨ Cálculo de métricas básicas (valor total, retorno, mejor posición)
- ✨ Soporte para múltiples tipos de activos (acciones, ETFs, 3x, crypto, commodities)
- ✨ Dark mode automático
- ✨ Auto-actualización de precios simulados
- 📱 Diseño responsive
- 💾 Persistencia de datos en navegador

---

## Tipos de Cambios

- `Added` - Nuevas funcionalidades
- `Changed` - Cambios en funcionalidad existente
- `Deprecated` - Funcionalidades que se eliminarán pronto
- `Removed` - Funcionalidades eliminadas
- `Fixed` - Corrección de bugs
- `Security` - Cambios de seguridad

## Links

- [2.0.1] - https://github.com/TU_USUARIO/portfolio-tracker/releases/tag/v2.0.1
- [2.0.0] - https://github.com/TU_USUARIO/portfolio-tracker/releases/tag/v2.0.0
- [1.0.0] - https://github.com/TU_USUARIO/portfolio-tracker/releases/tag/v1.0.0
