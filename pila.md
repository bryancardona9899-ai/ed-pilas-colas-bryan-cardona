# 1. Operacion push (dato)
Inserta un nuevo dato en la pila 

ALGORITMO push(dato)
    Si pilaEstaLllena () ENTONCES
        Escribir "Error: La pila se encuentra llena(Stack Overflow)"
        RETORNAR FALSO
    FIN SI

    cima ← cima + 1
    arreglo[cima] ← dato
    RETORNAR VERDADERO
FIN ALGORITMO

ALGORITMO pop()
    SI estaVacia() ENTONCES
        ESCRIBIR "Error: La Pila se encuentra vacia, no hay datos para eliminar (Stack Underflow)"
        RETORNAR NULL
    FIN SI

    elemento ← arreglo[cima]
    cima ← cima - 1
    RETORNAR elemento
FIN ALGORITMO

ALGORITMO peek()
    SI estaVacia() ENTONCES
        ESCRIBIR "La Pila esta vacia"
        RETORNAR NULL
    FIN SI

    RETORNAR arreglo[cima] 
FIN ALGORITMO

ALGORITMO estaVacia()
    SI cima == -1 ENTONCES
        RETORNAR VERDADERO
    SINO
        RETORNAR FALSO
    FIN SI
FIN ALGORITMO