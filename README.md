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
- Version de nginx:
![image](https://user-images.githubusercontent.com/94164299/212838484-557cd52d-7ad1-476d-9f7c-1869bf7e046b.png)
-------------------------------------------------------------------
- Ficheros de configuracion de nginx:
![image](https://user-images.githubusercontent.com/94164299/212838930-feac044d-869c-4c48-807f-6c0f5c611157.png)
-------------------------------------------------------------------
- Modificar pagina web: 
![image](https://user-images.githubusercontent.com/94164299/212840943-cbbfc5f2-2a47-4c67-9f45-e4da71a8a9df.png)
![image](https://user-images.githubusercontent.com/94164299/212841415-4fc83913-d5c2-490e-bcc7-5ebe083be5b5.png)
![image](https://user-images.githubusercontent.com/94164299/212841467-9c880e42-5f37-4da6-aa50-59fcddb128b9.png)
-------------------------------------------------------------------
- Virtual hosting:
![image](https://user-images.githubusercontent.com/94164299/212846418-d32a784b-daef-4ac8-bdd5-d80aa1fc401b.png)
![image](https://user-images.githubusercontent.com/94164299/212846789-415cfd19-640e-4045-8af9-c2468fbb9498.png)
![image](https://user-images.githubusercontent.com/94164299/212847152-1e48b854-9011-40b7-b441-fa0565fdd4fd.png)
![image](https://user-images.githubusercontent.com/94164299/212847874-70712f00-3855-4be1-9bb5-0fd1a0de2f5c.png)
![image](https://user-images.githubusercontent.com/94164299/212849390-424a4b75-3d17-4403-a014-712bc5cd2f25.png)
![image](https://user-images.githubusercontent.com/94164299/212850043-706f9e48-660b-4727-9915-5f3aadadcc24.png)




## 5-Referencias
- https://learn.microsoft.com/es-es/troubleshoot/developer/webapps/aspnetcore/practice-troubleshoot-linux/2-2-install-nginx-configure-it-reverse-proxy
- https://marketersgroup.es/diferencias-entre-apache-y-nginx/#:~:text=El%20servidor%20de%20Apache%20tiene,velocidad%20y%20mejora%20el%20rendimiento.
- https://kinsta.com/es/base-de-conocimiento/que-es-nginx/
- https://help.clouding.io/hc/es/articles/360019908839-Cómo-configurar-un-servidor-de-balanceo-de-carga-Nginx-en-Ubuntu-20-04
