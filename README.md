# Punto Estrella

Un Nombre de Dominio Internacionalizado (IDN) es un nombre de internet que contiene caracteres no ASCII (*American Standard Code for Information Interchange*), es decir, que se puedan incluir caracteres diferentes del alfabeto latino. Fue diseñado para una máxima compatibilidad hacia atrás con el sistema de nombres de dominio (DNS)existente, es una abstracción a nivel del usuario, que le permite encontrar páginas web.

Se decidió que los nombres de dominio con caracteres no-ASCII deben ser convertidos a una forma basada en ASCII por los navegadores web y otras aplicaciones de usuario.

El algoritmo se basa en la codificación ASCII Punycode para pasar cadenas de caracteres de Unicode a ASCII. Si una etiqueta dada contiene al menos un carácter no ASCII, el algoritmo primero convierte la cadena a minúsculas (normalización), luego se identifican las cadenas no ASCII y se las sustituye por su forma codificada usando Punycode y separandolas por un guión dependiendo si el caracter especial tiene cadenas a la izquierda o derecha. Por otra parte hay que anteponer antes la cadena de cuatro caracteres "xn--" que se la denomina prefijo ACE, significa ASCII Compatible Encoding, y se utiliza para distinguir las etiquetas codificadas en Punycode de las etiquetas ASCII ordinarias.

Por ejemplo, si tenemos el siguiente IDN "💩.la", contiene un emoji no incluido dentro de los caracteres permitidos por ASCII, entonces debe codificarse mediante punycode se dejará sin cambio la etiqueda "la", pero se modificará "💩". Como explicamos anteriormente se aplica el algoritmo y se normaliza la cadena, se antepondra el prefijo ACE (xn--) y como cada emoji tiene una repretación única en punycode la representación final esta dada por "xn--ls8h.la". 

En el caso de "中文.tw/" la traducción se realiza de la misma forma y se tiene como resultado "xn--fiq228c.tw/", a su vez "ñandu.cl" tiene como resultado " xn--andu-fqa.cl" y "müllers-café.com" tenemos "xn--mllers-caf-k7a2t.com".

Cabe resaltar que esto presenta algunos problemas como que el soporte entre los registradores de nombres de dominio para dominios emoji es limitado.​

Otro problema es que los emojis pueden verse diferentes según el sistema operativo, las aplicaciones y las fuentes utilizadas.​ No todos los navegadores soportan dominios emoji. En Google Chrome y Firefox , los emoji se muestran como Punycode en la barra de direcciones. En Safari, por otro lado, los emoji son visibles en la barra de direcciones.​

## Referencias

- https://es.wikipedia.org/wiki/Dominio_emoji
- https://es.wikipedia.org/wiki/Nombre_de_dominio_internacionalizado
- https://hmong.es/wiki/Emoji_domain
- https://rockcontent.com/es/blog/dns/#:~:text=DNS%20es%20la%20sigla%20en,permite%20el%20acceso%20a%20Internet
- https://www.punycoder.com/