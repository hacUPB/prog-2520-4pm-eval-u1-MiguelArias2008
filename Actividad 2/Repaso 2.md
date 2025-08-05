2. Un almacén de ropa tiene una promoción: por compras superiores a $250 000 se les aplicará un descuento de 15%, de caso contrario, sólo se aplicará un 8% de descuento. Realice un algoritmo para determinar el precio final que debe pagar una persona por comprar en dicho almacén y de cuánto es el descuento que obtendrá. Represéntelo mediante el pseudocódigo y el diagrama de flujo.


## Pseudocodigo

```
Inicio
Leer valor_compra > 250000
      Descuento = valor_compra * 0.15
Si no
      Descuento = valor_compra * 0.08
Fin Si
precio final = valor_compra - descuento
Mostrar "Valor a pagar $ ", precio_final
Fin
```
![E2](e2.png)