# Contribuir a Portfolio Tracker Pro

¡Gracias por tu interés en contribuir! 🎉

## 🚀 Cómo Contribuir

### Reportar Bugs 🐛

Si encuentras un bug:

1. Verifica que no esté ya reportado en [Issues](https://github.com/TU_USUARIO/portfolio-tracker/issues)
2. Abre un nuevo Issue con:
   - Descripción clara del problema
   - Pasos para reproducir
   - Comportamiento esperado vs actual
   - Capturas de pantalla (si aplica)
   - Navegador y versión

**Template de Bug Report:**
```markdown
**Descripción del bug**
[Descripción clara y concisa]

**Pasos para reproducir**
1. Ir a '...'
2. Hacer clic en '...'
3. Ver error

**Comportamiento esperado**
[Qué debería pasar]

**Capturas**
[Si aplica]

**Entorno**
- Navegador: [Chrome 120]
- OS: [Windows 11]
- Versión: [2.0]
```

### Sugerir Funcionalidades ✨

1. Abre un Issue con tag `enhancement`
2. Describe la funcionalidad y por qué sería útil
3. Si es posible, sugiere cómo implementarla

### Pull Requests 🔧

1. **Fork** el repositorio
2. **Crea una rama** desde `main`:
   ```bash
   git checkout -b feature/nombre-descriptivo
   # o
   git checkout -b fix/descripcion-del-bug
   ```

3. **Haz tus cambios**:
   - Código limpio y comentado
   - Sigue el estilo existente
   - Prueba tus cambios

4. **Commit** con mensajes descriptivos:
   ```bash
   git commit -m "feat: agregar indicador Bollinger Bands"
   # o
   git commit -m "fix: corregir cálculo de RSI en mercados volátiles"
   ```

5. **Push** a tu fork:
   ```bash
   git push origin feature/nombre-descriptivo
   ```

6. **Abre un Pull Request**:
   - Describe qué cambios hiciste y por qué
   - Referencia issues relacionados (#123)
   - Incluye capturas si hay cambios visuales

## 📝 Estilo de Código

### HTML
```html
<!-- Buenos nombres de clase descriptivos -->
<div class="stat-card">
  <div class="stat-label">Valor Total</div>
  <div class="stat-value">$100,000</div>
</div>
```

### CSS
```css
/* Usa variables CSS para colores */
.stat-card {
  background: var(--bg-primary);
  color: var(--text-primary);
  padding: 20px;
}
```

### JavaScript
```javascript
// Funciones descriptivas con comentarios
/**
 * Calcula el RSI de un array de precios
 * @param {number[]} prices - Array de precios de cierre
 * @param {number} period - Período para el cálculo (default 14)
 * @returns {number} - Valor RSI entre 0-100
 */
function calculateRSI(prices, period = 14) {
  // Implementación
}

// Nombres de variables claros
const currentPrice = position.currentPrice;
const dailyChange = ((currentPrice - previousClose) / previousClose) * 100;
```

## 🧪 Testing

Antes de hacer PR, prueba:

1. ✅ Agregar nueva posición con ticker válido
2. ✅ Agregar ticker inválido (debe mostrar error)
3. ✅ Editar posición existente
4. ✅ Eliminar posición
5. ✅ Actualizar precios (manual y auto)
6. ✅ Exportar/Importar datos
7. ✅ Responsive en móvil
8. ✅ Dark mode funciona correctamente

## 🎯 Áreas de Contribución

### Fácil 🟢
- Mejorar documentación
- Corregir typos
- Agregar ejemplos
- Traducciones

### Media 🟡
- Nuevos indicadores técnicos
- Mejorar UI/UX
- Optimizar performance
- Agregar tests

### Difícil 🔴
- Integración con brokers
- Machine Learning
- Backend opcional
- PWA / App móvil

## 📚 Recursos Útiles

- [JavaScript Style Guide](https://github.com/airbnb/javascript)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Chart.js Docs](https://www.chartjs.org/docs/)
- [Yahoo Finance API](https://finance.yahoo.com)

## ⚠️ Notas Importantes

- **No commits directos a `main`** - siempre usa branches
- **Un PR por funcionalidad** - no mezcles múltiples features
- **Mantén compatibilidad** - no rompas funcionalidad existente
- **Documenta cambios** - actualiza README si es necesario

## 💬 ¿Dudas?

Si tienes preguntas, abre un [Discussion](https://github.com/TU_USUARIO/portfolio-tracker/discussions) o comenta en un Issue existente.

---

**¡Gracias por hacer de Portfolio Tracker Pro una mejor herramienta para todos! 🚀**
