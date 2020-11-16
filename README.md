# Botic Cliente

###### Este es la instalación de parte del Cliente de la aplicación Botic, para poder realizar esta guía tiendrá que tener instalado la aplicación de Botic en su ordenador. Si no cuenta con la aplicación, consulte la [guía de instalación de Botic](https://github.com/Luisgc98/Boticenv1/blob/main/README.md) para poder realizar este instructivo.
   ###### - [Guía de Instalación Botic](https://github.com/Luisgc98/Boticenv1/blob/main/README.md)


#### <h4>Descarga del repositorio botic-autoengine</h4>

   - Si cuentas con un sistema Windows, puedes continuar con el siguiente paso. En el caso de los ordenadores Linux, para este paso, git ya debería de contar con la configuración inicial del usuario, sino es así, consulte [la guía de instalación de Botic](https://github.com/Luisgc98/Boticenv1#instalaci%C3%B3n-git-en-linux) en la parte de instalación git Linux.

   - Para descargar este repositorio haremos uso de los comandos de git, en caso de Windows usa la línea de comandos de git. Descargaremos este repositorio de la rama 3.0.0b:
      
      ```bash
        $ git clone -b 3.0.0b https://github.com/brik18/botic-autoengine.git
      ```
   - Se descargará un directorio llamado botic-autoengine, donde se encontrará alojado toda la configuración de los bots, y donde se hará la conexión de nuestro ordenador como bot en la aplicación. Es en este directorio en donde vamos a estar trabajando.
   
#### <h4>Crear el ambiente virtual en botic-autoengine y conexión de nuestro ordenador como bot en la aplicación de Botic</h4>
   ###### Para este paso, el servidor de su aplicación Botic tiene que estar desplegada de manera local en su ordenador.
       
   - Antes de crear nuestro ambiente virtual nos tenemos que posicionar en la carpeta de botic-autoengine, una vez ahí proseguimos con el
      siguiente paso.

   - Para crear ambientes virtuales con Python 3.7.4, usamos el siguiente comando, reemplazando "tu_ambiente_virtual" por el nombre
      que le quieras poner a tu ambiente:
      
   ```bash
        $ python3.7 -m venv tu_ambiente_virtual
   ```
    
   - Terminando el proceso, nos aparecerá una carpeta con el nombre que le hayamos puesto a nuestro ambiente virtual.
      Para activarlo usamos el siguiente comando:
      
   ```bash
        $ source tu_ambiente_virtual/bin/activate
   ```
   
   - Al activarlo nos marcará entre parentesis el nombre de nuestro ambiente:
   
   ```bash
        (tu_ambiente_virtual) $ 
   ```
    
   - Una vez activado nuestro ambiente, proseguimos con la instalación de los requerimientos para la configuración de automagica (que es la herramienta con la que se hacen las diferentes acciones posibles en la app), para esto usamos el siguiente comando:
    
   ```bash
        (tu_ambiente_virtual) $ python3.7 -m pip install .
   ```

   - Una vez terminando la instalación, proseguimos con la configuración de automagica, para esto usamos el siguiente comando:
     ###### Nota: puede haber errores al usar la orden "python3.7", así que usaremos la orden única "python".

   ```bash
        (tu_ambiente_virtual) $ python -m autoengine.cli configure
   ```

   - Al accionar este comando, nos aparecerá una opción para registrar una URL donde se hará la conexión con el portal de nuestra aplicación Botic. Aquí usted debe ingresar la URL donde corren nuestros servicios Rest, o sea, el servidor que corre en el puerto 5002: 

   ```bash
        Bot Player Configuration

        To register bot player you need login with portal
        Leave a value empty to enter the proposed or default value between [brackets].

        Portal URL []:http://127.0.0.1:5002
   ```

   - Luego nos pedirá una "User Secret", para esto iremos a nuestra aplicación Botic, en la sección donde se encuentra nuestro correo, se desplegará un menú donde se encontrará el apartado de "Perfil", ingresamos y en la parte izquierda, habrá una sección que se llama "secret key": 

   ![dates_profile](https://lh3.googleusercontent.com/-W9R0KBc098Y/X7IKSVdm-_I/AAAAAAAAFXg/4ewK2qOHr7Mrbuczu5UlhAspKPTyD_OfwCK8BGAsYHg/s0/Captura%2Bde%2Bpantalla%2Bde%2B2020-11-15%2B23-12-23.png)

   - Copiamos la llave y la pegamos en nuestra terminal:

   ```bash
        Bot Player Configuration

        To register bot player you need login with portal
        Leave a value empty to enter the proposed or default value between [brackets].

        Portal URL []:http://127.0.0.1:5002
        User Secret []:your_user_secret
   ```

   - Echo esto, nuestro ordenador quedará registrada como un bot en la aplicación de Botic. Podemos confirmarlo en la [página principal de Botic](http://127.0.0.1:5000/index), donde podremos ver un recuadro en la parte de la izquiera con el nombre de nuestro ordenador: 

   ![cpu_bot](https://lh3.googleusercontent.com/-oLppsa0ipVc/X7INTdalvUI/AAAAAAAAFYQ/Fi7S_HknHmwwzON5QOE0veNstJhQWwA6wCK8BGAsYHg/s0/Captura%2Bde%2Bpantalla%2Bde%2B2020-11-15%2B23-25-22.png)

   - Como podremos observar, el estado de este bot se encuentra desconectado. Para activarlo vamos a la línea de comandos donde tenemos activado nuestro ambiente virtual de la carpeta botic-autoengine, e ingresamos el siguiente comando:

   ```bash
        python -m autoengine.cli bot
   ```

   - Esto activará el portal de nuestro ordenador, y listo! Ya tendremos nuestro ordenador registrado como bot y listo para realizar las tareas que subas.
       
###### Si ha llegado hasta este punto, ¡felicidades! Ya ha logrado registrar su ordenador de manera correcta en la aplicación de Botic y está listo para subir las tareas a realizar de manera calendarizada. 
