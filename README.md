# cvds-lab2
PATTERNS - FACTORY
# ***HERRAMIENTA MAVEN***
# (imagen1)
## Cuál es su mayor utilidad
Esta es una herramienta de software que se usa fundamentalemnte para la construcción y gestión de proyectos de Java.
Maven utiliza un Project Object Model tambié conodiso como POM, esto para poder describir el proyecto a construir, componentes externos, el orden de construcción de elementos y sus dependencias de otros módulos. 
Es de anotar quie presenta una ventaja al tener conectividad remota a su propio repositorio dando acceso a utilidades adicionales.
## Fases de Maeven
1. ***Validate***: Valida que el proyecto sea correcto, que tenga la información necesaria sea accesible.
2. ***Compile***: Compila codigo guente del proyecto.
3. ***Test***: Prueba el código compilado, mediante pruebas unitarias.
4. ***Package***: Empaqueta en un formato distribuible el código compilado.
5. ***Verify***: Ejecuta pruebas de integración, ver que cumplen los criterios de calidad.
6. ***Install***: En el paquete del repositorio local instala, para que se pueda  usar en otros proyecto.
7. ***Deploy***: Copia el paquete finak a un repositorio remoto para compartirlo con otros desarrolladores.
## Ciclo de vida de la construcción
- Default --> Gestiona construcción y despliegue del proyecto.
- Clean --> Gestiona la limpieza del directorio.
- Site --> Gestiona la creación de la documentación.
## Para qué sirven los plugins
El plugien es un componente de codigo que esta hecho con el fin ampliar las funciones de una herramienta. En si tiene como proposito aportar funciones adicionales a programas informáticos.
## Qué es y para qué sirve el repositorio central de maven 
Este tiene una estructura  que permite que los archivos tengan versiones distintas, que a traves de un mecanismo de denominación bien conocido se descubran los mismos facilmente. \
Las herramientas de compilación pueden usar estos nombres para extraer dinámicamente las dependencias de la aplicación. En la definición de la aplicación, llamada archivo POM, usando Maven como herramienta de compilación, simplemente nombra las dependencias y el proceso de compilación sabe qué hacer a partir de ahí.
# ***CREAR UN PROYECTO CON MAVEN***
## Cómo se crea un proyecto en Maven con ayuda de arquetipos
```
mvn archetype:generate -Dfilter=maven-archetype-quickstart 
```
Esto solicitará:

- Grupo
- Id del artefacto
- Versión
- Paquete
# ***AJUSTAR ALGUNAS CONFIGURACIONES ENEL PROYECTO***
# ***COMPILANDO Y EJECUTANDO***
## Objetivo del parámetro "package"-parámetros se podrían enviar al comando mvn.
- Objetivo --> Empaquetar el proyecto que por defecto crea un ejecutable .jar.
## cómo ejecutar desde línea de comandos, un proyecto maven y verifique la salida cuando se ejecuta con la clase App.java como parámetro en "mainClass"
 ```
      mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.App"
 ```
 ##  Enviar parámetros al plugin "exec"
 ```
      mvn exec: exec -Dexec.executable = "maven" [-Dexec.workingdir = "/ tmp"] -Dexec.args = "- X myproject: dist"
 ```
## Buscar cómo enviar parámetros al plugin "exec".
## Ejecutar nuevamente la clase desde línea de comandos y verificar la salida: Hello World!
## Ejecutar la clase desde línea de comandos enviando su nombre como parámetro y verificar la salida. Ej: Hello Pepito!
## Ejecutar la clase con su nombre y apellido como parámetro.¿Qué sucedió?
## Verifique cómo enviar los parámetros de forma "compuesta" para que elsaludo se realice con nombre y apellido.

# ***ESQUELETO DE LA APLICACIÓN***
## ¿Cuál(es) de las anteriores instrucciones se ejecutan y funcionan correctamente y por qué?
# ***Gitinore***
Es un archivo .gitignore que  permite escribir extensiones de archivo que no quiero en el repositorio, (Archivos basura), como podriasser la clase .class de algún proyecto.
