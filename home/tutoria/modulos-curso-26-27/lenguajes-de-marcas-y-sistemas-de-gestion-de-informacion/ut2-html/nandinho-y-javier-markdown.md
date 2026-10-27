# Nandinho  y Javier  Markdown&#x20;

## Formularios HTML

***

| Nombre                  | Módulo                        |
| ----------------------- | ----------------------------- |
| Nandinho Antonio Mendes | DAM1 Lenguaje de Marcas 26-27 |
| Javier Figueroa Perdomo | DAM1 Lenguaje de Marcas 26-27 |

***

### 1. ¿Qué es un formulario?

Se conoce como formulario a los mecanismos para enviar información por parte del usuario, a través de unos campos visuales de forma sencilla e intuitiva, que determinan la naturaleza del tipo de información que se va a enviar y cómo hacerla llegar a otro extremo donde se procesará esa información.

HTML proporciona una serie de etiquetas, atributos y conceptos muy útiles para la entrada de información por parte del usuario y enviarla a través de una página. Una de las problemáticas que existen a la hora de que el usuario envíe información es la de eliminar la ambigüedad, o conseguir que la información del usuario cumpla ciertas restricciones y pueda utilizarse o procesarse de la mejor forma posteriormente.

***

### 2. Etiquetas de formularios

#### 01 · ¿Cómo se crea un formulario?

Para comenzar con la creación de un formulario, el primer paso es indicar una etiqueta contenedora `<form>`. También se pueden crear varias etiquetas `<form>` por página para que cada una haga una función.

***

### 3. Atributos de `<form>`

La etiqueta `<form>` dispone de varios atributos que se pueden indicar:

| Atributo         | Descripción                                                                               | Más información   |
| ---------------- | ----------------------------------------------------------------------------------------- | ----------------- |
| `autocomplete`   | Activa (`on`) o desactiva (`off`) el autocompletado para todos los campos del formulario. |                   |
| `novalidate`     | Desactiva la validación HTML5 del formulario.                                             |                   |
| `name`           | Nombre del formulario. Útil para identificar el formulario y procesarlo posteriormente.   |                   |
| `target`         | Nombre del lugar donde se abrirá el formulario. `_blank` para nueva pestaña.              |                   |
| `enctype`        | Codificación para el envío del formulario. Importante para envío de archivos.             | Envío de archivos |
| `accept-charset` | Fuerza a utilizar una codificación en los parámetros de texto del formulario.             |                   |

***

### 4. Ejemplo de formulario

```html
<form name="formulario" method="post" action="/send/">
</form>
```

**Los atributos utilizados en el ejemplo:**

* **`name`**: define el nombre del formulario para diferenciarlo de otros.
* **`method`**: define el método HTTP a utilizar. Usaremos `GET` cuando nos interese enviar datos a través de la URL. En caso contrario, `POST`.
* **`action`**: se usa para indicar la URL a donde se enviarán los datos cuando el usuario pulse el botón de enviar. En caso de omisión, se enviarán a la propia página actual, volviéndola a cargar. En este caso, se estarían enviando a la ruta absoluta `https://dominiopagina.com/send/`.

***

### 5. Información de un formulario

Para que un usuario pueda introducir información en un formulario, requiere que se le indiquen una serie de campos que le permitan introducir la información de la forma más cómoda y rápida posible. Para ello, debemos saber a priori qué tipo de dato le vamos a pedir al usuario (**texto**, **cantidades numéricas**, **fechas**, etc.), y así saber qué tipo de campo de entrada de datos es más conveniente utilizar.

