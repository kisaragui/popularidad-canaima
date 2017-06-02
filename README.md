# popularidad-canaima
Paquete de Popularity-Contest de Debian para Canaima 

Los scripts que conforman este paquete son los siguientes:

En la carpeta "cliente":

	* popcon-largest-unused: Filtra los paquetes menos usados en el informe que generado por el script de popcon.

    * popcon-upload: Script que maneja el envio del informe del popcon, puede ser comprimido.

    * popularity-contest: Script que genera un informe con informacion proporcionada por la computadora,
      dicha informacion son los paquetes instalados y tiempo de acceso a los archivos de estos paquetes.

En la carpeta "servidor":
	
	* gensections.pl: por definir ...

	* popanal.py: Es llamado por el script popcon-process.sh para generar 2 archivos "results" y results.stable".

	* popcon-process.sh: Llama para ejecutar a prepop.pl, popanal.py, popcon-stat.pl y popcon.pl. 

	* popcon-stat.pl: Genere las imagenes para la pagina web, con informacion subministrada .....

	* popcon.cgi: Servidor que gestiona las peticiones por popcon-upload para ser pasado a prepop.pl.

	* popcon.pl: Utiliza todo los documentos generados por los scripts anteriores para montarlos y contruye la pagina 
	  web.

	* prepop.pl: por definir ...




