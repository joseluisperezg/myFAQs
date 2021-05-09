¿Qué es powershell?


¿Como puedo consultar los comandos disponibles?
 get-command
 gcm
 
 ¿como puedo extraer un fichero .zip?
 
 como recordatorio podemos usar gcm *archive*
 
 expand-Archive -path <file> -destinationPath .
  
 ¿como puedo comprimir un fichero en un fichero .zip?
 
 $compress = @{
  Path = "C:\Reference\Draftdoc.docx", "C:\Reference\Images\*.vsd"
  CompressionLevel = "Fastest"
  DestinationPath = "C:\Archives\Draft.Zip"
}

Compress-Archive @compress

  
¿como puedo cambiar la fecha de los ficheros?
 
dir *.txt | foreach { $_.LastWriteTime = $_.CreationTime = get-date } 


¿Como puede obtener el hash de un fichero?

expand-archive -path file.zip
