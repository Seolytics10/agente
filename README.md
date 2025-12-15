# agente
Agente OSSEC HIDS para que funcione en la computadora

Paso 1: actualiza tu sistema Ubuntu
Antes de realizar cualquier instalación, asegúrese de que su sistema esté actualizado.

sudo apt update -y
sudo apt upgrade -y

Paso 2: Instalar el agente en Ubuntu
Ahora configuremos el agente en un PC diferente y agreguémoslo al servidor Seolytics.

Paso 3.2: Instale el agente.
tar xvf $VERSION.tar.gz
Navegue a la carpeta generada al descomprimir y ejecute el script de instalación.

cd ossec-agent-${VERSION}
sudo sh install.sh
(en/br/cn/de/el/es/fr/hu/it/jp/nl/pl/ru/sr/tr) [en]: es // Establece tu idioma preferido
You are about to start the installation process of the OSSEC HIDS.
You must have a C compiler pre-installed in your system.

  - System: Linux tinc 5.4.0-29-generic
  - User: root
  - Host: tinc

  -- Press ENTER to continue or Ctrl-C to abort. --

1- What kind of installation do you want (server, agent, local, hybrid or help)? agent // Seleccione el tipo de instalación como agente.

2- Setting up the installation environment. // Deje el entorno de instalación como predeterminado.

 - Choose where to install the OSSEC HIDS [/var/ossec]: PRESS ENTER

    - Installation will be made at  /var/ossec .

Add OSSEC server to connect to

3- Configuring the OSSEC HIDS.

  3.1- What's the IP Address or hostname of the OSSEC HIDS server?: 172.12.24.10

   - Adding Server IP 172.12.24.10

Run integrity daemon. 

 3.2- Do you want to run the integrity check daemon? (y/n) [y]: y

   - Running syscheck (integrity check daemon).

Enable rootkit detection engine. 
3.3- Do you want to run the rootkit detection engine? (y/n) [y]: y

   - Running rootcheck (rootkit detection).

Disable active responses. 
  3.4 - Do you want to enable active response? (y/n) [y]: n

   - Active response disabled.


You will be lead to screen of this kind. 

 3.5- Setting the configuration to analyze the following logs:
    -- /var/log/auth.log
    -- /var/log/syslog
    -- /var/log/dpkg.log
    -- /var/log/nginx/access.log (apache log)
    -- /var/log/nginx/error.log (apache log)

 - If you want to monitor any other file, just change
   the ossec.conf and add a new localfile entry.
   Any questions about the configuration can be answered
   by visiting us online at http://www.ossec.net .


   --- Press ENTER to continue ---

 - System is Debian (Ubuntu or derivative).
 - Init script modified to start OSSEC HIDS during boot.

 - Configuration finished properly.

 - To start OSSEC HIDS:
      /var/ossec/bin/ossec-control start

 - To stop OSSEC HIDS:
      /var/ossec/bin/ossec-control stop

 - The configuration can be viewed or modified at /var/ossec/etc/ossec.conf

    Thanks for using the OSSEC HIDS.
    If you have any question, suggestion or if you find any bug,
    contact us at https://github.com/ossec/ossec-hids or using
    our public maillist at
    https://groups.google.com/forum/#!forum/ossec-list

    More information can be found at http://www.ossec.net

    ---  Press ENTER to finish (maybe more information below). ---

NOTA: Una vez que finalice la instalacion, deberá solicitar a Seolytics la creacion de una clave y el alta del cp en el servidor de la nube para instalar en el agente, sin estos pasos el agente no funcionara correctamente.