| Información a obtener      | Ejemplos                                     | Etiqueta y atributo a utilizar                   |
| -------------------------- | -------------------------------------------- | ------------------------------------------------ |
| Información de texto corto | Nombres, apellidos, textos cortos…           | `<input>`                                        |
| Información de texto largo | Comentarios, observaciones…                  | `<textarea>`                                     |
| Números o cantidades       | Edades, precios, cuantías…                   | `<input type="number">` ó `<input type="range">` |
| Fechas u horas             | Fecha de nacimiento, inicio de evento…       | `<input type="date">` o derivados                |
| Verdadero/falso            | Sí/No, Opción A/B, ON/OFF…                   | `<input type="checkbox">`                        |
| Opción única               | (Elegir una opción de 2 ó más posibles)      | `<input type="radio">` ó `<select>`              |
| Varias opciones            | (Elegir varias opciones de 2 ó más posibles) | `<select multiple>` ó `<input type="checkbox">`  |
| Opción única abierta       | (Elegir una opción o indicar una propia)     | `<datalist>`                                     |
| Selección de color         | (Escoger un color o tonalidad)               | `<input type="color">`                           |
| Selección de archivo       | (Escoger un archivo para enviar)             | `<input type="file">`                            |

***

### 6. Sintaxis básica de un formulario

La etiqueta `<form>` es sólo la etiqueta contenedora del formulario. Luego, hay que ir añadiendo campos para crear un formulario extenso y personalizado. Una de las etiquetas que más utilizaremos es la etiqueta `<input>`.

```html
<form name="userdata" method="post" action="/send/">
  <input type="text" name="username">
  <input type="submit">
</form>
```

#### Demo

&#x20;

En este ejemplo tenemos un pequeño formulario en el cual:

* Se pide al usuario su nombre con la etiqueta `<input type="text">`.
* Hay un botón para permitir enviar el formulario con la etiqueta `<input type="submit">`.

***

### 7. La etiqueta HTML `<input>`

**Controles: campos de entrada de texto.**

La etiqueta `<input>` es una etiqueta HTML sin etiqueta de cierre. Tiene una gran cantidad de atributos (algunos dependen del valor del atributo `type`).

| Atributo       | Descripción                                                                                           |
| -------------- | ----------------------------------------------------------------------------------------------------- |
| `name`         | Indica el nombre del campo. Útil para hacer referencia a la información almacenada.                   |
| `type`         | Indica la naturaleza de datos que se espera del usuario (texto, número, fechas, etc.).                |
| `value`        | Indica el valor inicial que tendrá este campo de datos. Si se omite, está vacío.                      |
| `form`         | Asocia este campo con un formulario específico. Útil si necesitamos tenerlo fuera del `<form>`.       |
| `list`         | En algunos `<input>` permite combinar con otra etiqueta para personalizarla. Lo veremos más adelante. |
| `placeholder`  | Indica una sugerencia visual.                                                                         |
| `size`         | Tamaño visual (aprox.: número de caracteres) del campo de datos.                                      |
| `autocomplete` | Activa `on` o desactiva `off` el autocompletado para este campo. Activado por defecto.                |
| `autofocus`    | Establece el foco (coloca el cursor) en este campo al cargar la página.                               |

> **No confundir `value` con `placeholder`.** El primero establece un valor para el campo, un contenido. El atributo `placeholder` establece una sugerencia visual, pero al enviar o pulsar sobre el campo para escribir, su valor estará en blanco: no hay contenido.

#### Demo: `value` frente a `placeholder`

```html
<input type="text" name="con_value" value="Texto real (value)">
<input type="text" name="con_placeholder" placeholder="Sugerencia (placeholder)">
```

&#x20;

***

### 8. Textos cortos de `<input>`

En primer lugar, si lo que queremos es guardar información de texto libremente, la opción más habitual es optar por utilizar el campo de entrada de datos `<input type="text">`. Este atributo es el que se utiliza en las etiquetas `<input>` por defecto si no indicamos ningún atributo `type`.

```html
<form method="post" action="/send/">
  Nombre:
  <input name="nombre" autocomplete="off">
</form>
```

> En la diapositiva original el código aparece cortado; aquí se ha completado de forma mínima.

#### Demo

Nombre:&#x20;

***

### 9. Textos cortos específicos

En HTML5 se añaden nuevos tipos para etiquetas `<input>` como `type="search"`, `type="tel"`, `type="url"` o `type="email"`. Aunque la idea es la misma que un campo de texto y en principio no notaremos ningún cambio, estos campos específicos tienen como objetivo hacer más semántico y sencillo el proceso de introducción de datos por parte del usuario.

