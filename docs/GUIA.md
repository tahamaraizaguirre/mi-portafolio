# Guía Tienda TECSUP - Laboratorio 03

En el Laboratorio 03 del curso Diseño de Interfaces de Programación Avanzado trabajé con **Tienda TECSUP**, un proyecto compartido por el docente en GitHub. Mi trabajo consistió en identificar dos errores, corregirlos desde mi propio repositorio y proponer los cambios mediante Pull Requests.

## ¿De qué trata el proyecto?

Tienda TECSUP es una página web sencilla que muestra dos productos, sus precios y cantidades, además del total de la compra. El proyecto utiliza:

- **HTML** para mostrar los productos y el carrito.
- **CSS** para aplicar colores y estilos a la página.
- **JavaScript** para calcular el total de la compra.
- **Git y GitHub** para registrar cambios y trabajar con repositorios remotos.

### Errores que corregí

Encontré dos problemas durante el laboratorio:

1. **Cálculo del carrito:** el programa sumaba los precios sin tomar en cuenta la cantidad. Mostraba **S/ 43.00** en lugar de **S/ 68.00**.
2. **Estilos de la página:** el archivo `index.html` no tenía bien escrita la referencia a `estilos.css`, por lo que no se mostraban los estilos.

## Archivos principales

| Archivo | ¿Para qué sirve? |
| --- | --- |
| `index.html` | Contiene el título, los productos y la sección del total. |
| `estilos.css` | Define los colores y la presentación de la tienda. |
| `script.js` | Calcula el total de los productos del carrito. |
| `README.md` | Explica de manera general el proyecto. |

## Cómo descargar y usar el proyecto

Se necesita tener Git instalado y un navegador web. Para trabajar con el código:

1. Abrir una terminal en la computadora.
2. Clonar mi repositorio con el siguiente comando:

   ```bash
   git clone https://github.com/tahamaraizaguirre/tienda-tecsup.git
   ```

3. Entrar a la carpeta del proyecto con `cd tienda-tecsup`.
4. Abrir el archivo `index.html` en el navegador para ver la tienda.
5. Revisar el total de los productos. Si el repositorio recibe cambios nuevos, se puede actualizar la copia local con `git pull`.

## Correcciones realizadas

### Corrección del total

En `script.js` modifiqué la función `calcularTotal` para multiplicar el precio de cada producto por su cantidad:

```javascript
function calcularTotal(lista) {
    let total = 0;
    for (const producto of lista) {
        total = total + producto.precio * producto.cantidad;
    }
    return total;
}
```

Con este cambio, los dos polos de S/ 25.00 y la taza de S/ 18.00 suman correctamente **S/ 68.00**.

### Corrección de los estilos

En `index.html` corregí el enlace al archivo CSS. La referencia correcta es `href="estilos.css"`, lo que permite que el navegador aplique los colores y la presentación de la tienda.

## Evidencia del trabajo
![Carrito de Tienda TECSUP](../img\lab.png)

También registré los problemas y envié mis correcciones en GitHub:

- [Mi repositorio (fork) de Tienda TECSUP](https://github.com/tahamaraizaguirre/tienda-tecsup)


## Lista de tareas

- [x] Crear el fork del repositorio del docente y clonarlo.
- [x] Reportar los dos errores mediante Issues.
- [x] Corregir el cálculo del carrito y la referencia del CSS.
- [x] Subir los cambios y abrir los dos Pull Requests.
- [x] Revisar los archivos modificados en `Files changed`.
- [x] Publicar esta guía en `docs/GUIA.md` y enlazarla desde el README principal.

## Conclusión

Este laboratorio me ayudó a comprender cómo se trabaja con un repositorio de otra persona sin modificar directamente el original. 
