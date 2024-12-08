# descifrador_hash.py
# generar_diccionario.py

Este script (descifrador_hash.py) hace lo siguiente:

1. Implementa funciones para hashear contraseñas y para intentar descifrar un hash dado usando un archivo de diccionario.
2. Soporta los algoritmos de hash MD5, SHA1 y SHA256.
3. Utiliza `argparse` para manejar los argumentos de línea de comandos, lo que hace que el script sea más flexible y fácil de usar.
4. Maneja posibles errores, como archivos de diccionario no encontrados.


Para usar este script:

1. Guárdalo como `descifrador_hash.py`.
2. Prepara un archivo de diccionario (una lista de contraseñas potenciales, una por línea).
3. Ejecuta el script desde la línea de comandos. Por ejemplo:

```plaintext
python descifrador_hash.py 5f4dcc3b5aa765d61d8327deb882cf99 mi_diccionario.txt
```

Esto intentará descifrar el hash MD5 de "password" usando el diccionario "mi_diccionario.txt".


4. Para usar un algoritmo diferente, agrega el argumento `--algorithm`. Por ejemplo:

```plaintext
python descifrador_hash.py 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8 mi_diccionario.txt --algorithm sha1
```




Consideraciones importantes:

1. Este script es para fines educativos y de pruebas de seguridad. Úsalo solo en sistemas para los que tengas permiso explícito.
2. El éxito del descifrado depende de que la contraseña esté en el diccionario utilizado.
3. Los hashes son unidireccionales; este método prueba cada palabra del diccionario, no "descifra" el hash en el sentido tradicional.
4. Para contraseñas seguras, este método no debería tener éxito, lo que demuestra la importancia de usar contraseñas fuertes y técnicas de hashing adecuadas (como salting y algoritmos de derivación de claves).

   Este script hace lo siguiente:

1. Define una función `generar_diccionario` que crea un archivo de texto con una lista de contraseñas comunes.
2. Escribe cada contraseña en una nueva línea del archivo.
3. Después de generar el archivo, lee y muestra su contenido para verificación.


Para usar este script (generar_diccionario.py):

1. Guárdalo como `generar_diccionario.py`.
2. Ejecuta el script con Python: `python generar_diccionario.py`.
3. El script creará un archivo llamado `diccionario_contraseñas.txt` en el mismo directorio.


Advertencias importantes:

1. Este diccionario contiene contraseñas muy comunes y débiles. Nunca uses estas contraseñas para tus propias cuentas.
2. El propósito de este diccionario es educativo y para pruebas de seguridad autorizadas.
3. Usar este tipo de diccionario para intentar acceder a sistemas sin autorización es ilegal y poco ético.


Este diccionario puede ser utilizado con el script de descifrado de hash que creamos anteriormente. Por ejemplo:

```plaintext
python descifrador_hash.py 5f4dcc3b5aa765d61d8327deb882cf99 diccionario_contraseñas.txt
```

Esto intentaría descifrar el hash MD5 de "password" usando el diccionario que acabamos de crear.
