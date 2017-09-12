# Popularidad-canaima

Paquete Popularity-Contest basado en la version 1.56 y 1.61 de Debian para Canaima Gnu/Linux.

 En la carpeta "paquete", contiene todo los scripts necesarios para que el popularity-contest se ejecute en las computadoras, proximamente llevara la estructura de un paquete. Dicha carpeta posee los siguientes scripts y/o archivos de configuracion:

	*  etc/popularity-contest.conf: archivo de configuracion del paquete, necesarios para la ejecucion del cron-daily. 

	* usr/sbin/popcon-largest-unused: Filtra los paquetes menos usados en el informe que generado por el script de popcon.

    * usr/sbin/popularity-contest: Script que genera un informe con informacion proporcionada por la computadora, dicha informacion son los paquetes instalados y tiempo de acceso a los archivos de estos paquetes.

    * usr/share/poppularity-contest/popcon-upload: Script que maneja el envio del informe del popcon, puede ser comprimido. El informe es enviado por via HTTP o por correo al servidor.

    * usr/share/poppularity-contest/debian-popcon.gpg: llave publica para encriptar el informe.

    * usr/share/popularity-contest/default.conf: archivo de configuracion con variables por defecto.

    * /var/log/popularity-contest: informe generado por el cron-daily.

En la carpeta "servidor", se encuentra todo los script necesarios para levantar el servidor del popularity-contest, asi como la pagina web. 

	* Mail/surgey: por definir...
	
	* bin/gensections.pl: por definir...

	* bin/popanal.py: Es llamado por el script popcon-process.sh para generar 2 archivos "results" y results.stable".

	* bin/popcon-process.sh: Llama para ejecutar a prepop.pl, popanal.py, popcon-stat.pl y popcon.pl. 

	* bin/popcon-stat.pl: Genere las imagenes para la pagina web, con informacion subministrada.

	* bin/popcon.pl: Utiliza todo los documentos generados por los scripts anteriores para montarlos y contruye la pagina web.

	* bin/prepop.pl: Recibe el informe enviado por el popcon-upload para guardarlo y ser procesado por el popcon-process.sh.

	* logs/: carpeta que se guardaran los registros de eventos en la parte servidor. 

	* mirrors/: por definir...

	* popcon-mail/: carpeta que almacena los informes, resultados generados , etc.

	* popcon-stat/: carpeta que almacena las imagenes generanas por popcon-stat.pl.

	* popcon-web/: carpeta que almacena la pagina web y sus contenidos estaticos.

	* var/www/cgi-bin/popcon.cgi: Servidor que gestiona las peticiones HTTP de popcon-upload para ser pasado al prepop.pl y las peticiones por correo por sendmail.