```html
<form method="post" action="/send/">
  URL: <input type="url" name="web" placeholder="https://pagina.com/">
  Teléfono: <input type="tel" name="telefono" placeholder="+XX XXX XXXXXX">
  Email: <input type="email" name="correo" placeholder="nombre@dominio.com">
</form>
```

#### Demo

URL: \
\
Teléfono: \
\
Email:&#x20;

#### Teclado móvil según el tipo

En dispositivos móviles, el navegador adapta el teclado al tipo de campo:

| `type="url"`                     | `type="tel"`     | `type="email"`            |
| -------------------------------- | ---------------- | ------------------------- |
| Teclado con `/` y `.` accesibles | Teclado numérico | Teclado con `@` accesible |

***

### 10. La etiqueta HTML `<textarea>`

Para indicar un campo para escribir textos extensos, probablemente la etiqueta HTML `<input>` se nos quede corta o sea incómoda. Lo más apropiado sería utilizar la etiqueta HTML `<textarea>`, que nos permite escribir párrafos y líneas de contenido de texto sin restricciones.

Esta etiqueta tiene algunos atributos que podría ser interesante destacar:

| Atributo | Descripción                                                                                                 |
| -------- | ----------------------------------------------------------------------------------------------------------- |
| `cols`   | Número de caracteres que caben en horizontal (columnas).                                                    |
| `rows`   | Número de caracteres que caben en vertical (filas).                                                         |
| `wrap`   | Con `soft` (por defecto) o `hard` puedes indicar si el texto debe enviarse ajustado o tal cual se escribió. |

```html
<form method="post" action="/send/">
  <div>
    Nombre: <input name="nickname">
  </div>
  <textarea name="text" cols="32" rows="8">
Este es el valor de texto por defecto</textarea>
</form>
```

#### Demo

Nombre: Este es el valor de texto por defecto

***

### 11. Librerías para mejorar un `<textarea>`

Existen algunas librerías de **JavaScript** que permiten mejorar, «enriquecer» y ampliar la funcionalidad de estas áreas de texto, permitiendo realizar ciertas tareas visuales como si fueran pequeños editores de texto: fragmentos en negrita, cursiva, imágenes, tablas, etc.

Este tipo de librerías se suelen denominar editores **WYSIWYG** (_lo que ves es lo que obtienes_) y existen muchos y muy variados. Algunos de ellos son los siguientes:

**Ligeros**

| Nombre         | Descripción                                                     |
| -------------- | --------------------------------------------------------------- |
| Quill          | Editor WYSIWYG sencillo, ligero y atractivo.                    |
| Medium Editor  | Al estilo de la web Medium.                                     |
| Woofmark       | Basado en DOM, modular, progresivo y soporta Markdown.          |
| EtherPad       | Editor colaborativo, en tiempo real y escalable.                |
| ProseMirror    | Editor WYSIWYG semántico y modular.                             |
| Trix           | Editor WYSIWYG sencillo y bonito.                               |
| Jodit Editor 3 | Editor WYSIWYG escrito en TypeScript sin librerías adicionales. |
| Slate          | Editor WYSIWYG personalizable.                                  |

**Clásicos (y algo más pesados)**

| Nombre               | Descripción                                               |
| -------------------- | --------------------------------------------------------- |
| Aloha Editor         | Uno de los editores WYSIWYG más conocidos.                |
| Tiny (antes TinyMCE) | Probablemente, el primer editor WYSIWYG en popularizarse. |
| CKEditor5            | Editor WYSIWYG bastante popular.                          |
| AlloyEditor          | Editor moderno WYSIWYG basado en CKEditor.                |
| TrumboWYG            | Incorpora soporte de plugins. Requiere jQuery.            |

***

### 12. La etiqueta HTML `<select>`

Esta etiqueta es una alternativa a radios/checkboxes:

