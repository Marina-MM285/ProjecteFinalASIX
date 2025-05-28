# Problemas y Soluciones

## Reserva de dirección IP en router cisco

**Problema**

En la configuracion de reserva de direciones IP de cisco no me dejaba reservar la direccion pq aparecia el error de que la MAC ya tenia una dirección assignada

**Solución**

Tenia que encender el equipo sin que tuviera el dhcp activado para poder reservar la ip sin problemas



## Conexión entre las dos diferentes redes y a internet

**Problema**

Una vez hechas las configuraciones de los 2 ubuntu, es decir, la pagina web y la base de datos de MySQL las todos los equipos podian acceder a internet pero no a la otra red. Necesitaba que las dos redes se pudieran ver para poder hacer el servicio de archivos en los dos equipos windows.

**Solución**

Estuve haciendo pruebas, primero con dos router cisco con y sin internet y conexión entre las dos redes, luego lo mismo con dos router mikrotik. Cuando hice la prueba de un cisco y un mikrotik sin acceso a internet no me dio ningún tipo de problema, pero al hacer el nateo fue cuando no se puedieron ver, de la red del cisco a la red del mikrotik si, pero de la red del mikrotik a la red del cisco no.
Busqué información y según lo que encontré deduje que los paquetes que se estaban enviando hacia los equipos del cisco, a la vuelta, el router los confundia con paquetes de internet y los pasaba por nat, por lo que no llegaban a la otra red.

Después de probar 3 configuraciones diferentes que encontré en foros, seguía sin funcionar, ya que si la red del cisco tenia acceso a internet pero al mismo tiempo podia ver la red del mirkotik salían fallos con el nat y dejaba de funcionar el nateo.

Después de todas las pruebas realizadas me di cuenta que la solución más viable que tenia en ese momento era dejar el cisco sin nateo pero que puediera ver la otra red. Como ya tenia todas las demas configuraciones hechas, no tenia necesidad de usar internet.

**Explicación**

Después de haber explicado el problema y la solución, una que me gustaría haber evitado, busqué una explicación por la que ha salido dicho error.

Cisco un modelo estructurado basado en listas de acceso, donde todo el trafico se traduce según las reglas  de manera más explícita. El cisco puede llegar a traducir todos los paquetes salientes, incluidos los paquetes del mikrotik.

Mikrotik, por otro lado, usa reglas de firewall, que es más flexible pero depende del orden de las reglas. Si la regla del NAT se aplica antes, el tráfico podría ser traducido.

Cuando usamos dos ciscos o dos mikrotiks, las configuraciones son expresadas de la misma forma, en cambio, al mezclarlos, la diferencia de cómo se procesan los distintos paquetes puede generar incompatibilidad.

## Instalación de agentes de pandora

**Problema**

En el despliegue de los agentes de pandora, nos indicaba los comando para instalar el agente, después de varios intentos con ellos no funcionaros ni en Ubuntu ni en Windows.

**Solución**

Busqué en la pagina oficial de Pandora a ver si habia otra forma de hacerlo y pude descargar directamente el archivo que necesitaba para instalar el agente y activar el daemon. De esta forma ya me aparecian los agentes en Pandora.


## Alertas con Telegram
**Problema**
Intenté crear mi propia alarma, con un comando que encontré por internet, pero cuando simulaba el fallo no se me enviaba ningún mensaje al chat que habia creado.



