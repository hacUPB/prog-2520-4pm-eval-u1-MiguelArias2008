## Tarea #1

# Pseudocodigo
```
Inicio
    Entrada (fecha de nacimiento)
    Escribir "Aqui dia de tu nacimiento:"
    Leer dia
    Escribir "Aqui mes de nacimiento:"
    Leer mes
    Escribir "Aqui año de nacimiento:"
    Leer año

    Entrada de datos (fecha actual)
    Escribir "Aqui dia actual:"
    Leer dia_actual
    Escribir "Aqui mes actual:"
    Leer mes_actual
    Escribir "Aqui año actual:"
    Leer año_actual

        Calculo inicial de la edad
        edad = año_actual - año_nacimiento

    Ajuste de edad si no ha cumplido años aún en el año actual
    Si mes_actual < mes_nacimiento Entonces
        edad = edad - 1
    Si no
        Si mes_actual = mes_nacimiento Entonces
            Si dia_actual < dia_nacimiento Entonces
                edad = edad - 1
            Fin Si
        Fin Si
    Fin Si

Salida
Escribir "La edad actual es: "

Fin
```
