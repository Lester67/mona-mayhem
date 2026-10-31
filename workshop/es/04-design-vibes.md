<!-- l10n-sync: source-file="04-design-vibes.md" -->
# Parte 4: Tematización con diseño primero

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación de tema completa. Este es un desarrollo con diseño primero: empieza con la visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el Tema Retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo plan.
<!-- track:cli:end -->

Ingresa este prompt:

> I want to transform this page into a full retro arcade experience. Plan a comprehensive visual overhaul that includes: CRT scanline effects on the background, neon glow on the title that pulses like a neon sign, animated VS badge with gradient color shifts, shine/shimmer overlay on the user result cards, float-in animations for input fields, color-shifting loading text between green and purple, and hover glow effects on contribution squares. Keep the dark background (#0a0a1a) with green (#5fed83) and purple (#8a2be2) accent colors. Use a dark theme with the Press Start 2P retro gaming font from Google Fonts.

Copilot generará un plan detallado de implementación cubriendo todos los efectos visuales. **No lo aceptes de inmediato** — revisa el plan e itera:

- Sugiere ajustes en la velocidad de las animaciones (por ejemplo, "Make the neon pulse slower, around 3 seconds")
- Pregunta sobre efectos específicos (por ejemplo, "How will the shimmer overlay work on the cards?")
- Solicita cambios en el enfoque si algo no te convence

Cuando estés satisfecho con el plan, pide a Copilot que lo implemente.

## Tarea 2: Implementa el Tema

> Implement the retro arcade theme plan we just designed.

Copilot agregará múltiples animaciones CSS, pseudo-elementos y transiciones en tu hoja de estilos. Esto puede incluir:

- `@keyframes` para scanlines, pulso neón, shimmer y efectos de aparición flotante
- Pseudo-elementos (`::before`, `::after`) para efectos de superposición
- CSS custom properties para los colores del tema
- Transiciones y estados hover para elementos interactivos

<!-- track:cli:start -->
Después de aplicar los cambios, usa `/diff` para revisar los cambios de estilo antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Perfecciona el diseño

> **⚠️ ¿No ves los cambios?** Si el nuevo tema o las animaciones no aparecen, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y actualiza el navegador con una recarga forzada (`Ctrl+Shift+R`).

Mantén la vista previa del navegador abierta e itera sobre el diseño. Prueba prompts como:

> The scanline effect is too strong, reduce opacity to 0.03

> Add a subtle electrical flicker to the title text

> The VS badge should pulse more dramatically

Esto es **desarrollo orientado al diseño** — estás iterando sobre el resultado visual en tiempo real. Cada prompt perfecciona la experiencia hasta que tenga el aspecto adecuado. No te conformes con un resultado aceptable: ajusta el diseño hasta que la página parezca propia de una máquina arcade.

## Tarea 4: Actualiza las Instrucciones

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Add a design guide section to copilot-instructions.md describing our retro arcade theme: colors, fonts, animation style
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Update our repository instructions with a short design guide for the retro arcade theme: colors, fonts, animation style, and the rule that new UI should keep the neon aesthetic.
<!-- track:cli:end -->

Haz commit de las instrucciones actualizadas y de los cambios de diseño cuando la página tenga el aspecto adecuado.

## ✅ Parte 4 Completa

**Lo que aprendiste:**

- Usar flujos de planificación para esbozar un **sistema de diseño antes de implementarlo**
- **Iterar sobre el resultado visual** con prompts de seguimiento breves
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener una identidad visual coherente
