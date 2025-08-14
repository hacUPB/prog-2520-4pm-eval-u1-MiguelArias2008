## Taller 1 programacion.

# Ejercicios con condicionales:

1. **Verificación de peso de despegue**
    
    En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.

# Tabla: 

| Variables de entrada | Variables de salida| Constatntes| Unidades |
|----------------------|--------------------|------------|----------|
| peso_combustible, peso_carga | peso_total | peso_limite| Toneladas |

## Pseudocodigo:

```
Inicio 
    peso_limte = 640
    Escribir "Ingrese peso de la carga"
    Leer peso_carga
    Escribir "Ingrese peso de combustible"
    Leer peso_combustible
    peso_total = peso_combustible + peso_carga
    Si peso_total > peso_limte Entonces 
        Mostrar "Error: Reducir carga o combustible"
    Si no 
        Mostrar "Listo para despegue"
    Fin si
Fin
```


# **Ejercicios con bucles**

1. **Registro de altitudes de vuelo**
    
    Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.

# Tabla:

|Variables de entrada| Variables de salida | Variable de control | constante |
|--------------------|---------------------|---------------------|-----------|
|registro_altitud| registro_altitud| i | 5 |

## Pseudocodigo:

```
Inicio
    Mientras  0 <= i < 5
    Leer registro_altitud
    Altitud[i] = registro_altitud
    i = i + 1
    Mostrar Altitud[i]
    Fin mientras
Fin
```

# Ejercicios con bucle y condicionales

3. **Simulación de conteo de pasajeros**
    
    Durante el abordaje, un sistema cuenta a los pasajeros que ingresan. Si el número total supera la capacidad máxima, el sistema debe detener el conteo y mostrar un mensaje de alerta.


# Tabla:

|Variables de entrada| Variables de salida | Variable de control | constante |
|--------------------|---------------------|---------------------|-----------|
| - | pasajeros_ingresan | i | 100 |

## Pseudocodigo:

```
Inicio
    i = 0
    Pasajeros_maximos = 100
    Mientras 0 <= i < 99
       
        i = i + 1
        Mostrar Pasajeros[i]
        Si i > 99 
            Mostrar "Error: Capacidad maxima"
        Si no 
            Mostrar "Adelante"
        Fin si
    Fin Mientras
Fin
```
