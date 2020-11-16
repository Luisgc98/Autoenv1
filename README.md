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
   
   - Crear el ambiente virtual en botic-autoengine y conexión de nuestro ordenador como bot en la aplicación de Botic.
   
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
        ###### Nota: puede haber errores al usar python3.7, así que usar el comando único "python".
        
       ```bash
           (tu_ambiente_virtual) $ python autoengine.cli configure
       ```
