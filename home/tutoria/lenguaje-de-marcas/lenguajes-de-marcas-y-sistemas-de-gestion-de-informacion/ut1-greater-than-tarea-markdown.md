# UT1 -> Tarea Markdown

| Nombre                  | Módulo                        |
| ----------------------- | ----------------------------- |
| Nandinho Antonio Mendes | DAM1 Lenguaje de Marcas 26-27 |

## ¿Que es?

Markdown fue desarrollado en 2004 por John Gruber, y se refiere tanto a (1) una manera de formar archivos de texto, como a (2) una utilidad del lenguaje de programación Perl para convertir archivos Markdown en HTML. En esta lección nos centraremos en la primera acepción y aprenderemos a escribir archivos utilizando la sintaxis de Markdown.

## Sintaxis en Markdown

Los archivos en Markdown se guardan con la extensión `.md` y se pueden abrir en un editor de texto como TextEdit, Notepad, Sublime Text o Vim. Muchos sitios web o plataformas de publicación también ofrecen editores basados en la web y/o extensiones para introducir texto utilizando la sintaxis de Markdown.

## Encabezado en Markdown

Markdown dispone de cuatro niveles de encabezados definidos por el número de `#` antes del texto del encabezado. Pega los siguientes ejemplos en la caja de texto de la izquierda:

## Primer nivel de encabezado

### Segundo nivel de encabezado

#### Tercer nivel de encabezado

**Cuarto nivel de encabezado**

## Tipos de textos

Los tipos de textos son:

_En cursiva_.

**En negrita**.

_**ambas**_

## Ordenadas, desordenadas y anidadas

### Listas desordenadas

* Primer elemento
* Segundo elemento
* Tercer elemento

### Listas ordenadas

1. Primer paso
2. Segundo paso
3. Tercer paso

_Los números no tienen que ser correlativos_

1. Primer paso
2. Segundo paso
3. Tercer paso

### Listas anidadas

* Fruta
  * Manzana
  * Pera
* Verdura
  * Espinaca
  * Brócoli

## Citas en Markdown

### Sintaxis básica

> Un país, una civilización se puede juzgar por la forma en que trata a sus animales. — Mahatma Gandhi

#### Citas de varios párrafos

> Creo que los animales ven en el hombre un ser igual a ellos que ha perdido de forma peligrosa el sano intelecto animal.
>
> Es decir, que ven en él al animal irracional, al animal que ríe, al animal que llora. — Friedrich Nietzsche

#### Citas anidadas

> Esto es una cita normal.
>
> > Y esto es una cita dentro de la cita.
>
> Volvemos al primer nivel.

## Bloques con vallas en Markdown

```
function saludar(nombre) {
  return `Hola, ${nombre}`;
}
```

### Bloques con sangría

```
Esto es un bloque de código
creado con sangría
```

### Anidar bloques dentro de listas

{% stepper %}
{% step %}
### Instala las dependencias

```bash
npm install
```
{% endstep %}

{% step %}
### Arranca el servidor

```bash
npm run dev
```
{% endstep %}
{% endstepper %}

### Código en línea

Ejecuta `npm install` antes de continuar.

## Salto de línea en Markdown

Primer párrafo.

Segundo párrafo.

## Casillas de verificación en Markdown: listas de tareas

### Sintaxis

* [x] Escribir el borrador
* [x] Revisar la ortografía
* [x] Publicar
* [ ] Compartir en redes

### Anidar tareas

* [ ] Preparar el lanzamiento
  * [x] Escribir la nota de prensa
  * [x] Preparar las capturas
  * [ ] Grabar el vídeo de demostración
* [ ] Publicar

### Formato dentro de la tarea

