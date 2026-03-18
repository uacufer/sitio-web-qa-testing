TEST 1: Validez HTML 
• Opción 1: 
o Herramienta: W3C Validator. 
o Acción: Sube tu archivo index.html (pestaña "Validate by File Upload"). 
o Criterio de éxito: Documento verde (Pass). Se aceptan máximo 3 warnings, 
pero 0 errores. 

• Opción 2: 
o Usa un validador local: 
npm install -g nu-html-checker 
html-checker index.html 
o Mismo criterio de éxito. 

TEST 2: Auditoría Accesibilidad (WAVE) 
• Herramienta: Extensión WAVE para Chrome/Firefox. 
• Acción: Abre tu index.html en el navegador y activa la extensión. 
• Criterio de éxito: 0 Errores rojos. Las alertas amarillas son aceptables si están 
justificadas (máximo 5 alertas).

TEST 3: Estrés Responsive 
• Herramienta: DevTools (F12) -> Device Mode. 
• Acción: Prueba en 3 anchos clave: 
o 320px (Móvil): 
▪ [ ] Sin scroll horizontal 
▪ [ ] Botones ≥48px 
▪ [ ] Texto ≥14px 
▪ [ ] Imágenes escalan 
▪ [ ] Navegación adaptada o 768px (Tablet): 
[ ] Grid 2 columnas 
[ ] Espaciado adecuado o 1440px (Desktop): 
[ ] Grid 3 columnas 
[ ] Max-width respetado 
• Criterio de éxito: Diseño fluido sin roturas. 

TEST 4: Contraste de Color (WCAG) 
• Herramienta: Color Contrast Analyzer (o la herramienta de DevTools). 
• Acción: Mide el color del texto gris oscuro contra el fondo blanco y el azul de los 
enlaces. 
• Criterio de éxito: Ratio mínimo de 4.5:1 (AA). 

TEST 5: Navegación por Teclado (Focus) 
• Herramienta: Tu tecla TAB. 
• Acción: Navega por toda la web sin usar el ratón. 
o [ ] Links 
o [ ] Buttons 
o [ ] Form inputs 
o [ ] Navigation items 
• Criterio de éxito: Debes ver siempre un recuadro (outline) azul grueso en el elemento seleccionado. 

TEST 6: Rendimiento (Lighthouse) 
• Herramienta: DevTools -> Pestaña Lighthouse. 
• Acción: Genera un reporte en modo "Mobile". 
• Criterio de éxito: Puntuaciones verdes (>90) en Performance, Accessibility y Best 
Practices .