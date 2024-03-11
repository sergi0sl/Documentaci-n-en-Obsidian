
Puede exportar las políticas a un servidor de directorios. Lea esta nota para ver los conceptos y la configuración de LDAP (Lightweight Directory Access Protocol), así como el esquema de calidad de servicio (QoS).

La configuración de la política QoS se puede exportar a un servidor de directorios, utilizando LDAP versión 3.

## Cómo utilizar un servidor de directorios

La exportación de políticas de QoS a un servidor de directorios facilita la gestión de las políticas. Existen tres formas de utilizar el servidor de directorios:

- Los datos de configuración se pueden almacenar en un servidor de directorios local para que los compartan muchos sistemas.
- Los datos de configuración se pueden configurar, almacenar y utilizar sólo por un sistema (no compartido).
- Los datos de configuración pueden residir en un servidor de directorios que contiene datos para otros sistemas, pero no se comparte entre esos otros sistemas. Esto le permite utilizar una única ubicación para realizar una copia de seguridad y guardar datos para varios sistemas.

## Ventajas de ahorrar exclusivamente en su sistema local

Guardar las políticas de QoS en el sistema local no es tan complejo. Existen varias ventajas al utilizar las políticas localmente:

- Elimine la complejidad de la configuración LDAP para los usuarios que no la necesitan.
- Mejore el rendimiento, porque escribir en LDAP no es el método más rápido.
- Duplique una configuración entre distintos sistemas más fácilmente. Puede copiar el archivo de un sistema a otro. Puesto que no hay ninguna máquina primaria o secundaria, puede adaptar cada política directamente en los sistemas individuales.

## Recursos LDAP

Si decide exportar las políticas a un servidor LDAP, debe estar familiarizado con los conceptos LDAP y las estructuras de directorios antes de continuar. Dentro de la función QoS en IBM® Navigator for i, puede configurar un servidor de directorios que se utilice con la política QoS .

- **Palabras clave**
    Al configurar el servidor de directorios, debe determinar si desea asociar palabras clave con cada configuración de calidad de servicio (QoS).
- **Nombre distinguido** 
    Cuando desee gestionar parte del directorio, haga referencia al nombre distinguido (DN) o (si lo desea) a una palabra clave.