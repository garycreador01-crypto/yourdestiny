# YourDestiny

Página web de una agencia de viajes hecha como proyecto de clase (Parcial 2). La idea es sencilla: tú eliges tu presupuesto (barato, medio o caro) y la página te muestra al instante el vuelo, el hotel y el auto que te corresponden, además de un itinerario armado para ese presupuesto.

🔗 **Míralo funcionando:** https://garycreador01-crypto.github.io/yourdestiny/

---

## ¿Qué tiene la página?

- **Inicio con video:** un video de playa se repite en bucle de fondo, con el título, los botones y unos contadores que suben solos.
- **Cinta de destinos:** una franja que se mueve sin parar con los lugares que ofrecemos.
- **Destinos:** tres tarjetas (Caribe, Ballenas del Pacífico y Ciudad Perdida) que se animan al pasar el mouse.
- **Cotización:** tres botones (Económico, Medio, Premium). Al elegir uno cambian el vuelo, el hotel, el auto y el total del viaje.
- **Itinerario:** otros tres botones (Barato, Medio, Caro). Cambian las actividades de cada día y el hotel recomendado según el presupuesto.
- **Se adapta al celular:** en pantallas pequeñas todo se acomoda en una sola columna.

---

## ¿Con qué está hecho?

Solo con **HTML y CSS**. No usamos JavaScript, ni librerías, ni frameworks. Todo lo que se mueve o se filtra lo hace el CSS.

| Tecnología | Para qué la usamos |
|---|---|
| HTML5 | La estructura de la página |
| CSS3 | Colores, diseño, animaciones y filtros |
| GitHub Pages | Publicar la página gratis |

---

## ¿Cómo filtra sin JavaScript?

Esta fue la parte que más nos gustó. El truco funciona así:

1. En el HTML hay tres botones de opción (`<input type="radio">`) escondidos.
2. Cada botón bonito que ves es en realidad un `<label>` conectado a uno de esos radios.
3. Cuando haces clic, el radio queda marcado y el CSS lo detecta con `:checked`.
4. Con el símbolo `~` el CSS busca el grupo que viene después y le pone `display: grid`. Los demás grupos quedan en `display: none`.

Por ejemplo, esta línea significa: "si el radio `q2` está marcado, muestra el grupo del presupuesto medio":

```css
#q2:checked ~ .w .t2 { display: grid; }
```

Todo esto está explicado paso a paso con comentarios en la sección 8 de `css/styles.css`.

---

## Estructura del proyecto

```
yourdestiny/
├── index.html        → todo el contenido de la página
├── css/
│   └── styles.css    → todos los estilos, ordenados y comentados
├── img/              → fotos de destinos, hoteles y autos (.webp)
└── video/
    └── travel.mp4    → video de fondo del inicio
```

El archivo `styles.css` tiene un índice al principio con 13 secciones, para que sea fácil encontrar cada cosa (variables, animaciones, botones, hero, filtros, etc.).

---


##  Equipo

Proyecto hecho por:

- _Isaac Garizabalo
- _Camilo Castro
- _Juan Sebastián Torres
- _Nafklin Martínez 

 Materia: Electiva Disciplinar I
Profesor: Morillo Vergel Edgar

---
