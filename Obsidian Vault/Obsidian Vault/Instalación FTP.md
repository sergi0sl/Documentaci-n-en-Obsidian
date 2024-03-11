### Paso 1: Instalar el servidor FTP (en este caso, vsftpd)
```
sudo apt update
sudo apt install vsftpd

```
### Paso 2: Configurar el servidor FTP

Editar el archivo de configuración `/etc/vsftpd.conf` utilizando un editor de texto como nano o vi.
```
sudo nano /etc/vsftpd.conf

```
Aquí tienes algunas configuraciones básicas que podrías ajustar:

- **anonymous_enable**: Cambiar a NO si no deseas permitir conexiones anónimas.
- **local_enable**: Cambiar a YES si deseas permitir a los usuarios locales conectarse.
- **write_enable**: Cambiar a YES si deseas permitir a los usuarios escribir en el servidor.
- **chroot_local_user**: Cambiar a YES si deseas que los usuarios estén limitados a su directorio de inicio.
### Paso 3: Reiniciar el servidor FTP para aplicar los cambios en la configuración

```
sudo systemctl restart vsftpd

```

### Paso 4: Configurar el firewall (si es necesario)

Si estás usando un firewall, como UFW en Ubuntu, asegúrate de permitir conexiones FTP.
```
sudo ufw allow 20/tcp
sudo ufw allow 21/tcp

```

### Paso 5: Verificar el estado del servidor FTP

Puedes verificar que el servidor FTP esté ejecutándose correctamente con el siguiente comando:

```
sudo systemctl status vsftpd

```

### Paso 6: Acceder al servidor FTP

Puedes acceder al servidor FTP utilizando un cliente FTP, como FileZilla, utilizando la dirección IP de tu servidor y el puerto 21. Ingresa con un nombre de usuario y contraseña válidos.


>NOTA: Esto es solo un ejemplo para trabajar con la importación de códigos, no por ello los códigos y pasos anteriores tienen que estar bien.