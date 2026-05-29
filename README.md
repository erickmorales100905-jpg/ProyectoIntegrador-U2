# ProyectoIntegrador-U2


Título: Optimización del Pipeline de Animación 2D: Integración de IA Generativa de Poses y Animación Cuadro a Cuadro en Blender
FASE 1: CONCEPTUALIZACIÓN Y GENERACIÓN DE ACTIVOS CON INTELIGENCIA ARTIFICIAL
Esta fase inicial se centró en utilizar la Inteligencia Artificial como una herramienta de co-creación y conceptualización rápida para romper la "hoja en blanco" y establecer las bases anatómicas y de estilo del personaje.

Paso 1: Definición del Modelo y Prompting Inicial
Descripción: El proceso comenzó con la conceptualización del personaje: un perro de raza tipo pitbull/terrier, con un patrón de manchas marrón y blanco bien definido. El objetivo era crear un diseño lo suficientemente estilizado para ser animado, pero con la complejidad anatómica de un cuadrúpedo.

Prompting utilizado
<img width="699" height="249" alt="image" src="https://github.com/user-attachments/assets/d7110317-cbd1-445e-9988-4fdcee02911e" />

Ejecución: Se alimentó a la IA con parámetros específicos solicitando un layout o secuencia de movimiento dividida en cuadros independientes y debidamente numerados (del 1 al 8). La intención original era obtener un desglose de caminata (walk cycle) tradicional de perfil para analizar los puntos de contacto de las patas con el suelo.

Paso 2: Control de Calidad, Iteración y Corrección de Coherencia Motriz
Descripción: Al analizar la primera entrega de la IA, se realizó una auditoría visual crítica (rol del director de animación). Se detectó un error común en la generación de movimiento: los cuadros 2 y 3 eran prácticamente idénticos, lo que habría provocado un "congelamiento" o un bucle estático en la animación final, rompiendo la fluidez.

<img width="1600" height="588" alt="image" src="https://github.com/user-attachments/assets/a77a0319-51e9-4a6a-8034-0ec4f9e2c01b" />

Solución e Intervención: Se enviaron instrucciones de corrección a la IA sin alterar el diseño base ni el fondo del entorno (para evitar el flicker o rediseño total). Se solicitó cambiar drásticamente la dinámica del movimiento, transformando la caminata lineal en una acción progresiva de aceleración:

Cuadro 2: Transición de apoyo a impulso.

Cuadro 3: Fase de suspensión en el aire (brinco), donde ninguna pata toca el suelo.

Esto dotó a la secuencia de una narrativa visual: el perro no solo camina, sino que reacciona, corre y salta.


FASE 2: PREPARACIÓN DEL ENTORNO DE TRABAJO EN BLENDER
Una vez obtenidos los cuatro cuadros definitivos de la IA, el proyecto se trasladó al entorno de producción digital en Blender para aprovechar sus herramientas de dibujo vectorial y línea de tiempo.

Paso 3: Configuración del Espacio de Trabajo (Grease Pencil)
Descripción: Se abrió un proyecto nuevo en Blender utilizando la plantilla 2D Animation. Esta interfaz optimiza el programa para trabajar en dos dimensiones, configurando la cámara de manera ortogonal y activando el motor de renderizado Eevee.

Importación de Referencias: Las imágenes numeradas generadas por la IA se importaron al espacio 3D utilizando la función Images as Planes (o como vacíos de referencia de imagen). Se alinearon secuencialmente detrás del lienzo de dibujo para utilizarlas como plantillas físicas de fondo, ajustando la opacidad al 50% (efecto papel cebolla digital).

FASE 3: PRODUCCIÓN, ROTOSCOPIA Y ANIMACIÓN 2D
Aquí es donde el criterio del animador toma el control total del proyecto, utilizando la técnica de rotoscopia para dar vida a los bocetos estáticos de la IA.

Paso 4: Trazado y Calcado Digital de Keyframes (Cuadros Clave)
Descripción: Utilizando el objeto Grease Pencil y una tableta digitalizadora, se crearon los cuatro fotogramas clave principales (keyframes) en la línea de tiempo de Blender, colocándolos en los frames correspondientes (por ejemplo: Frame 1, 10, 20 y 30) para planificar el timing inicial.

<img width="780" height="446" alt="image" src="https://github.com/user-attachments/assets/64f94baf-2a4f-492a-938c-eb13bf06cf0b" />


Técnica de Dibujo: Se calcó minuciosamente la silueta del perro en cada uno de los 4 estados provistos por la IA. Este proceso de rotoscopia garantizó la consistencia absoluta del volumen del perro (manteniendo el tamaño de la cabeza, el largo de la cola y las manchas idénticas), superando uno de los mayores problemas de la animación tradicional: la pérdida de proporciones.

Paso 5: Desarrollo de Intermedios (In-betweens) y Arcos de Movimiento
Descripción: Con las 4 poses base calcadas de la IA, la secuencia se sentía "entrecortada". El trabajo crucial consistió en dibujar los cuadros intermedios (in-betweens) para conectar orgánicamente las poses.
<img width="787" height="443" alt="image" src="https://github.com/user-attachments/assets/7c434593-d327-44a8-b227-8a3e3323d66a" />

Dinámica del Movimiento: * Entre el cuadro 1 y 2, se dibujó la aceleración del paso.
<img width="777" height="441" alt="image" src="https://github.com/user-attachments/assets/15b597cd-d919-44d5-919a-4e793ea9b1df" />

Entre el cuadro 2 y 3, se animó el despegue de las patas traseras del suelo y la flexión del cuerpo para el salto.
<img width="783" height="443" alt="image" src="https://github.com/user-attachments/assets/3f07c56a-e436-4308-9486-3a7566d92f52" />

Entre el cuadro 3 y 4, se diseñó la parábola de caída y el impacto de las patas delanteras contra el piso, aplicando los principios clásicos de animación como el Squash and Stretch (estiramiento y aplastamiento) y el seguimiento de arcos en la cola y orejas.
<img width="776" height="442" alt="image" src="https://github.com/user-attachments/assets/f05894e1-6def-4ce2-bbf4-382c4e173892" />

FASE 4: EVALUACIÓN FINAL Y CONCLUSIONES DEL PROYECTO
Paso 6: Renderizado, Revisión Cinematográfica y Conclusión
Renderizado: Se configuró la tasa de refresco a 24 fps (estándar cinematográfico) y se exportó la animación en una secuencia de imágenes PNG con canal alfa y un video final en formato MP4 (H.264).

Conclusión de la Actividad: El proyecto demuestra con éxito la viabilidad de un pipeline híbrido. La Inteligencia Artificial actuó como un generador ultra-rápido de storyboard y anatomía de referencia, ahorrando horas de diseño de personajes. Por su parte, Blender proporcionó la precisión técnica y el control artístico necesarios para inyectar peso, ritmo y fluidez al movimiento, demostrando que la IA es una aliada del artista y no su reemplazo.
