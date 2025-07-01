# Código de Huffman

## En 1952, David Huffman propuso un método estadístico que permitía asignar un código binario a los diversos símbolos a comprimir

La longitud de cada código no es idéntica para todos los símbolos

- Se asignan códigos cortos a los símbolos utilizados con más frecuencia (los que aparecen más a menudo)
- Los símbolos menos frecuentes reciben códigos binarios más largos
- La expresión Código de Longitud Variable (VLC) se utiliza para indicar este tipo de código porque ningún código es el prefijo de otro, la sucesión final de códigos con longitudes variables será en promedio más pequeña que la obtenida con códigos de longitudes constantes

El codificador Huffman crea una estructura arbórea ordenada con todos los símbolos y la frecuencia con que aparecen, las ramas se construyen en forma recursiva comenzando con los símbolos menos frecuentes

La construcción del árbol se realiza ordenando en primer lugar los símbolos según la frecuencia de aparición. Los dos símbolos con menor frecuencia de aparición se eliminan sucesivamente de la lista y se conectan a un nodo cuyo peso es igual a la suma de la frecuencia de los dos símbolos
El símbolo con menor peso es asignado a la rama 1, el otro a la rama 0 y así sucesivamente, considerando cada nodo formado como un símbolo nuevo, hasta que se obtiene un nodo principal llamado raíz
El código de cada símbolo corresponde a la sucesión de códigos en el camino, comenzando desde este carácter hasta la raíz, cuanto más dentro del árbol esté el símbolo, más largo será el código

### Ejemplos

Consideramos el conjunto A = {a,b,c,d} y realicemos la codificación de la secuencia `aabcdad`

recordemos que tenemos 2*n+1 números para los nodos, entonces 2*4+1 = 9 Nodos

### Pasos

1. Contamos la cantidad de apariciones de cada caracter, `a = 3` `d = 2` `b = 1` `c = 1`
2. Ordenamos de menor a mayor: `b 1`, `c 1`, `d 2`, `a 3`
3. Ahora hay que unir sumamos b con 1 y c con 1, esto da 2, b pasa a quedar con 0 y c con 1. `Si hubiese otro caracter con valor 1 se sumaría con el 2 arriba`

```
Queda algo así, va formando el árbol
     2
(B) 0 1 (C)
```

4. Continuamos uniendo nodos, unimos d 2 al 2 que venía de B C

```
Queda algo así
          
   (D) 2     2
        (B) 0 1 (C)
```

Como se unen queda 4 en el nodo superior y nuevamente le damos valores 0 izquierda y 1 derecha, quedando

```
          4       
   (D) 0     1
        (B) 0 1 (C)
```

5. Nos queda el último valor, a con 3. En este caso el nodo con valor 4 es mayor, por lo que A se ubicará del lado izquierdo


```
 (A) 3       4       
      (D) 0     1
        (  B) 0   1 (C)
```

Ahora toca unir nuevamente los nodos para finalizar y pasar a 0 y 1 los valores izquierda y derecha


```
         7
  (A) 0      1       
      (D) 0     1
        (  B) 0   1 (C)
```

6. ¡LISTO ya codificamos todos los valores! ¿Qué queda? ¡CONOCER LOS VALORES CODIFICADOS!

Tomemos los valores de izquierda superior a derecha, es decir, primero A, luego D, luego B y finalmente C

A 0
D 10
B 110
C 111

7. El código Huffman de `aabcdad` es `010110111`

8. Decodifiquemos basados en esta codificación este código: `101110110111010`

```
10 111 0 110 111 0 10
D   C  A  B   C  A  D

```

9. Fin del ejercicio

---

Creado por Favio Joel Zalazar

Fuentes consultadas 

https://www.youtube.com/watch?v=w2xQkOGyouQ

https://es.ccm.net/aplicaciones-e-internet/museo-de-internet/enciclopedia/12086-como-funciona-el-codigo-huffman/

https://www.kramirez.net/RI/Material/Internet/T3_CODIGO_DE_HUFFMAN.pdf