* **Ideal cuando hay demasiadas opciones disponibles.**
* **Optimización de espacio:** evita recargar el aspecto visual del formulario.
* **Definición:** también es conocida como **combo** o **lista desplegable**.

**Tipos de listas de selección**

| Tipo de lista   | Etiqueta     | Uso principal                                  |
| --------------- | ------------ | ---------------------------------------------- |
| **Desplegable** | `<select>`   | Selección entre un número cerrado de opciones. |
| **Abierta**     | `<datalist>` | Sugerencias autocompletables para el usuario.  |

> **Conclusión:** se recomienda usar `<select>` cuando queremos asegurar que el usuario elija exclusivamente una opción dentro de un listado amplio.

***

### 13. Personalizar la etiqueta `<select>`

#### 1. El problema del `<select>` nativo

* **Inconsistencia:** su aspecto depende del sistema operativo y del navegador.
* **Control limitado:** históricamente, las opciones de estilo con CSS eran muy reducidas.

#### 2. Solución moderna: `<selectmenu>` / `appearance`

* **Control total con CSS:** permite cambiar borde, fondo, tipografía y flecha desplegable mediante la propiedad `appearance: none`.
* **Estructura personalizable:** permite modificar tanto la casilla visible como el menú desplegable interno.

***

### 14. La etiqueta HTML `<input>` submit

#### 1. Concepto principal

* **Función:** permite crear botones interactivos en una página web.
* **Contenido flexible:** a diferencia de `<input type="button">` (que solo admite texto plano), la etiqueta `<button>` permite incluir contenido enriquecido en su interior, como texto con formato o imágenes.

#### 2. Funcionalidad con JavaScript

* Se pueden asociar eventos mediante atributos como `onclick` para ejecutar scripts cuando el usuario interactúa con el botón.
* Es la opción preferida para desencadenar acciones dinámicas y de programación en la web.

Hay varios tipos de botones que actúan sobre un formulario en general:

| Tipo de botón de control     | Etiqueta a utilizar                  | Ejemplo (demo) |
| ---------------------------- | ------------------------------------ | -------------- |
| Botón de envío de formulario | `<input type="submit">`              |                |
| Botón de envío con imagen    | `<input type="image">`               |                |
| Botón de resetear formulario | `<input type="reset">`               |                |
| Botón sin funcionalidad      | `<input type="button">` o `<button>` |  Botón         |

***

### 15. La etiqueta HTML `<button>`

#### La etiqueta HTML `<button>`

**1. Definición y ventaja principal**

* **Uso:** sirve para mostrar un botón en la interfaz web.
* **Diferencia clave con `<input>`:** a diferencia de la etiqueta `<input>`, el elemento `<button>` admite contenido en su interior.

**2. Funcionalidad con JavaScript**

* **Interactividad:** se le pueden añadir eventos para realizar acciones dinámicas al pulsar.
* **Comportamiento dinámico:** permite modificar contenido, enviar datos o disparar código mediante la API de eventos de JavaScript.

**3. Personalización de apariencia**

* **Estilo por defecto:** los navegadores aplicaban tradicionalmente un aspecto nativo y tosco.
* **Estilizado moderno:** es un elemento de tipo bloque/en línea al que se le pueden aplicar libremente estilos CSS para modificar su diseño.

***

### 16. Validaciones de formularios

#### ¿Qué son las validaciones?

Las validaciones son comprobaciones que permiten verificar si los datos introducidos en un formulario cumplen determinadas condiciones.

#### ¿Para qué sirven?

* Evitan que falten datos obligatorios.
* Ayudan a detectar formatos incorrectos.
* Limitan los valores que se pueden introducir.
* Mejoran la calidad de la información recibida.

***

## Javier ---> ETIQUETAS ESPECIALIZADAS

### 1. Entrada numérica

La entrada numérica permite que el usuario introduzca números en un formulario. Se crea con la etiqueta `input` y el atributo `type="number"`. Se utiliza, por ejemplo, para pedir una edad, una cantidad de productos o un precio.

Se pueden utilizar diferentes atributos para controlar los valores permitidos:

