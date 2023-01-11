# Nginx-ajustes-basicos
## 1-Introducción
- Nginx es un servidor web que también se puede utilizar como proxy inverso, equilibrador de carga, proxy de correo y caché HTTP. El software fue creado por Igor Sysoev y lanzado públicamente en 2004. Nginx es un software gratuito y de código abierto, lanzado bajo los términos de la licencia BSD de 2 cláusulas.
## 2-Comparativa con apache
- Existen diferencias entre estos servidores, las cuales debes conocer para que puedas tomar la decisión más adecuada:
    
    - Sistema operativo: Compatibilidad
        - Ambos servidores funcionan bien en sistemas como UNIX, LINUX y variaciones. Sin embargo, si el sistema operativo que se quiere usar es Windows, Apache tiene           una mejor performance que Nginx. 
    
    - Administración y mantenimiento
        - Por un lado, en Apache el soporte, las actualizaciones, el desarrollo y la corrección de errores es realizado por una comunidad de desarrolladores de todo el           mundo apoyados por la Fundación de software de Apache. Mientras, en Nginx, todo el soporte y la administración es realizada por la compañía que la creó. 
    
    - Rendimiento o ‘performance’
        - El servidor de Apache tiene un sólo hilo que está asociado con una sola conexión. Por otro lado, Nginx tiene la capacidad de manejar miles de conexiones que           se gestionan de forma simultánea. Esto reduce la memoria, aumenta la velocidad y mejora el rendimiento.
    
    - Escalabilidad de la arquitectura 
        - Nginx sigue un enfoque que se basa en eventos asíncronos que sirven para poder administrar varias solicitudes de clientes. Esta arquitectura de Nginx basada           en eventos es lo que permite tener un rendimiento mayor incluso si se trata de un tráfico pesado. Esto no es posible con Apache, ya que tiene una                       arquitectura de subprocesos múltiples que hacen difícil que esta escalabilidad se pueda lograr. 
    
    - Procesamiento de contenido dinámico
        - Apache procesa contenido dinámico de forma nativa dentro del propio servidor web, algo que Nginx carece porque no tiene la capacidad de hacerlo internamente.           Nginx depende de procesos que sólo se pueden ejecutar externamente.
## 3-Instalacion
- La instalación de Nginx es sencilla. Ejecute el sudo apt install nginx comando para instalar el programa en la máquina virtual Ubuntu, aunque en nuestro caso será una maquina debian (entramos en modo administrador con el comando "su -" y realizamos un "apt install nginx"). Una vez finalizada la instalación, ejecute whereis nginx para descubrir dónde está instalado el programa.
## 4-Casos practicos
- Nginx está diseñado para ofrecer un bajo uso de memoria y alta concurrencia. En lugar de crear nuevos procesos para cada solicitud web, Nginx usa un enfoque asincrónico basado en eventos donde las solicitudes se manejan en un solo hilo. Con Nginx, un proceso maestro puede controlar múltiples procesos de trabajo. El proceso maestro mantiene los procesos de trabajo, y son estos lo que hacen el procesamiento real.

- Algunas características comunes que se ven en Nginx incluyen:

    - Proxy inverso con caché
    - IPv6
    - Balanceo de carga
    - Soporte FastCGI con almacenamiento en caché
    - Websockets
    - Manejo de archivos estáticos, archivos de índice y auto indexación
    - TLS / SSL con SNI
## 5-Referencias
- https://learn.microsoft.com/es-es/troubleshoot/developer/webapps/aspnetcore/practice-troubleshoot-linux/2-2-install-nginx-configure-it-reverse-proxy
- https://marketersgroup.es/diferencias-entre-apache-y-nginx/#:~:text=El%20servidor%20de%20Apache%20tiene,velocidad%20y%20mejora%20el%20rendimiento.
- https://kinsta.com/es/base-de-conocimiento/que-es-nginx/
