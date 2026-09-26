# Práctica 2: Guardar los números pares
## 1. Descripción del problema (Fase 1)
El programa debe pedirle 5 numeros enteros al usuario y determinar cuales son pares. Los numeros pares se guardan en un arreglo y los impares se descartan.
_____

## 2. Entradas y salidas (Fase 1)
<!-- Define cada entrada y cada salida, con su tipo de dato y su objetivo. -->

**Entradas:**
1. 5 numeros enteros dados por el usuario

**Salidas:**
1. Mostarar cuantos pares encontro
2. Cuales son

## 3. Restricciones e invariante (Fase 1 y 2)

**Restricciones** (¿qué debe cumplirse?):
- El programa debe recibir 5 números enteros y el arreglo debe tener capacidad para 5 elementos.
- Solo se deben guardar los números pares.

**Tamaño del arreglo y por qué** (piensa en el peor caso):
El arreglo debe tener un tamaño de 5, porque en el peor caso los 5 numeros pueden ser pares
**¿El 0 y los negativos son pares? ¿Por qué?**
Si, el 0 es par porque es divisible entre 2. Los numeros negativos tambien pueden ser pares, por ejemplo -4, porque es divisible entre 2.

**Invariante** (¿qué es verdad después de cada vuelta del ciclo?):
El total de pares que lleva, ya qu representa exactamente la cantidad de numeros pares encontrados hasta ese momento y tambien indica la siguiente posicion libre del arreglo.

## 4. Casos resueltos a mano (Fase 1)

| Caso | Números | Pares guardados | Posición de cada par |
|---|---|---|---|
| 1 | 3, 8, 5, 2, 7 | 8,2 | 0=[8], 1=[2] |
| 2 | 2, 4, 7, 9, 10 | 2,4,10 | 0=[2], 1=[4], 2=[10]|
| 3 | 1, 6, 3, 8, 5 | 6,8 | 0=[6] 1=[8] |

## 5. Receta en pseudocódigo (Fase 2)
<!-- Tu receta va en el archivo RECETA.md. Aquí solo responde las dos preguntas. -->

**¿Probé mi receta a mano con un caso?** Sí 
**¿Tuve que corregirla?** No

## 6. Cómo compilar y ejecutar (Fase 3)

```bash
g++ -Wall -Wextra -std=c++17 main.cpp -o numeros_pares
./numeros_pares
```

## 7. Ejemplo de ejecución (Fase 3)
Guardar los numeros pares de 5 numeros
Escribe un numero: 5
Escribe un numero: 8
Escribe un numero: 12
Escribe un numero: 24
Escribe un numero: 4
Numero pares encontrados: 4
8
12
24
4

## 8. Experimentos (Fase 3)

**Experimento A: ¿qué apareció al imprimir las 5 posiciones del arreglo? ¿Por qué?**
En las posiciones que no llené aparecen valores desconocidos o basura de memoria, porque esas posiciones del arreglo nunca recibieron un valor.
Porque el arreglo tiene 5 posiciones, pero solo se guardaron 4 números pares. Las otras posiciones no fueron inicializadas.

**Experimento B: ¿qué pasó al usar la variable del ciclo como posición del arreglo? ¿Por qué?**
Los pares se guardan en posiciones incorrectas, porque contador cuenta todas las vueltas del ciclo, incluyendo los números impares. Por eso el 8 se guarda en la posición 1 y el 12 en la posición 2, dejando espacios vacíos.

## 9. Tabla de pruebas (Fase 4)

| Caso | Números | Esperado | Obtenido | ¿Pasó? |
|---|---|---|---|---|
| Mezcla | 1, 2, 3, 4, 5 | 2 pares: 2, 4 | 2,4 | funciona |
| Posiciones distintas | 3, 8, 5, 2, 7 | 2 pares: 8, 2 | 8,2| funciona |
| Todos pares | 2, 4, 6, 8, 10 | 5 pares | 2,4,6,8,10 | funciona |
| Todos impares | 1, 3, 5, 7, 9 | 0 pares | 0 | funiona |
| Con cero y negativos | 0, -3, -4, 7, 1 | 2 pares: 0, -4 | 0,-4 | funciona |
| Entrada inválida | `hola` o `3.5` | vuelve a pedir | pide numeros nuevos | funciona |
| Caso propio 1 | 6,4,12,34,79 | 6,4,12,34, | 4 pares | funciona |
| Caso propio 2 | 90,67,82,4,1 | 90,82,4 | 3 pares | funciona |

## 10. Bitácora de mejoras (Fase 4)

| # | ¿Qué falló o qué quise mejorar? | ¿Qué cambié? | ¿Funcionó? |
|---|---|---|---|
| 1 | _____ | _____ | _____ |
| 2 | _____ | _____ | _____ |

**Reto elegido (opcional):** _____

## 11. Dudas para el profesor (Fase 3)

| Duda | Lo que ya intenté |
|---|---|
| _____ | _____ |

## 12. Reflexión final

**¿Qué aprendí con esta práctica?**
Utilizar arreglos para guardar datos a identificar numeros pares utilizando el operador MOD y utilizar el contador

**Ahora que terminé, ¿qué cambiaría de mi proceso?**
Pienso que la manera en que lo desarrolle es correcta y me ayudo a tener oren y ressolverlo rapido 
**¿Qué fue lo más difícil y cómo lo resolví?**
Como guardar los numeros en la posiscion correcta. Aun que la receta despues me ayudo mucho
**¿Qué pregunta me quedó sin responder?**
Que otras formas existen para recorrer y guardar datos en un arreglo de forma mas sencilla 
**¿Por qué no puedo usar la variable del ciclo para guardar en el arreglo?**
La variable del ciclo cuenta con todas las vueltas, incluyendo los impares, si la uso para guardar pares pueden quedar espacios vacios entre ellos. Por eso se utiliza totalPares, que cuenta solo los pares que se han guardado
## 13. Lista de verificación antes de entregar (Fase 5)

- [ /] Llené todas las secciones (no quedan `_____`)
- [/] Mi programa compila sin advertencias
- [/] Probé todos los casos de la tabla
- [/] Hice los Experimentos A y B y dejé el código correcto al terminar
- [/] No modifiqué `utilerias.h`
- [/] Hice al menos 3 commits con mensajes claros
- [/] Hice `git push` y verifiqué mi fork en GitHub
- [/] Entregué el enlace de mi fork en Classroom