# Modelo OSI

## ¿Qué es el modelo OSI?

- El modelo de interconexión de sistemas abiertos (Open Systems Interconnection, OSI) es un `marco conceptual` que divide las funciones de comunicaciones de red en siete capas

- Proporciona un lenguaje universal para las redes informáticas

## ¿Por qué es importante el modelo OSI?

Las capas del modelo de interconexión de sistemas abiertos (OSI) encapsulan todos los tipos de comunicación de red en los componentes de software y hardware

El modelo se diseñó para permitir que dos sistemas independientes se comuniquen a través de interfaces o protocolos estandarizados basados en la capa de operación actual

## Beneficios del modelo OSI

- Comprensión compartida de sistemas complejos

- Investigación y desarrollo más rápidos

- Estandarización flexible


## Capas del modelo OSI

1. Capa física
2. Capa de enlace de datos
3. Capa de red
4. Capa de transporte
5. Capa de sesión
6. Capa de presentación
7. Capa de aplicación

## Capa física

- Se refiere al medio de comunicación físico y a las tecnologías para transmitir datos a través de ese medio

- La comunicación de datos es la transferencia de señales digitales y electrónicas a través de varios canales físicos, como cables de fibra óptica, NFC, bluetooth, cableado de cobre y aire

## Capa de enlace de datos

- La capa de enlace de datos se refiere a las tecnologías utilizadas para conectar dos máquinas a través de una red donde la capa física ya existe

- Ethernet es un ejemplo de un estándar a este nivel

- La capa de enlace de datos a menudo se divide en dos subcapas: la capa de control de acceso a los medios (MAC) y la capa de control de enlace lógico (LLC)

## Capa de red

- La capa de red se ocupa de conceptos como el enrutamiento, el reenvío y el direccionamiento a través de una red dispersa o de múltiples redes conectadas de nodos o máquinas, gestionar el control de flujo

- El Protocolo de Internet IPv4 y el IPv6 se utilizan como protocolos de capa de red principales

## Capa de transporte

- El objetivo principal de la capa de transporte es garantizar que los paquetes de datos lleguen en el orden correcto, sin pérdidas ni errores, o que se puedan recuperar sin problemas si es necesario

- El control del flujo, junto con el control de errores, suele ser un objetivo en la capa de transporte

### Protocolos de uso común
  
1. Protocolo de Control de Transmisión (TCP), es un protocolo basado en conexiones casi sin pérdidas
2. Protocolo de datagramas de usuario (UDP), un protocolo sin conexiones con pérdidas

## Capa de sesión

- La capa de sesión es responsable de la coordinación de la red entre dos aplicaciones independientes en una sesión

- Una sesión gestiona el inicio y el final de los conflictos de sincronización y conexión de una aplicación uno a uno

## Procolos de uso común

1. Network File System (NFS)
2. Server Message Block (SMB)

## Capa de presentación

- La capa de presentación se ocupa principalmente de la sintaxis de los datos en sí para que las aplicaciones los envíen y consuman

Ej: el lenguaje de marcas de hipertexto (HTML), la notación de objetos JavaScript (JSON) y los valores separados por comas (CSV) son lenguajes de modelado para describir la estructura de los datos en la capa de presentación

## Capa de aplicación

- La capa de aplicación se refiere al tipo específico de aplicación en sí y a sus métodos de comunicación estandarizados

Ejemplos

1. Los navegadores pueden comunicarse mediante el Protocolo seguro de transferencia de hipertexto (HTTPS)
2. Los clientes de correo electrónico y HTTP pueden comunicarse mediante POP3 (Protocolo de oficina de correo versión 3) y SMTP (Protocolo simple de transferencia de correo)

## ¿Cómo se comunica el modelo OSI?

1. La capa de aplicación del remitente transfiere la comunicación de datos a la capa inferior
2. Cada capa añade sus propios encabezados y direccionamientos a los datos antes de transmitirlos
3. La comunicación de datos desciende por las capas hasta que finalmente se transmite a través del medio físico
4. En el otro extremo del medio, cada capa procesa los datos de acuerdo con los encabezados relevantes en ese nivel
5. En el extremo receptor, los datos suben por la capa y se desempaquetan gradualmente hasta que la aplicación del otro extremo los recibe

---

## A TENER EN CUENTA, No todos los sistemas que utilizan el modelo OSI implementan todas las capas

---

Creado por Favio Joel Zalazar

Fuentes consultadas https://aws.amazon.com/es/what-is/osi-model/
