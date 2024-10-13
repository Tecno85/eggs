# `Flexbox`

**`display: flex`** y **`display: inline-flex`** son propiedades de CSS que permiten crear un diseño flexible y organizar los elementos dentro de un contenedor de manera eficiente. Aquí te explico cada una:

### 1. **`display: flex`**:
   - **Descripción**: Cuando aplicas `display: flex` a un contenedor, sus elementos hijos se organizan en un formato flexible. Puedes controlar la alineación, la dirección y el tamaño de estos elementos dentro del contenedor.
   - **Comportamiento**: El contenedor se convierte en un bloque, ocupando todo el ancho disponible si no se especifica lo contrario.
   - **Uso común**:
     - Crear menús de navegación.
     - Organizar secciones de una página de forma flexible.

   ```css
   .flex-container {
       display: flex;
   }
   ```

### 2. **`display: inline-flex`**:

   - **Descripción**: Es similar a `display: flex`, pero la diferencia clave es que el contenedor conserva las propiedades de un elemento en línea (es decir, no ocupa todo el ancho). Los hijos dentro de este contenedor se organizan de la misma manera que en `display: flex`, pero el contenedor se comporta como un elemento en línea.
   - **Comportamiento**: Se comporta como un elemento en línea, lo que significa que no "rompe" el flujo del texto o de los elementos circundantes.
   - **Uso común**:
     - Agrupar pequeños elementos de forma flexible sin que ocupen todo el ancho disponible, como botones o íconos.

   ```css
   .inline-flex-container {
       display: inline-flex;
   }
   ```

### Diferencia principal:
- **`display: flex`**: El contenedor se comporta como un bloque.
- **`display: inline-flex`**: El contenedor se comporta como un elemento en línea.

### Ejemplo visual:
Si usas `display: flex`, el contenedor sería como una caja grande que ocupa todo el espacio disponible. Mientras que con `display: inline-flex`, sería una caja pequeña que solo ocupa el espacio necesario para los elementos dentro.

### `Ejemplo`

### HTML:
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex vs Inline-Flex</title>
    <style>
        /* Estilos para el contenedor con display: flex */
        .flex-container {
            display: flex;
            background-color: lightblue;
            padding: 10px;
            border: 2px solid blue;
            width: 100%; /* Ocupa todo el ancho */
        }

        /* Estilos para el contenedor con display: inline-flex */
        .inline-flex-container {
            display: inline-flex;
            background-color: lightgreen;
            padding: 10px;
            border: 2px solid green;
        }

        /* Estilos comunes para los elementos hijos */
        .item {
            background-color: #f0f0f0;
            padding: 10px;
            margin: 5px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>

    <h2>Contenedor con display: flex</h2>
    <div class="flex-container">
        <div class="item">Elemento 1</div>
        <div class="item">Elemento 2</div>
        <div class="item">Elemento 3</div>
    </div>

    <h2>Contenedor con display: inline-flex</h2>
    <div class="inline-flex-container">
        <div class="item">Elemento 1</div>
        <div class="item">Elemento 2</div>
        <div class="item">Elemento 3</div>
    </div>

    <p>Texto al lado del inline-flex container.</p>

</body>
</html>
```

### Explicación:
1. **`display: flex`**:
   - El contenedor con `display: flex` ocupa todo el ancho disponible (gracias a `width: 100%`).
   - Los elementos dentro del contenedor (los divs con clase `item`) se distribuyen en línea en el eje horizontal.

2. **`display: inline-flex`**:
   - El contenedor con `display: inline-flex` se comporta como un elemento en línea, es decir, no ocupa todo el ancho, solo el necesario para los elementos hijos.
   - Además, el siguiente texto (`Texto al lado del inline-flex container.`) se muestra en la misma línea que el contenedor porque es un elemento en línea.

### Visualización:
- En el contenedor `flex`, los elementos están en un bloque que ocupa todo el espacio horizontal.
- En el contenedor `inline-flex`, los elementos están en una caja que solo ocupa el espacio que necesitan, dejando el texto "Texto al lado del inline-flex container." a su lado.

Puedes copiar este código en tu editor y probarlo para ver cómo funcionan. ¿Te gustaría que te explique alguna otra propiedad o ajuste del ejemplo?


## `flex-direction`

Es una propiedad de CSS que se utiliza en un contenedor con **`display: flex;`**. Esta propiedad determina la dirección en la que los elementos flexibles dentro de ese contenedor se organizarán.

### Valores principales de `flex-direction`:
1. **`row` (predeterminado):** Los elementos se colocan en una fila, de izquierda a derecha (o de derecha a izquierda si el idioma es RTL, como el árabe).
   
   ```css
   .container {
     display: flex;
     flex-direction: row; /* o simplemente se omite porque es el valor por defecto */
   }
   ```

2. **`row-reverse`:** Similar a `row`, pero los elementos se colocan de derecha a izquierda.
   
   ```css
   .container {
     display: flex;
     flex-direction: row-reverse;
   }
   ```

3. **`column`:** Los elementos se organizan en una columna, de arriba hacia abajo.
   
   ```css
   .container {
     display: flex;
     flex-direction: column;
   }
   ```

4. **`column-reverse`:** Similar a `column`, pero los elementos se colocan de abajo hacia arriba.
   
   ```css
   .container {
     display: flex;
     flex-direction: column-reverse;
   }
   ```

### Ejemplo práctico:
```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: column; /* Cambia la dirección aquí */
    border: 1px solid #000;
  }

  .item {
    padding: 10px;
    border: 1px solid #ccc;
  }
</style>
```

En este ejemplo, los elementos hijos (`.item`) se apilarán en una columna porque se ha usado `flex-direction: column;`. Si cambias el valor a `row`, se organizarán en fila.

### Resumen:
- **`row`**: fila horizontal (izquierda a derecha).
- **`row-reverse`**: fila horizontal (derecha a izquierda).
- **`column`**: columna vertical (de arriba hacia abajo).
- **`column-reverse`**: columna vertical (de abajo hacia arriba).

¿Te gustaría algún ejemplo más detallado o tienes alguna duda adicional?