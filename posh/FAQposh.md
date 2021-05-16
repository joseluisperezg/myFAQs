![](https://docs.microsoft.com/en-us/powershell/media/index/ps_black_128.svg)
# powershell 

1. [¿Qué es powershell?](#qué-es-powershell)
2. [¿Cómo determinar la versión de powershell utilizada?](#cómo-determinar-la-versión-de-powershell-utilizada)
3. [¿Cómo puedo consultar los comandos disponibles?](#cómo-puedo-consultar-los-comandos-disponibles)
4. [¿Cómo obtener ayuda sobre un comando?](#cómo-obtener-ayuda-sobre-un-comando)
5. [¿Cómo obtener ayuda sobre tópicos de powershell?](#cómo-obtener-ayuda-sobre-tópicos-de-powershell)
6. [¿Cómo determino el tipo que devuelve un comando?](#cómo-determino-el-tipo-que-devuelve-un-comando)
7. [¿Cómo puedo extraer un fichero .zip?](#cómo-puedo-extraer-un-fichero-zip)
8. [¿Cómo puedo comprimir un fichero en un fichero .zip?](#cómo-puedo-comprimir-un-fichero-en-un-fichero-zip)
9. [¿Cómo puedo cambiar la fecha de los ficheros?](#cómo-puedo-cambiar-la-fecha-de-los-ficheros)
10. [¿Cómo puedo obtener el hash de un fichero?](#cómo-puedo-obtener-el-hash-de-un-fichero)
11. [¿Cómo obtener números aleatorios?](#cómo-obtener-números-aleatorios)
12. [¿Cómo hacer "String Sustitution"?](#cómo-hacer-"String-Sustitution")




## ¿Qué es powershell?
Es un entorno de línea de comandos, mejor conocidos como shell. 

Es una evolución de los entornos de comando tradicionales como, cmd en windows o Bourne Shell en unix, ya que este opera con objetos más que secuencias de caracteres. Las salidas de los comandos de los entornos tradicionales siempre retornan un respuesta en formato de texto, mientras que en powershell las salidas representan objetos, potenciando la manipulación de los resultados.

## ¿Cómo determinar la versión de powershell utilizada?

```powershell
$PSVERSIONTABLE
```
```powershell
$PSVERSIONTABLE.PSVERSION
```
```powershell
get-host
```
```powershell
(get-host).version

```

## ¿Cómo puedo consultar los comandos disponibles? 

```powershell
get-command gcm
```

## ¿Cómo obtener ayuda sobre un comando?

```powershell
get-help <cmd>
  
man <cmd>  
man -full <cmd>
```

## ¿Cómo obtener ayuda sobre tópicos de powershell?
```powershell
man about
```  
## ¿Cómo determino el tipo que devuelve un comando?
```powershell
get-date | get-member
get-date | gm
```
## ¿Cómo puedo extraer un fichero .zip?

como recordatorio podemos usar gcm archive
```powershell
expand-Archive -path -destinationPath .
```

## ¿Cómo puedo comprimir un fichero en un fichero .zip?
```powershell
$compress = @{ Path = "C:\Reference\Draftdoc.docx", "C:\Reference\Images*.vsd" 
               CompressionLevel = "Fastest" 
               DestinationPath = "C:\Archives\Draft.Zip" }

Compress-Archive @compress
```
## ¿Cómo puedo cambiar la fecha de los ficheros?
```powershell
dir *.txt | foreach { $_.LastWriteTime = $_.CreationTime = get-date }
```
## ¿Cómo puedo obtener el hash de un fichero?
```powershell
expand-archive -path file.zip
```
## ¿Cómo obtener números aleatorios?
```powershell
get-random
```
## ¿Cómo hacer "String Sustitution"?

usando el format operator -f

```powershell
man about_Operators

"<string definition>" -f <values>

"{0:0#} {1:0#}" -f (1..12 | get-random -count 2 | sort)
```
