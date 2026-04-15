# 📊 Portfolio Tracker Pro

**Sistema profesional de seguimiento y análisis de portfolios de inversión con datos en tiempo real y recomendaciones automáticas basadas en análisis técnico.**

![Version](https://img.shields.io/badge/version-2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## 🌟 **Características Principales**

### 📈 **Datos en Tiempo Real**
- ✅ Conexión directa a Yahoo Finance API
- ✅ Precios actualizados de acciones, ETFs, criptomonedas y commodities
- ✅ Historial de 30 días automático
- ✅ Auto-actualización cada 5 minutos (configurable)

### 🎯 **Análisis Técnico Completo**
- ✅ **RSI (14)** - Relative Strength Index
- ✅ **MACD** - Moving Average Convergence Divergence
- ✅ **Moving Averages** (50 y 200) - Golden Cross / Death Cross
- ✅ **Sharpe Ratio** - Retorno ajustado por riesgo
- ✅ **Análisis de Volatilidad** por tipo de activo

### 🤖 **Sistema de Recomendaciones Automáticas**
- 🟢 **COMPRA FUERTE**: RSI sobrevendido + MACD alcista
- 🔴 **VENTA FUERTE**: RSI sobrecomprado + MACD bajista
- ⭐ **Golden Cross**: MA50 > MA200 (señal alcista)
- ⚠️ **Death Cross**: MA50 < MA200 (señal bajista)
- 📊 **Alertas de Riesgo**: Concentración excesiva, apalancamiento alto

### 💾 **Gestión de Datos**
- ✅ CRUD completo (Crear, Leer, Actualizar, Eliminar)
- ✅ Almacenamiento local en navegador (localStorage)
- ✅ Exportar/Importar datos en JSON
- ✅ Número ilimitado de posiciones

### 📊 **Visualización**
- ✅ Gráfico de distribución del portfolio (pie chart)
- ✅ Gráfico de riesgo por tipo de activo (bar chart)
- ✅ Evolución histórica del portfolio (line chart)
- ✅ Dashboard con métricas clave en tiempo real

---

## 🚀 **Inicio Rápido**

### **Opción 1: Usar Directamente (Recomendado)**

1. **Descarga el archivo**
   ```bash
   wget https://raw.githubusercontent.com/TU_USUARIO/portfolio-tracker/main/portfolio-tracker-advanced.html
   ```

2. **Abre el archivo en tu navegador**
   - Doble clic en `portfolio-tracker-advanced.html`
   - O arrastra el archivo a Chrome/Firefox/Safari/Edge

3. **¡Listo! Ya funciona**
   - No requiere instalación
   - No necesita servidor
   - 100% offline después de la primera carga

### **Opción 2: Desde GitHub Pages**

Visita: `https://TU_USUARIO.github.io/portfolio-tracker/portfolio-tracker-advanced.html`

### **Opción 3: Clonar Repositorio**

```bash
git clone https://github.com/TU_USUARIO/portfolio-tracker.git
cd portfolio-tracker
# Abre portfolio-tracker-advanced.html en tu navegador
```

---

## 📖 **Guía de Uso**

### **1️⃣ Agregar una Posición**

1. Clic en **"➕ Agregar Posición"**
2. Completa los campos:
   - **Ticker**: Símbolo de Yahoo Finance (ej: GOOGL, AAPL, QQQ)
   - **Tipo**: Acción, ETF, 3x Apalancado, Crypto, Commodity
   - **Acciones**: Cantidad que posees
   - **Precio promedio**: Tu precio de compra

3. Clic en **"Guardar"**
   - La app validará el ticker automáticamente
   - Descargará datos históricos y técnicos

### **2️⃣ Símbolos Válidos**

La app usa símbolos de **Yahoo Finance**:

| Tipo | Ejemplos |
|------|----------|
| **Acciones** | GOOGL, AAPL, TSLA, NVDA, MSFT |
| **ETFs** | QQQ, VOO, SPY, IWM, VTI |
| **ETFs 3x** | TQQQ, SOXL, UPRO, TECL, FNGU |
| **Criptomonedas** | BTC-USD, ETH-USD, SOL-USD |
| **Commodities** | GC=F (oro), SI=F (plata), CL=F (petróleo) |

**Tip**: Busca el símbolo en [finance.yahoo.com](https://finance.yahoo.com)

### **3️⃣ Actualizar Precios**

- **Manual**: Clic en **"🔄 Actualizar Precios"**
- **Automático**: Activa el toggle **"Auto (5min)"**
  - Se actualizará cada 5 minutos
  - Perfecto para monitoreo continuo

### **4️⃣ Ver Recomendaciones**

El panel de recomendaciones aparece automáticamente cuando detecta:

- 🟢 Oportunidades de compra (RSI bajo + momentum positivo)
- 🔴 Señales de venta (RSI alto + momentum negativo)
- ⭐ Golden/Death Cross (cambios de tendencia)
- ⚠️ Alertas de riesgo (concentración, apalancamiento)

### **5️⃣ Editar/Eliminar Posiciones**

- **Editar**: Clic en ✏️ → Modifica campos → Guardar
- **Eliminar**: Clic en 🗑️ → Confirmar

---

## 🎨 **Capturas de Pantalla**

### Dashboard Principal
*(Agrega aquí una captura de pantalla del dashboard)*

### Panel de Recomendaciones
*(Agrega aquí una captura del panel de recomendaciones)*

### Análisis Técnico
*(Agrega aquí una captura de la tabla con indicadores)*

---

## 🔧 **Configuración Avanzada**

### **Modificar Parámetros de Indicadores**

Edita el archivo HTML directamente:

```javascript
// Cambiar período RSI (línea ~450)
const rsi = calculateRSI(closes, 14); // Cambia 14 a 7 para más sensibilidad

// Cambiar frecuencia auto-update (línea ~1050)
autoUpdateInterval = setInterval(updateAllPrices, 300000); // 300000ms = 5min

// Ajustar umbrales de señales (línea ~380)
if (tech.rsi < 30) // Cambia a 25 para señales más agresivas
if (tech.rsi > 70) // Cambia a 75 para señales más conservadoras
```

### **Agregar Indicadores Personalizados**

```javascript
// Ejemplo: Agregar Bollinger Bands
function calculateBollingerBands(prices, period = 20, stdDev = 2) {
  const ma = calculateMA(prices, period);
  const variance = prices.slice(-period).reduce((sum, p) => 
    sum + Math.pow(p - ma, 2), 0) / period;
  const std = Math.sqrt(variance);
  
  return {
    upper: ma + (stdDev * std),
    middle: ma,
    lower: ma - (stdDev * std)
  };
}
```

---

## 📊 **Indicadores Técnicos**

### **RSI (Relative Strength Index)**
- **Rango**: 0-100
- **Sobrecomprado**: >70
- **Sobrevendido**: <30
- **Neutral**: 40-60

**Interpretación**:
- RSI < 30 → Posible rebote alcista
- RSI > 70 → Posible corrección bajista

### **MACD (Moving Average Convergence Divergence)**
- **Fórmula**: EMA(12) - EMA(26)
- **Positivo**: Momentum alcista
- **Negativo**: Momentum bajista

**Interpretación**:
- MACD > 0 → Presión compradora
- MACD < 0 → Presión vendedora

### **Moving Averages (50 y 200)**
- **Golden Cross**: MA50 cruza arriba de MA200 (alcista)
- **Death Cross**: MA50 cruza abajo de MA200 (bajista)

**Interpretación**:
- MA50 > MA200 → Tendencia alcista de largo plazo
- MA50 < MA200 → Tendencia bajista de largo plazo

### **Sharpe Ratio**
- **Fórmula**: Retorno promedio / Volatilidad
- **>1.0**: Excelente riesgo-retorno
- **0.5-1.0**: Bueno
- **<0.5**: Pobre

---

## 🔒 **Privacidad y Seguridad**

- ✅ **100% Local**: Todos los datos se guardan en tu navegador
- ✅ **Sin Servidor**: No enviamos datos a ningún servidor externo
- ✅ **Sin Registro**: No requiere cuenta ni email
- ✅ **API Pública**: Yahoo Finance API es gratuita y pública
- ✅ **Open Source**: Código completamente auditable

**Datos que se almacenan localmente**:
- Posiciones del portfolio (ticker, cantidad, precio)
- Historial de precios (30 días)
- Indicadores técnicos calculados
- Configuración de auto-update

**NO se almacena**:
- Información personal
- Credenciales de broker
- Números de cuenta
- Datos bancarios

---

## 🚨 **Limitaciones y Consideraciones**

### **API de Yahoo Finance**
- **Límite**: ~2,000 requests/hora (gratuito)
- **Con 10 posiciones**: 120 requests/hora (auto-update 5min)
- **Solución si excedes**: Aumentar intervalo a 10-15 min

### **Datos Históricos**
- Máximo 30 días de historial automático
- Para más datos, usa el backtesting manual

### **Precisión de Indicadores**
- RSI y MACD son calculados desde datos de cierre
- No considera gaps overnight ni pre/post-market
- Usa como guía, no como única fuente de decisiones

### **Disclaimer**
⚠️ **Este software es solo para fines educativos e informativos.**
- No constituye asesoramiento financiero
- No garantiza resultados de inversión
- Siempre consulta con un profesional antes de invertir
- Invierte solo lo que puedas permitirte perder

---

## 🛠️ **Tecnologías**

- **HTML5** - Estructura
- **CSS3** - Estilos (con soporte para dark mode)
- **JavaScript (Vanilla)** - Lógica y cálculos
- **Chart.js** - Gráficos interactivos
- **Yahoo Finance API** - Datos de mercado
- **localStorage** - Persistencia de datos

**Sin dependencias backend**:
- No requiere Node.js
- No requiere Python
- No requiere base de datos
- 100% cliente-side

---

## 📝 **Roadmap**

### **v2.1 (Próximo)**
- [ ] Alertas por email/SMS
- [ ] Exportar a PDF
- [ ] Más indicadores (Bollinger Bands, Stochastic)
- [ ] Comparación con benchmarks (S&P 500, Nasdaq)

### **v2.2**
- [ ] Backtesting histórico (1-5 años)
- [ ] Simulador de trades
- [ ] Machine Learning para predicciones

### **v3.0**
- [ ] Conexión con brokers (solo lectura)
- [ ] Modo multi-portfolio
- [ ] Sync en la nube (opcional)

---

## 🤝 **Contribuir**

¡Las contribuciones son bienvenidas!

1. **Fork** el repositorio
2. Crea una **rama** (`git checkout -b feature/nueva-funcionalidad`)
3. **Commit** tus cambios (`git commit -m 'Agregar nueva funcionalidad'`)
4. **Push** a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un **Pull Request**

### **Áreas donde puedes contribuir**:
- 🐛 Reportar bugs
- ✨ Sugerir nuevas funcionalidades
- 📖 Mejorar documentación
- 🌍 Traducciones
- 🎨 Diseño UI/UX
- 📊 Nuevos indicadores técnicos

---

## 📄 **Licencia**

MIT License - Ver [LICENSE](LICENSE) para más detalles.

**En resumen**: Puedes usar, modificar y distribuir libremente este proyecto, incluso para fines comerciales, siempre que incluyas el aviso de copyright original.

---

## 👨‍💻 **Autor**

Creado con ❤️ para la comunidad de inversores.

**Contacto**:
- GitHub: [@TU_USUARIO](https://github.com/TU_USUARIO)
- Email: tu_email@ejemplo.com

---

## ⭐ **Apoya el Proyecto**

Si este proyecto te fue útil:
- ⭐ Dale una estrella en GitHub
- 🐛 Reporta bugs
- 💡 Sugiere mejoras
- 🔗 Compártelo con otros inversores

---

## 📚 **Recursos Adicionales**

- [Yahoo Finance API Docs](https://finance.yahoo.com)
- [Análisis Técnico - Investopedia](https://www.investopedia.com/technical-analysis-4689657)
- [Chart.js Documentation](https://www.chartjs.org/docs/)

---

## ❓ **FAQ**

### **¿Es gratis?**
Sí, 100% gratuito y open source.

### **¿Necesito API key?**
No, la API de Yahoo Finance es pública.

### **¿Funciona offline?**
Después de la primera carga y actualización, puedes ver tus datos offline. Para actualizar precios necesitas internet.

### **¿Mis datos están seguros?**
Sí, todo se guarda localmente en tu navegador. Nada se envía a servidores externos.

### **¿Puedo usar en móvil?**
Sí, el diseño es responsive y funciona en tablets y smartphones.

### **¿Qué navegadores son compatibles?**
Chrome, Firefox, Safari, Edge (versiones modernas).

---

**¿Preguntas? Abre un [Issue](https://github.com/TU_USUARIO/portfolio-tracker/issues)**
