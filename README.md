# Flappy Bird con 3 Tuberías en Power Apps

¡Bienvenido/a a este proyecto de **Flappy Bird** creado dentro de **Power Apps**!  
El objetivo es demostrar cómo, con un poco de ingenio, podemos usar la plataforma no solo para crear aplicaciones empresariales, sino también para divertirnos y aprender con un minijuego.

---

## Descripción

Esta versión recrea la mecánica básica de Flappy Bird:
- Un pajarito (**imgPajaro**) que “vuela” mediante saltos.
- **Tres pares** de tuberías (superior e inferior) que se desplazan de derecha a izquierda.
- **Dos timers** para controlar la gravedad/colisiones y el movimiento/puntaje.
- Un sistema de **colisiones** que provoca Game Over al chocar, y un botón de **reinicio** para volver a empezar.

### ¿Para qué sirve?
1. **Aprender Power Apps**: Practicar el manejo de variables, propiedades (X, Y, Width, Height) y la configuración de timers.  
2. **Demostrar versatilidad**: Mostrar que Power Apps no solo es para formularios empresariales, sino que también permite experiencias interactivas.  
3. **Divertirnos**: ¿Quién no quiere un minijuego de desconexión dentro de su app?

---

## Estructura y componentes

1. **Pantalla principal**  
   - Contiene los controles principales:  
     - **imgPajaro** (el pajarito)  
     - **tubo1Inf, tubo1Sup** (tubería inferior y superior #1)  
     - **tubo2Inf, tubo2Sup** (tubería inferior y superior #2)  
     - **tubo3Inf, tubo3Sup** (tubería inferior y superior #3)  
     - **Botón o ícono de reinicio**  
2. **Variables** (OnStart)  
   - Configuran las posiciones, el puntaje, nivel, velocidad, etc.  
3. **Timer de gravedad y colisiones** (ej. `timerGravedad`)  
   - Maneja la caída (sumando a la posición vertical) y detecta choques.  
4. **Timer de movimiento** (ej. `timerMovimiento`)  
   - Desplaza las tuberías de derecha a izquierda y controla el puntaje.  

---

## Cómo usarlo

1. **Importar la app**:  
   - Abre el archivo `.msapp` (u otro) en Power Apps Studio (versión web o de escritorio).

2. **Revisar controles**:  
   - Asegúrate de que cada tubería tiene la propiedad `X, Y, Width, Height` bien ajustada.  
   - El pajarito (`imgPajaro`) también debe tener posición y tamaño adecuados.

3. **Activar timers**:  
   - Comprueba que `timerGravedad` y `timerMovimiento` tengan `Enabled = true`.  
   - Ajusta su `Interval` a tu gusto (por ejemplo, 50 ms, 100 ms).

4. **Probar el juego**:  
   - Toca la pantalla (o un botón configurado) para que el pajarito salte.  
   - Observa cómo se mueven las tuberías y aumenta el puntaje.  
   - Si chocas, presiona el botón de reinicio para volver a empezar.

---

## Personalización

- **Altura del salto**:  
  - Se define en la fórmula `If(numPosVertical > 100, Set(numPosVertical, numPosVertical - 100))`.  
  - Cambia `100` por un valor que se ajuste a tu gusto.

- **Dificultad**:  
  - Modifica `tamGap` (espacio entre tuberías), `numVelocidad` y/o la lógica en `Mod(numPuntaje, 200) = 0` para mayor desafío.  
  - Incrementa o reduce la velocidad de desplazamiento (por ejemplo, en lugar de `-10`, usa `-8` o `-12`).

- **Número de tuberías**:  
  - Si quieres más (o menos) tuberías, repite la lógica agregando más pares y sus controles correspondientes.

- **Estilo gráfico**:  
  - Cambia imágenes, fondos y colores.  
  - Agrega sonidos (por ejemplo, un “beep” al saltar o un “crash” al chocar).

---

## Próximos pasos

- **Tablas de puntuaciones**:  
  - Usa SharePoint o Dataverse para almacenar y mostrar un ranking.
- **Más niveles**:  
  - Aumenta el nivel con cambios de fondo, tuberías con estilos diferentes o añadiendo obstáculos.
- **Compatibilidad móvil**:  
  - Ajusta tus pantallas y disposiciones para que sea cómodo jugar desde el celular o la tablet.

---

**¡Gracias por usar Flappy Bird en Power Apps!**
