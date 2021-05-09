¿Qué es powershell?

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
