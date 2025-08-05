## Ejercicio 4

4. una tienda de ropa tiene la sigueinte promocion: por la compra de tres productos, la prenda de menor valor, tiene un 70% de descuento.
Calcular cual fue el descuento aplicado y cuanto tiene que pagar la persona.

## Pseudocodigo

```
Inicio 
leer cantidad_prendas
Si cantidad_prendas >= 3

    leer prenda1
    leer prenda2
    leer prenda3
        
        Si prenda1 > prenda2 > prenda3
            descuento = prenda3 * 0.70
        Si no prenda1 + prenda2 + prenda3 = precio_total

    Fin si

        Si prenda2 > prenda3 > prenda 1
            descuento = prenda1 * 0.70
        Si no prenda2 + prenda3 + prenda1 = precio_total
    
    Fin si

        Si prenda3 > prenda1 > prenda2
            descuento = prenda2 * 0.70
        Si no prenda3 + prenda1 + prenda2 = precio_total
    Fin si

precio_total = prenda_costo_menor * 0.70
Fin 
```