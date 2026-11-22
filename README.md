# Simulador de bioplásticos

Experimenta con recetas virtuales de bioplásticos y compáralas con tus muestras reales.

**[Abrir el simulador](https://TU-USUARIO.github.io/bioplasticos/)** · **[Versión en realidad aumentada](https://TU-USUARIO.github.io/bioplasticos/ar/)**

## Qué es

Una herramienta web para explorar cómo cambia un bioplástico casero según su receta antes de llevarlo a la cocina o al taller. Ajustas los ingredientes y ves al instante cómo se verá el material en 3D, qué tan flexible y transparente será, cuánto se encogerá al secar y para qué tipo de producto puede servir.

Está pensada para personas interesadas en biomateriales: diseñadores, makers, docentes, estudiantes y cualquiera que quiera experimentar con materiales hechos a partir de recursos naturales.

Funciona en el navegador, en computadora y celular, sin instalar nada.

## Funciones

**Receta**
- Cuatro bases: gelatina, agar, almidón de maíz y alginato de sodio.
- Control de polímero, agua, glicerina, vinagre, relleno, pigmento y tamaño del molde.
- Rellenos (café, cáscara de huevo, cáscara de naranja, aserrín) y pigmentos naturales (espirulina, cúrcuma, jamaica, betabel, carbón vegetal).
- Ingredientes propios: crea rellenos y pigmentos con sus propiedades (rigidez, opacidad, absorción de agua, tamaño de partícula, sensibilidad al calor y a la luz) y compártelos con un código.

**Visualización 3D**
- Formas: lámina, maceta, pantalla de lámpara, botón, cartera y cono de grosores.
- Carga tu propio modelo en STL, OBJ o GLB y velo hecho con tu receta.
- Usa una foto de tu muestra real como textura.
- Simulación del secado, prueba de flexión (la pieza se dobla o se rompe), luz de fondo para ver la transparencia y regla para medir el encogimiento.
- Comparador de dos muestras lado a lado.

**Análisis**
- Indicadores de flexibilidad, transparencia, encogimiento, grosor, tiempo de secado y riesgo de hongos.
- Composición de la mezcla al verter y de la lámina seca.
- Vista microscópica animada de las cadenas del polímero, la glicerina y el agua.
- Aplicaciones sugeridas según la receta, con indicaciones para ajustarla.
- Procedimiento paso a paso con las cantidades exactas.
- Ficha técnica descargable en PNG.

## Cómo funciona el modelo

El simulador usa un modelo didáctico basado en proporciones de recetarios abiertos de bioplásticos:

- La **flexibilidad** depende de la proporción de glicerina respecto al polímero, de la concentración de la mezcla y de la cantidad y tipo de relleno.
- El **encogimiento** se calcula a partir de la pérdida de agua de cada base y del efecto estabilizador de los rellenos, en especial las fibras.
- El **color** de los pigmentos sigue una versión simplificada de la ley de Beer-Lambert: depende de la concentración en la lámina seca y del grosor.
- El **riesgo de hongos** considera la base, el exceso de glicerina, los rellenos orgánicos, la absorción de agua y el tiempo de secado.

> **Importante:** los valores son aproximados y sirven para explorar tendencias. Los resultados reales cambian con la humedad, la temperatura, el grosor y la marca de los insumos. Usa el simulador para planear y compara siempre con tus muestras reales.

## Uso rápido

1. Elige una base en la pestaña **Receta** y ajusta las cantidades.
2. Observa la pieza en el visor: gírala, sécala, dóblala o enciende la luz de fondo.
3. Revisa la pestaña **Usos** para ver en qué productos funciona tu material.
4. Sigue la pestaña **Pasos** para fabricarlo.
5. Guarda la muestra o descarga su ficha técnica.

## Realidad aumentada

La carpeta `ar/` contiene una versión hecha con A-Frame para ver la pieza a tamaño real:

- **Android con Chrome:** toca AR, apunta a una mesa y toca la pantalla para colocar la pieza.
- **Visores Meta Quest:** abre el enlace en el navegador del visor y toca VR.
- En iPhone se ve en 3D, aunque sin AR, porque Safari no es compatible con WebXR.

## Privacidad y datos

Todo se ejecuta en tu navegador. Las muestras y los ingredientes que crees se guardan solo en tu dispositivo y siguen ahí al recargar la página. Se pierden si borras los datos de navegación o si usas modo incógnito. Los modelos 3D y las fotos que cargues no se envían a ningún servidor.

## Tecnología

- HTML, CSS y JavaScript en un solo archivo, sin proceso de compilación.
- [three.js](https://threejs.org/) r128 para el render 3D, con oclusión ambiental (SSAO), sombras de contacto y antialiasing FXAA.
- [A-Frame](https://aframe.io/) 1.5 para la versión de realidad aumentada y virtual.
- Tipografía [Inter Tight](https://fonts.google.com/specimen/Inter+Tight).

Las librerías se cargan desde internet, por lo que el visor 3D necesita conexión.

## Estructura

```
bioplasticos/
├── index.html      Simulador principal
├── ar/
│   └── index.html  Versión de realidad aumentada y virtual
└── docs/
    └── captura.png Imagen para este README
```

## Publicar tu propia copia

1. Haz un fork de este repositorio o descarga los archivos.
2. En tu repositorio ve a **Settings → Pages**.
3. En **Branch** elige `main` y la carpeta `/ (root)`, y guarda.
4. En uno o dos minutos tu copia estará en `https://tu-usuario.github.io/bioplasticos/`.

## Seguridad

Al preparar bioplásticos usa guantes térmicos para calentar, trabaja con supervisión si hay menores y no consumas las mezclas, aunque sus ingredientes sean comestibles.

## Créditos

Creado por **Valens**.

## Licencia

[MIT](LICENSE). Puedes usar, modificar y compartir este proyecto citando la fuente.

---

Valens · v1.22
