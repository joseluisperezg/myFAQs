¿Qué es powershell?

Es un entorno de linea de comandos, mejor conocidos como shell. 

Es una evolucion de los entornos de comando tradicionales como, cmd en windows o Bourne Shell en unix, ya que este opera con objetos mas que caracteres. Las salidas de los comandos de los entornos tradicionales siempre retornan un respuesta en formato de texto, mientras que en powershell las salidas representan objetos, potenciando la manipulación de los resultados.

¿como determinar la version de powershell utilizada?

$PSVERSIONTABLE

$PSVERSIONTABLE.PSVERSION

get-host

(get-host).version

¿Como puedo consultar los comandos disponibles? 

get-command gcm

¿como obtener ayuda sobre un comando?

get-help <cmd>
  
man <cmd>  
man -full <cmd>
  
¿como obtener ayuda sobre tópicos de powershell?

man about
  
¿Como determino el tipo que devuelve un comando?

get-date | get-member
get-date | gm

¿como puedo extraer un fichero .zip?

como recordatorio podemos usar gcm archive

expand-Archive -path -destinationPath .

¿como puedo comprimir un fichero en un fichero .zip?

$compress = @{ Path = "C:\Reference\Draftdoc.docx", "C:\Reference\Images*.vsd" 
               CompressionLevel = "Fastest" 
               DestinationPath = "C:\Archives\Draft.Zip" }

Compress-Archive @compress

¿como puedo cambiar la fecha de los ficheros?

dir *.txt | foreach { $_.LastWriteTime = $_.CreationTime = get-date }

¿Como puede obtener el hash de un fichero?

expand-archive -path file.zip

¿como obtener numeros aleatorios?

get-random

¿como hacer string sustitution?

usando el format operator -f

man about_Operators

"<string definition>" -f <values>

"{0:0#} {1:0#}" -f (1..12 | get-random -count 2 | sort)
