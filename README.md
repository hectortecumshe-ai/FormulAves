# FormulAves

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23094626.svg)](https://doi.org/10.5281/zenodo.23094626)

**Plataforma guiada para la formulación de dietas de mínimo costo para pollo de engorda.**

👉 **Usar la aplicación:** https://hectortecumshe-ai.github.io/FormulAves/

FormulAves es una aplicación web de un solo archivo (`index.html`) que funciona por completo en el navegador: no requiere instalación ni servidor, y ningún dato sale de la computadora del usuario.

## Qué hace

La formulación se organiza en bloques, cada uno con su marco teórico:

1. **Línea genética y sexo**: Ross 308, Arbor Acres Plus, Cobb 500, Hubbard Efficiency Plus, pollo criollo o de crecimiento lento, NRC (1994) o un perfil personalizado (p. ej., NASEM 2025 o Tablas Brasileñas 2024).
2. **Etapa y requerimientos**: requerimientos editables por fase, con el perfil de proteína ideal.
3. **Condiciones de producción**: altitud (ascitis), estrés por calor (balance electrolítico), tamaño del lote y pigmentación.
4. **Ingredientes**: 29 materias primas con aminoácidos totales y digestibles; matriz editable.
5. **Precios y límites de inclusión**.
6. **Formulación de mínimo costo**: programación lineal (símplex en dos fases), precios sombra, precio de entrada de ingredientes y certificado de optimalidad por dualidad.
7. **Programa multifase**: todas las fases a la vez, con el costo de alimento por ave y por kg de peso vivo.
8. **Informe**: resumen, impresión en PDF, exportación a CSV y guardado del proyecto.

**Dos vistas (botón Productor / Científico):** la de productor muestra lo esencial en lenguaje sencillo, con hoja de mezclado en kg, costo por pollo y consejos en cada paso; la científica muestra el modelo de programación lineal, precios sombra, costos reducidos, certificado de dualidad, los 20 nutrientes, la validación y las referencias, con exportación del modelo en JSON.

**Ayuda contextual:** cada parámetro, índice e indicador tiene un signo **?** que, al pasar el mouse (o tocarlo en el celular), muestra su concepto y su escala de decisión.

## Validación

- Se reprodujeron 8 dietas publicadas en 4 artículos (Rev. Mex. Cienc. Pecu. 2020; *Animals* 2025 ×2; *Poultry* 2022). El error medio en el análisis calculado fue de 0.9 % en energía metabolizable y de 2.7 % en proteína cruda.
- Al reformular con los mismos ingredientes y el mismo aporte, la app reencontró exactamente las 6 fórmulas publicadas evaluables.
- El motor de optimización se comparó con HiGHS (SciPy) en 400 problemas aleatorios, con resultados idénticos (diferencia relativa máxima de 5×10⁻¹⁴).

El detalle está en la pestaña **Validación** de la aplicación.

## Cómo citar

Mojica-Zárate, H. T., y Barrera-Guzmán, L. A. (2026). *FormulAves: Plataforma guiada para la formulación de dietas de mínimo costo para pollo de engorda* (Versión 2.1.0) [Software]. https://doi.org/10.5281/zenodo.23094626

## Autores

- Héctor Tecumshé Mojica Zárate
- Luis Ángel Barrera Guzmán

> Herramienta de apoyo: los resultados deben ser revisados por un profesional en nutrición animal.
