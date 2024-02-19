# Define las siguientes características de Typescript:



1. **Static type-checking:**
- *Definición:* Es un proceso en el que TypeScript verifica y analiza los tipos de variables y expresiones durante la fase de compilación, antes de que se ejecute el código. Ayuda a detectar posibles errores y mejorar la robustez del código.

```ts
// Ejemplo de verificación estática de tipos
let nombre: string = "Juan";
// La siguiente línea causaría un error en tiempo de compilación
// porque no se puede asignar un número a una cadena.
// nombre = 123;
```

2. **Non-exception Failures:**
- *Significado:* Se refiere a situaciones en las que el código no arroja excepciones durante la ejecución, pero aún así puede contener errores. TypeScript busca identificar y prevenir este tipo de fallos, como errores de lógica, antes de la ejecución del programa.

```ts
// Ejemplo de fallo sin excepción
function dividir(a: number, b: number): number {
    // Este código no genera una excepción,
    // pero puede llevar a resultados inesperados.
    return a / b;
}
```

3. **Types for Tooling:**
- *Concepto:* Se refiere al uso de información de tipos por parte de TypeScript para proporcionar herramientas de desarrollo más eficientes, como autocompletado de código, mensajes de error precisos y sugerencias durante la edición del código.

```ts
// Ejemplo de tipos para herramientas
interface Persona {
    nombre: string;
    edad: number;
}

const usuario: Persona = {
    nombre: "Alicia",
    edad: 30,
};

// Con la información de tipos, el editor puede proporcionar
// autocompletado y sugerencias con conocimiento de tipos.
usuario.
```

4. **tsc, the TypeScript compiler:**
- *Explicación:* Es el compilador de TypeScript que transforma el código TypeScript en código JavaScript. Puede ser ejecutado a través de la línea de comandos utilizando el comando `tsc`.

```bash
#Comando para ejecutar el compilador TypeScript (tsc)
tsc ejemplo.ts
```

5. **Emitting with Errors:**
- *Descripción:* Involucra la generación de archivos de salida (por ejemplo, JavaScript) incluso cuando existen errores en el código TypeScript. Esto permite que el código aún se ejecute, aunque se adviertan posibles problemas.

```ts
// Ejemplo de generación con errores
function saludar(nombre: string) {
    // Esta línea contiene un error (falta punto y coma),
    // pero TypeScript generará el código JavaScript de todos modos.
    console.log("¡Hola, " + nombre)
}
```

6. **Explicit Types:**
- *Definición:* Se refiere al acto de proporcionar anotaciones de tipos de manera explícita en el código TypeScript, indicando el tipo de variables, parámetros de funciones, etc., con el objetivo de mejorar la claridad y prevenir errores.

```ts
// Ejemplo de tipos explícitos
function sumarNumeros(a: number, b: number): number {
    // Especificando explícitamente los tipos de parámetros y el valor de retorno
    return a + b;
}
```

7. **Erased Types:**
- *Significado:* Alude al hecho de que las anotaciones de tipos en TypeScript no afectan el comportamiento en tiempo de ejecución, ya que son eliminadas durante la compilación. Esto significa que TypeScript no introduce cambios en el comportamiento del programa.

```ts
// Ejemplo de tipos eliminados
interface Producto {
    nombre: string;
    precio: number;
}

const laptop: Producto = {
    nombre: "Laptop",
    precio: 1200,
};

// Durante la compilación, la información de tipos se elimina.
// El código JavaScript generado no contiene anotaciones de tipo.
```

8. **Downleveling:**
- *Explicación:* Es el proceso de convertir código TypeScript escrito en una versión más reciente de ECMAScript a una versión más antigua. Por defecto, TypeScript apunta a ECMAScript 3, pero se puede especificar un objetivo diferente usando la opción `--target`.

```ts
// Ejemplo de reducción de nivel
// Código TypeScript dirigido a ECMAScript 2015 (ES6)
const arrowFunction = () => console.log("¡Hola, función de flecha!");

// Comando para compilar con reducción de nivel a ECMAScript 3
// tsc --target es3 nombredelarchivo.ts
```

9. **Strictness:**
- *Concepto:* Refiere al nivel de rigurosidad en la verificación de tipos en TypeScript. Permite activar o desactivar diversas configuraciones de estrictitud para adaptarse a las preferencias del desarrollador.

```ts
// Ejemplo de estrictitud con noImplicitAny
// Activar la bandera noImplicitAny evita el uso implícito del tipo 'any'.
function multiplicar(a: number, b) {
    // Error: El parámetro 'b' tiene implícitamente un tipo 'any'.
    return a * b;
}
```

10. **noImplicitAny:**
- *Explicación:* Es una configuración de TypeScript que, cuando está activada, genera un error si el compilador no puede inferir el tipo de una variable, evitando así el uso implícito de `any`.

```ts
// Ejemplo de noImplicitAny
// Al activar noImplicitAny, se genera un error si el compilador no puede inferir el tipo.
function multiplicar(a: number, b) {
    // Error: El parámetro 'b' tiene implícitamente un tipo 'any'.
    return a * b;
}

// Añadiendo la anotación de tipo para evitar el error
function multiplicarConTipos(a: number, b: number): number {
    return a * b;
}

// La configuración noImplicitAny ayuda a hacer explícito el tipo de las variables
// y prevenir el uso inadvertido de 'any'.
```

11. **strictNullChecks:**
- *Significado:* Es una configuración que, al estar habilitada, hace que TypeScript sea más estricto en cuanto al manejo de `null` y `undefined`, ayudando a prevenir errores relacionados con valores nulos.

```ts
// Ejemplo de strictNullChecks
// Al activar la bandera strictNullChecks, se requiere el manejo explícito de null y undefined.
let nombrede

usuario: string | null = "Juan";
// Error: El objeto posiblemente es 'null'.
console.log(nomUsuario.length);
```

