## Ejercicio 2

1. Un profesor tiene un salario inicial de $1500, y recibe un incremento de 10% anual durante 6 años ¿Cual es su salario al cabo de 6 años?¿Que salario ha recibido en cada uno de los 6 años?


# Pseudocodigo

```
Inicio
    año = 1
    salario = 1500
    salario_total = 0
    mientras año <= 6
        anual = salario * 1.1
        total = total + anual
        salario = anual
        año = año + 1
        mostrar anual
    fin mientras
    mostrar total
Fin
```
# Diagrama

![ejercicio2](../imagenes/ejercicio%202.png)
