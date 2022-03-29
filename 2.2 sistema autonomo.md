# Sistemas autónomos

![Texto alternativo](https://www.mikrotiklabs.com/wp-content/uploads/2019/09/OSPF-image.png)

>Un sistema autónomo es un grupo de redes y pasarelas de las que es responsable una autoridad administrativa.

Las pasarelas son vecinos interiores si residen en el mismo sistema autónomo y vecinos exteriores si residen en sistema autónomos diferentes. Las pasarelas que intercambian información de direccionamiento utilizando EGP se conocen como iguales o vecinos EGP. Las pasarelas de sistemas autónomos utilizan EGP para proporcionar información de acceso a los vecinos EGP.

EGP permite a una pasarela exterior solicitar a otra pasarela exterior que acceda a intercambiar información de acceso, comprueba continuamente que los vecinos EGP respondan y ayuda a los vecinos EGP a intercambiar información de acceso pasando mensajes de actualización de direccionamiento.

EGP restringe las pasarelas exteriores permitiéndoles anunciar sólo las redes de destino totalmente alcanzables dentro del sistema autónomo de esa pasarela. De este modo, una pasarela exterior que utiliza EGP pasa información a los vecinos EGP pero no anuncia información de acceso acerca de los vecinos EGP fuera del sistema autónomo.

EGP no interpreta ninguna de la métrica de distancia que aparecen en los mensajes de actualización de direccionamiento de otros protocolos. EGP utiliza el campo de distancia para especificar si existe una vía de acceso (un valor de 255 significa que no se puede alcanzar la red). El valor no se puede utilizar para calcular la ruta más corta entre dos, a menos que ambas rutas estén contenidas en un solo sistema autónomo. Por consiguiente, EGP no se puede utilizar como algoritmo de direccionamiento. Como resultado, sólo habrá una vía de acceso de la pasarela exterior a cualquier red.

A diferencia de RIP (Routing Information Protocol - Protocolo de información de direccionamiento), que se puede utilizar en un sistema autónomo de redes de Internet que reconfiguran dinámicamente las rutas, las rutas de EGP están predeterminadas en el archivo /etc/gated.conf. EGP supone que IP es el protocolo subyacente.

## ¿Qué son sistemas autónomos y sistemas no autónomos?
>En pocas palabras, los sistemas autónomos se caracterizan por la capacidad de actuar con independencia del control humano directo, mientras que los sistemas automatizados no. Cuando se trata de sistemas autónomos en la industria, un objetivo justo y alcanzable es aspirar al Nivel 3 de la NHTSA

 ### Referencia  Bibliografica

 https://new.abb.com/news/es/detail/28920/sistemas-autonomos
 
https://www.ibm.com/docs/es/aix/7.1?topic=protocol-autonomous-systems

