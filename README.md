Cifrador Cesar y Atbash utilizando base ASCII

1. Introduccion

Desde que el ser humano fue capaz de generar informacion escrita, tambien surgio la necesidad de protegerla. A lo largo de la historia se han desarrollado diferentes tecnicas de cifrado para evitar que terceros puedan interpretar mensajes sin autorizacion.
Uno de los primeros metodos de cifrado conocidos es el cifrado Cesar, atribuido a Julio Cesar, quien lo utilizaba para proteger mensajes militares. Este metodo consiste en desplazar las letras del alfabeto un numero determinado de posiciones.
Posteriormente surgieron otros metodos de sustitucion simple, como el cifrado Atbash, que consiste en invertir el alfabeto (primera letra por la ultima, segunda por la penultima, etc.).
Sin embargo, estos metodos presentan debilidades importantes. En el siglo IX, Abu Yusuf Yaqub ibn Ishaq al-Kindi desarrollo el analisis de frecuencia, una tecnica que permite romper cifrados por sustitucion analizando la frecuencia de aparicion de letras en un idioma. Este aporte marco el inicio formal del criptanalisis.
Gracias a este tipo de tecnicas, hoy se sabe que cifrados como Cesar y Atbash no son viables para proteger informacion real, ya que pueden romperse facilmente mediante fuerza bruta o analisis estadistico.
Aun asi, estos metodos siguen siendo fundamentales en el aprendizaje de la criptografia porque permiten comprender conceptos basicos como clave, sustitucion, desplazamiento y transformacion de caracteres.

2. Objetivo

Desarrollar una aplicacion web capaz de cifrar y descifrar mensajes utilizando los metodos clasicos Cesar y Atbash, tomando como base un conjunto de caracteres configurable por el usuario y permitiendo trabajar con el rango ASCII imprimible (32 a 126). Ademas, el sistema debe ser capaz de identificar el tipo de cifrado utilizado mediante un modulo de deteccion.

3. Desarrollo
   
3.1 Estructura general del sistema

El sistema fue desarrollado utilizando:
HTML para la estructura
CSS para el diseño visual
JavaScript para la logica del cifrado y descifrado

La aplicacion permite:
Seleccionar el modulo de cifrado (Cesar, Atbash o Detectar)
Seleccionar la accion (Cifrar o Descifrar)
Ingresar el texto
Definir el alfabeto manualmente
Cargar automaticamente el rango ASCII imprimible

3.2 Uso del codigo ASCII

El sistema puede trabajar con el conjunto de caracteres ASCII imprimibles, que corresponden a los codigos del 32 al 126.

Esto incluye:
Letras mayusculas y minusculas
Numeros
Signos de puntuacion
Simbolos especiales
Trabajar con ASCII permite que el cifrado no se limite solo a letras, sino que pueda incluir caracteres especiales dentro del proceso de transformacion.

3.3 Funcionamiento del cifrado Cesar

El cifrado Cesar funciona desplazando cada caracter dentro del alfabeto un numero determinado de posiciones (shift).

Si el desplazamiento es positivo, se cifra.
Si es negativo, se descifra.
El sistema utiliza aritmetica modular para evitar errores cuando se llega al final del alfabeto.

Ejemplo:

Texto original: HOLA
Shift: 3
Resultado: KROD

3.4 Funcionamiento del cifrado Atbash

El cifrado Atbash es un metodo de sustitucion fija.
Cada caracter es reemplazado por su correspondiente "espejo" dentro del alfabeto:
Primero ↔ Ultimo
Segundo ↔ Penultimo
Este metodo es involutivo, lo que significa que aplicar el proceso dos veces devuelve el texto original.

3.5 Modulo Detectar

El modulo Detectar intenta identificar automaticamente si un texto fue cifrado con Cesar o Atbash.

Para ello:

Aplica Atbash al texto y evalua si el resultado parece legible.
Prueba diferentes desplazamientos de Cesar.
Asigna un puntaje segun cantidad de espacios, letras y numeros.
Selecciona la opcion con mayor puntaje como la mas probable.
Este metodo es una aproximacion educativa y no garantiza una deteccion perfecta.

3.6 Seguridad del sistema

Este sistema es academico y no esta diseñado para proteger informacion real.

Debilidades del cifrado Cesar:

Numero limitado de desplazamientos posibles.
Puede romperse por fuerza bruta.
Vulnerable a analisis de frecuencia.
Debilidades del cifrado Atbash:
Sustitucion fija sin clave.
Facil de invertir.
Vulnerable a tecnicas estadisticas.
En la actualidad se utilizan algoritmos criptograficos modernos como AES o RSA, que emplean claves largas y operaciones matematicas complejas.

3.7 Publicacion y documentacion segura

El proyecto se encuentra publicado en:

Repositorio GitHub (codigo fuente documentado)
Plataforma Vercel (programa funcionando en la web)
La documentacion se entrega de manera digital, evitando impresiones fisicas, y el repositorio es de solo lectura, lo que garantiza integridad del codigo.

4. Conclusion

Con la investigacion posterior y el desarrollo de este programa aprendi de la gran importancia del cifrado para quizas informacion importante que puede ser delicada, tambien me permitio comprender de manera practica el funcionamiento de cifrados clasicos y sus debilidades frente a tecnicas de criptanalisis desarrolladas desde la epoca de Al-Kindi.
Aunque estos metodos no son seguros en la actualidad, representan la base historica sobre la cual se construyeron los sistemas criptograficos modernos. 
El uso del cifrado en los sistemas de seguridad social es una herramienta fundamental para garantizar la protección de la información sensible de los ciudadanos. Datos como historial médico, número de afiliación, aportaciones económicas y registros personales requieren un alto nivel de confidencialidad, ya que cualquier vulneración puede afectar directamente la privacidad y seguridad de las personas.
Implementar mecanismos de cifrado no solo fortalece la seguridad informática de las instituciones, sino que también genera confianza en los usuarios al saber que su información está protegida frente a accesos no autorizados, fraudes o ataques cibernéticos. Además, el cifrado contribuye al cumplimiento de normativas legales relacionadas con la protección de datos personales.
El proyecto demuestra la relacion entre teoria criptografica y aplicacion practica mediante una herramienta web funcional. 

5. Bibliografia

National Institute of Standards and Technology (NIST). (2023). Advanced Encryption Standard (AES). https://nvlpubs.nist.gov

https://faculty.ksu.edu.sa/sites/default/files/cryptography-network-security-5th-edition.pdf?utm_source

https://es.wikipedia.org/wiki/ISO/IEC_27002?utm_source=chatgpt.com

Katz, J., & Lindell, Y. (2014). Introduction to Modern Cryptography.

Singh, S. (1999). The Code Book.

Wikipedia. Caesar cipher.

Wikipedia. Atbash cipher.

Documentacion oficial ASCII.