* **`min`:** establece el valor mínimo.
* **`max`:** establece el valor máximo.
* **`step`:** determina de cuánto en cuánto aumenta o disminuye el valor.

#### Ejemplo de código: campo numérico

```html
<label for="edad">Edad:</label>
<input type="number" id="edad" name="edad" min="0" max="120" step="1">
```

**Vista previa:**

Edad:&#x20;

**Explicación:** el usuario puede introducir una edad entre 0 y 120 años. Las flechas permiten aumentar o disminuir el valor de uno en uno.

### 2. Fechas

El atributo `type="date"` permite seleccionar una fecha mediante un calendario. Esto evita errores al escribirla manualmente y resulta útil para fechas de nacimiento, citas médicas o reservas.

También se pueden utilizar los atributos `min` y `max` para establecer un intervalo de fechas permitido.

**Otros tipos relacionados:**

* `type="time"`: permite seleccionar una hora.
* `type="month"`: permite seleccionar un mes y un año.
* `type="datetime-local"`: permite seleccionar una fecha y una hora.

#### Ejemplo de código: selector de fecha

```html
<label for="fecha">Fecha de reserva:</label>
<input type="date" id="fecha" name="fecha">
```

**Vista previa:**

Fecha de reserva:&#x20;

**Explicación:** al pulsar sobre el campo, el navegador muestra un calendario para elegir la fecha deseada.

### 3. Casillas

Las casillas de verificación, también llamadas _checkboxes_, se crean con `type="checkbox"`. Permiten seleccionar una o varias opciones de forma independiente.

Se utilizan, por ejemplo, para elegir deportes, idiomas o aficiones.

**Atributos principales:**

* **`name`:** identifica el grupo de datos.
* **`value`:** indica el valor que se envía cuando la casilla está marcada.
* **`checked`:** hace que la casilla aparezca marcada por defecto.

#### Ejemplo de código: selección de deportes

```html
<p>Selecciona tus deportes favoritos:</p>

<input type="checkbox" id="futbol" name="deporte" value="futbol">
<label for="futbol">Fútbol</label>

<input type="checkbox" id="tenis" name="deporte" value="tenis">
<label for="tenis">Tenis</label>
```

**Vista previa:**

&#x20;Fútbol  Tenis

**Explicación:** el usuario puede marcar los dos deportes, solamente uno o ninguno.

**Diferencia entre `checkbox` y `radio`:**

* `checkbox`: permite seleccionar varias opciones.
* `radio`: permite seleccionar una única opción dentro del mismo grupo.

### 4. Colores

El atributo `type="color"` permite elegir un color mediante una paleta visual, sin necesidad de escribir su código manualmente.

Se utiliza para seleccionar el color del texto, el fondo de una página web o el de un producto.

El atributo `value` permite establecer el color inicial. Los colores se representan mediante códigos hexadecimales, como `#ff0000`, que corresponde al rojo.

#### Ejemplo de código: selector de colores

```html
<label for="color">Elige un color:</label>
<input type="color" id="color" name="color" value="#ff0000">
```

**Vista previa:**

Elige un color:&#x20;

**Explicación:** el selector aparece inicialmente en rojo, pero el usuario puede abrir la paleta y elegir otro color.

### 5. Organización de campos

Los formularios deben estar bien organizados para que sean fáciles de entender y utilizar. Para ello, HTML ofrece etiquetas que agrupan los campos y explican qué información debe introducirse.

* **`fieldset`:** agrupa campos relacionados dentro de un bloque.
* **`legend`:** añade un título al grupo creado con `fieldset`.
* **`label`:** identifica cada campo y explica qué dato debe introducirse.

La etiqueta `label` se relaciona con el campo mediante el atributo `for`, cuyo valor debe coincidir con el `id` correspondiente.

#### Ejemplo de código: formulario organizado

```html
<fieldset>
    <legend>Datos personales</legend>

    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">

    <br><br>

    <label for="edad">Edad:</label>
    <input type="number" id="edad" name="edad">
</fieldset>
```

**Vista previa:**