* [ ] Revisar el archivo `config.yml`
* [ ] Leer la [documentación de la API](https://ejemplo.com/)
* [x] ~~Arreglar el error de login~~ resuelto en #142
* [ ] **Urgente:** desplegar antes del viernes

## Enlaces en Markdown

Aprende mas en [naxof44.com](https://www.hola.com/).

### Con título emergente

[naxof44.com](/broken/pages/2b7c8bdd7ad2edc178459c6c1db835e76fbb8eba)

### URLs con espacios o paréntesis

[Un documento](https://ejemplo.com/mi%20archivo.pdf)

### Enlaces de referencia

Me llamo Airam y escribo sobre [videojuegos](https://www.hola.com/).

Ese [proyecto](https://www.hola.com/) nació porque me encanta los videojuegos.

### Etiqueta implícita

Consulta la [documentación](https://www.hola.com/) para más detalles.

### Enlaces automáticos

[https://airam.es](https://airam.es/)\
[hola@gmail.com](mailto:hola@gmail.com)

### Anclas

Salta a la sección de [tablas](ut1-greater-than-tarea-markdown.md#tablas).

### Enlaces relativos

[La guía de sintaxis](/broken/pages/635ae214e0f7ed9d8ef6acf9e82401e734e1c5fc)

[Un archivo vecino](/broken/pages/c55aea58046bca4ca6f8f4967d1f87fde947be1e)

[Subir un nivel](/broken/pages/aab7294884e47ec3b18c220f8e764c4916fe6342)

### Imágenes enlazadas



## Tachado en Markdown

El plazo era ~~el viernes~~ el lunes.

_Al poner dos \~\~Texto \~\~ obtienes el efecto tachado_

### Combinar con otros formatos

~~**Tachado y en negrita**~~

~~_Tachado y en cursiva_~~

~~Un~~ [~~enlace tachado~~](https://airam.es/)

### Un apunte de accesibilidad

El plazo era ~~el viernes~~, **cambiado al lunes**.

## Tablas en Markdown

### Sintaxis básica

| Lenguaje | Año  | Creador         |
| -------- | ---- | --------------- |
| Markdown | 2004 | John Gruber     |
| HTML     | 1993 | Tim Berners-Lee |
| LaTeX    | 1984 | Leslie Lamport  |

### Alineación de columnas

| Producto    | Cantidad |   Precio |
| ----------- | :------: | -------: |
| Teclado     |     2    |  89,00 € |
| Monitor     |     1    | 249,90 € |
| Cable USB-C |    12    |   7,50 € |

#### _Las columnas no necesitan estar alineadas_

| Lenguaje | Año  | Creador         |
| -------- | ---- | --------------- |
| Markdown | 2004 | John Gruber     |
| HTML     | 1993 | Tim Berners-Lee |

_produce el mismo resultado que:_

| Lenguaje | Año  | Creador         |
| -------- | ---- | --------------- |
| Markdown | 2004 | John Gruber     |
| HTML     | 1993 | Tim Berners-Lee |

### Formato dentro de las celdas

| Elemento | Ejemplo                          |
| -------- | -------------------------------- |
| Negrita  | **importante**                   |
| Cursiva  | _matiz_                          |
| Código   | `npm install`                    |
| Enlace   | [Markdown.es](https://hola.com/) |
| Tachado  | ~~obsoleto~~                     |

### Limitaciones y cómo sortearlas

La barra vertical dentro de una celda:

| Operador | Significado |
| -------- | ----------- |
| `\|\|`   | O lógico    |
| `&&`     | Y lógico    |

### Saltos de línea dentro de una celda

| Campo     | Valor                                          |
| --------- | ---------------------------------------------- |
| Dirección | <p>Calle Mayor 1<br>28013 Madrid<br>España</p> |

## Código en línea en Markdown

### Sintaxis

Ejecuta `npm install` antes de arrancar el proyecto.

#### Lo que va dentro no se interpreta

El texto `**esto no se pone en negrita**` conserva los asteriscos.

### Acentos graves dentro del código

Usa `` la plantilla `${nombre}` `` para interpolar.

#### _Un uso muy común: teclas_

Pulsa `Ctrl` + `C` para copiar.

## Escapar caracteres en Markdown

### Sintaxis

\*Esto no está en cursiva\*

2 \* 3 \* 4 = 24

Un guion bajo\_dentro\_de una palabra

## Imágenes en Markdown

### Sintaxis básica

![Texto alternativo](../../.gitbook/assets/300)

### Título emergente

![Montañas](../../.gitbook/assets/300.jpg)

### Imágenes de referencia

Aquí va el logo:&#x20;

Y aquí otra vez:&#x20;

### Imágenes clicables



### Rutas: relativas o absolutas

![Absoluta a otro dominio](https://ejemplo.com/imagen.jpg)

## Líneas horizontales en Markdown

### Las tres formas

_Las tres producen exactamente el mismo resultado:_

***

***

***

> Resumen\
> Markdown es un lenguaje de marcado ligero creado por _**John Gruber y Aaron Swartz**_ que trata de conseguir la máxima legibilidad y facilidad de publicación tanto en su forma de entrada como de salida, inspirándose en muchas convenciones existentes para marcar mensajes de correo electrónico usando texto llano.
