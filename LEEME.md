# 🎮 Regalo de aniversario estilo Blood Strike

Un mini juego para celebrar con tu novia sus meses juntos:

1. 🔒 **Lobby**: bloqueado con cuenta regresiva hasta el día del aniversario.
2. 🎯 **Selección de Striker**: ella, con su foto y sus habilidades.
3. 🪂 **Fase 1, Caída**: dispara a los objetivos mientras se cierra la zona.
4. 📦 **Fase 2, Airdrop**: cae una caja, la abre y salen tarjetas de **loot legendario**, una por cada mes, con un recuerdo de ustedes.
5. 💬 **Fase 3, Chat del escuadrón**: tu mensaje, con su canción de fondo.
6. 💌 **Fase 4, Invitación**: *"¿Jugamos otra temporada juntos?"*. El botón de **RECHAZAR se escapa** 😏
7. 🏆 **#1 VICTORIA**: días como dúo, sus estadísticas y rango **Leyenda**.

## 1. Personalízalo (5 minutos)

Abre `index.html` con el Bloc de notas o VS Code y busca el bloque
**`CONFIGURACIÓN — EDITA SOLO ESTA PARTE`**, al inicio del `<script>`.
Cambia solo lo que está entre comillas:

| Campo | Qué poner |
|---|---|
| `nombre` | Su nombre o apodo |
| `nombreChat` | Tu nombre o apodo en el chat |
| `firma` | Tu despedida al final |
| `juntosDesde` | **El día en que empezaron**, en formato `AAAA-MM-DD`, por ejemplo `"2026-08-14"` |
| `meses` | Qué aniversario es: `2` = dos meses |
| `bloqueo` | `true` = se abre solo el día del aniversario · `false` = se abre siempre |
| `habilidades` | Las 4 habilidades de su Striker |
| `recuerdos` | Las tarjetas del airdrop: **un recuerdo por cada mes** `["título", "recuerdo"]` |
| `mensajes` | Tu mensaje: cada línea es un mensaje del chat |

En los mensajes, `{nombre}` se cambia por su nombre y `{meses}` por "2 meses".

La fecha del aniversario se calcula sola: si empezaron el **14 de agosto** y
`meses` es `2`, el regalo se desbloquea el **14 de octubre**.

⚠️ No borres las comillas `" "`, los corchetes `[ ]` ni las comas `,` del final.

## 2. Pon su foto y su canción

Copia estos archivos en esta misma carpeta, junto a `index.html`, con estos nombres exactos:

- **`foto.jpg`**: una foto de ella. Si no hay foto, se muestra su inicial.
- **`cancion.mp3`**: su canción. Suena desde el chat hasta el final.

Para que suene solo una parte (por ejemplo el coro), cambia en la configuración:

```js
cancionInicio: 40,   // empieza en 0:40
cancionFin: 120,     // termina en 2:00 y vuelve a empezar
```

(Los minutos se pasan a segundos: 1:30 = 90, 2:00 = 120.)

## 3. Pruébalo

Abre `index.html` con doble clic. Si sale **Partida bloqueada**, es porque todavía
no es el aniversario: agrega **`#prueba`** al final de la dirección para verlo completo.

> Si la foto o la canción no cargan con doble clic, súbelo a Netlify (paso 4) y
> pruébalo desde ahí.

## 4. Súbelo a internet gratis (Netlify Drop)

1. Entra a **https://app.netlify.com/drop**
2. Arrastra **la carpeta completa** a la página.
3. Te da un link tipo `https://algo-raro.netlify.app`. Para cambiarlo, crea una
   cuenta gratis y ve a **Site configuration → Change site name**.

Ese link es el que le mandas a ella. Antes del aniversario verá el lobby con la
cuenta regresiva, y se abrirá solo ese día a las 12:00 a.m. (hora de su celular).

🔒 Para revisarlo tú: el mismo link con **`#prueba`** al final. No se lo mandes así.

## Ojo

- El link es público: cualquiera que lo tenga ve su foto. Compártelo solo con ella.
- Si subes la canción completa, queda descargable desde el link. No lo publiques en redes.