Datos personalesNombre: \
\
Edad:&#x20;

**Explicación:** `fieldset` agrupa los campos, `legend` muestra el título y `label` identifica cada entrada. Además, estas etiquetas mejoran la accesibilidad del formulario.

### 6. Ficheros

El atributo `type="file"` permite seleccionar archivos del ordenador o del móvil. Se utiliza para adjuntar fotografías, documentos o trabajos.

**Atributos principales:**

* **`accept`:** limita los tipos de archivos que se pueden seleccionar.
* **`multiple`:** permite seleccionar varios archivos a la vez.

Por ejemplo, `accept="image/*"` permite seleccionar imágenes y `accept=".pdf"` limita la selección a archivos PDF.

#### Ejemplo de código: selección de archivos

```html
<label for="archivo">Selecciona un documento PDF:</label>
<input type="file" id="archivo" name="archivo" accept=".pdf">
```

**Vista previa:**

Selecciona un documento PDF:&#x20;

**Explicación:** el usuario puede seleccionar un archivo PDF desde su dispositivo.

Para enviar archivos correctamente, el formulario debe utilizar `method="POST"` y `enctype="multipart/form-data"`.

#### Ejemplo de código: formulario para subir archivos

```html
<form method="POST" enctype="multipart/form-data">
    <input type="file" name="archivo">
    <button type="submit">Enviar</button>
</form>
```

**Explicación:** `POST` permite enviar los datos y `enctype="multipart/form-data"` permite incluir los archivos en el envío. Para subirlos realmente, también es necesario configurar el procesamiento en el servidor.

***

## VALIDACIONES DE FORMULARIOS

### 1. ¿Qué son las validaciones?

Las validaciones son comprobaciones que permiten verificar que los datos introducidos por el usuario cumplen determinadas condiciones antes de enviar un formulario.

Son importantes por dos motivos:

* **Evitan errores:** ayudan a detectar datos incorrectos o incompletos.
* **Mejoran la experiencia del usuario:** muestran avisos que permiten corregir los errores antes de enviar la información.

Por ejemplo, permiten comprobar que un campo obligatorio no esté vacío, que un correo electrónico tenga un formato adecuado o que una edad esté dentro de un rango permitido.

### 2. Validaciones básicas con HTML5

HTML5 permite realizar validaciones mediante atributos, sin necesidad de programar todas las comprobaciones desde cero.

**Principales atributos de validación:**

| Atributo                  | Función                                                |
| ------------------------- | ------------------------------------------------------ |
| `required`                | Hace que el campo sea obligatorio.                     |
| `type="email"`            | Comprueba el formato general de un correo electrónico. |
| `pattern`                 | Establece un patrón que el texto debe cumplir.         |
| `title`                   | Explica el formato esperado.                           |
| `min` y `max`             | Establecen los valores mínimo y máximo.                |
| `minlength` y `maxlength` | Limitan la longitud del texto.                         |

#### Ejemplo de código: validación de un código postal

```html
<label for="codigo">Código postal:</label>
<input
    type="text"
    id="codigo"
    name="codigo"
    pattern="[0-9]{5}"
    title="Introduce exactamente cinco dígitos"
    required
>
```

**Vista previa:**

Código postal:  Enviar

**Explicación:**

* `pattern="[0-9]{5}"`: exige exactamente cinco dígitos.
* `title`: indica el formato que debe introducirse.
* `required`: obliga a rellenar el campo.

Otros ejemplos de validación serían utilizar `type="email"` para un correo electrónico o `minlength="8"` para exigir una longitud mínima de ocho caracteres en una contraseña.

**Importante:** las validaciones del navegador pueden evitarse, por lo que también es necesario comprobar los datos en el servidor antes de procesarlos.

***

## CONCLUSIÓN

Las etiquetas especializadas permiten crear formularios organizados y adaptados a diferentes tipos de datos. Las validaciones ayudan a detectar errores y mejoran la experiencia del usuario. Para garantizar la fiabilidad de los datos, es importante validar tanto en el navegador como en el servidor.
