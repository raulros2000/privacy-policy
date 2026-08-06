# privacy-policy — Políticas legales de todos los juegos

Repositorio único para crear y mantener las políticas de privacidad y términos
de todos los juegos, con **una subcarpeta por juego**:

```
privacy-policy/
├── index.html            # índice público con enlaces a todos los juegos
├── bloque-rojo/          # Bloque Rojo (privacidad, términos, eliminar cuenta)
└── bloques-8x8/          # Bloques 8×8 (privacidad, términos)
```

Cada página incluye los 4 idiomas (es/en/pt/it) con anclas `#es #en #pt #it`.

## Publicación (GitHub Pages)

1. Crear el repo `privacy-policy` en GitHub (usuario `raulros2000`) y hacer push.
2. En GitHub: Settings → Pages → Deploy from branch → `main` / root.
3. URLs resultantes:
   - `https://raulros2000.github.io/privacy-policy/bloques-8x8/privacy-policy.html`
   - `https://raulros2000.github.io/privacy-policy/bloque-rojo/privacy-policy.html`

## Estado por juego

| Juego | Fuente en la app | URL pública en uso |
|-------|------------------|--------------------|
| **Bloques 8×8** | `bloques_tablero_8x8/lib/core/legal/legal_texts.dart` | La de este repo (pendiente de publicar) |
| **Bloque Rojo** | `bloque_rojo/lib/core/legal/legal_texts.dart` | ⚠️ Aún apunta al repo antiguo `bloque-rojo-legal`; migrar aquí con su próxima actualización de app (cambiar `kPrivacyPolicyUrl`/`kTermsUrl` y la ficha de Play). Hasta entonces, mantener el repo antiguo publicado. |

## Añadir un juego nuevo

1. Crear subcarpeta `<juego>/` con `privacy-policy.html` y `terms.html`
   (copiar una existente como plantilla y adaptar nombre + secciones).
2. Añadir sus enlaces a `index.html`.
3. Poner la URL en el `kPrivacyPolicyUrl` de la app y en su ficha de Play.

## Regla de oro

Si el comportamiento de datos de un juego cambia (analítica, anuncios,
cuentas…), actualizar su página aquí **y** el texto dentro de la app
(`legal_texts.dart`), subiendo la versión de términos para re-pedir
consentimiento.
