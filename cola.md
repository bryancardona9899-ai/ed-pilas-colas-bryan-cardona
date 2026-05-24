ALGORITMO enqueue(dato)
    SI colaEstaLlena() ENTONCES
        ESCRIBIR "Error: La cola se encuentra llena (QUEUE Overflow)"
        RETORNAR FALSO
    FIN SI

    SI estaVacia( ENTONCES)
        cabeza ← 0
    FIN SI

    final ← final + 1
    arreglo[final] ← dato
    RETORNAR VERDADERO
FIN ALGORITMO

ALGORITMO dequeue()
    SI estaVacia() ENTONCES
        ESCRIBIR "Error: No hay datos en la cola (Queue Underflow)"
        RETORNAR NULL
    FIN SI

    elemento ← arreglo[cabeza]

    SI cabeza == final ENTONCES
        cabeza ← -1
        final ← -1
    SINO
        cabeza ← cabeza + 1 
    FIN SI

    RETORNAR elemento
FIN ALGORITMO


ALGORITMO peek()
    SI estaVacia() ENTONCES
        ESCRIBIR "La cola esta vacia"
        RETORNAR NULL
    FIN SI

    RETORNAR arreglo[Cabeza]
FIN ALGORITMO


ALGORITMO estaVacia() 
    SI cabeza == -1 ENTONCES
        RETORNAR VERDADERO
    SINO
        RETORNAR FALSO
    FIN SI
FIN ALGORITMO