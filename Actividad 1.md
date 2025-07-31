## Ejercicios finales de repaso.
1. Explica, en tus propias palabras, por qué es necesario que las computadoras representen los datos en binario.

R/: Las computadoras usan binarios porque sus circuitos solo pueden distinguir dos estados: encendido (1) y apagado (0). Así, pueden procesar y almacenar toda la información de manera simple y eficiente usando solo ceros y unos.

2. Convierte el número binario 10011011 a decimal y a hexadecimal.
R/: Cada cifra del número binario representa una potencia de 2, comenzando desde la derecha (posición 0):

Posición	7	6	5	4	3	2	1	0

Potencia de 2	128	64	32	16	8	4	2	1

Dígito	1	0	0	1	1	0	1	1

## Multiplicamos cada dígito por su potencia y sumamos:

1 × 128 = 128
0 × 64 = 0
0 × 32 = 0
1 × 16 = 16
1 × 8 = 8
0 × 4 = 0
1 × 2 = 2
1 × 1 = 1
Total: 128 + 16 + 8 + 2 + 1 = 155

**Ahora en hexadecimal** 
Agrupamos el número binario en dos bloques de 4 bits:

1001 (izquierda) → 9
1011 (derecha) → B
Hexadecimal: 9B

3. Investiga y describe cómo se representa una imagen en formato PNG en el disco.
R/: Copiloto dijo: Una imagen en formato PNG se representa
Una imagen en formato PNG se representa en el disco como un archivo que almacena los datos de la imagen siguiendo el estándar PNG (Portable Network Graphics). Este archivo contiene una serie de  "chunks"  (bloques de datos) organizados de manera específica:

**Encabezado :** Comienza con una firma de 8 bytes que identifica el archivo como PNG.

**Bloques de datos ("chunks")** : Cada fragmento tiene un propósito específico:
- IHDR : Contiene información básica (ancho, alto, profundidad de color, tipo de color).
- IDAT : Guarda los datos de la imagen comprimidos (usando el algoritmo zlib/deflate).
- PLTE : (opcional) Paleta de colores usada en la imagen.
texto : (opcional) Metadatos como comentarios.
- IEND : Marca el final del archivo.
Los datos de la imagen (píxeles) se almacenan en comprimidos para reducir el tamaño del archivo sin perder calidad. Además, PNG soporta transparencias a través del canal alfa.

En resumen: Un archivo PNG en disco es una secuencia de estructura de bloques que contienen datos comprimidos, metadatos y parámetros de la imagen, permitiendo almacenar gráficos con alta calidad y transparencia.

4. Analiza la siguiente situación: ¿Qué sucede si intentas almacenar un número mayor al que puede representar un byte (por ejemplo, 300)? ¿Cómo lo maneja Python?
R/: Si intentas almacenar un número mayor al que puede representar un byte (por ejemplo,  300 ) en un solo byte, ese valor no cabe, ya que un byte solo puede representar valores entre  0  y  255 .

En Python, si usas un tipo de datos estándar como  int , no hay problema porque Python puede manejar números mucho más grandes que un byte. Pero si trabajas con bytes directamente (por ejemplo, usando  bytes  o  bytearray ), y tratas de poner el valor  300  en una posición, Python genera un error:

b = bytearray(1)
b[0] = 300  # error: ValueError: byte must be in range(0, 256)

**En resumen:**
Python no permite guardar  300  en un solo byte y lanza un error si lo intentas. Si necesitas almacenar números más grandes, tienes que usar más bytes (por ejemplo, dos bytes para valores de 0 a 65535).