Instalar y ejecutar minishift en windows 10

1.- Seguir los pasos de la web:
	https://docs.okd.io/3.11/minishift/getting-started/setting-up-virtualization-environment.html#for-windows

2.- Lanzar los siguientes comandos en una powershell como administrador:

	$> minishift config set hyperv-virtual-switch "External VM Switch"
	$> minishift config set skip-check-hyperv-driver true

3.- Ejecutar minishift:

	$> minishift start
	
	
Otros comándos útiles

	* Parar minishift:  $> minishift start
	
	* Borrar maquina virtual minishift:  $> minishift delete
	
Pruebas de rendimiento de una web

En ubuntu instalar las utilidades de apache y ejecutar el comando:

  ab -t 60 -c 50 -k https://facebook.com
  
  60 indica los segundos que va ha estar enviando peticiones
  50 indica el número de accesos simultaneos a dicha web
  
  e
  El comando para instalar las utilidades en ubuntu es el siguiente:
  apt-get install apache2-utils
  
  
Es posible instalar el CLI para interactuar con openshif en esta web

	https://github.com/openshift/origin/releases
	
	- Una vez descargado descromprimir y copiar en una ubicación en c: 
	- Yo lo he metido en una carpeta cli dentro de openshift/origin/releases.
	- Despues meterlo en el path de windows para que se pueda acceder al cli desde cualquier ubicación.
	
	
Saber la ruta de minishift	
	
	minishift console --url
	
	
Templates para openshift:

	- MSSQL:
		oc create -f https://raw.githubusercontent.com/gsyjdcg/openshift-templates/036fa9a0f7c06f8a546638a2d83763490e628b5c/mssql2019.json
		
	- OPENJDK11-RHEL7:
		oc create -f https://raw.githubusercontent.com/gsyjdcg/openshift-templates/main/openjdk11-rhel7.yarm