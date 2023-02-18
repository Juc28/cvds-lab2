# cvds-lab2

PATTERNS - FACTORY
# ***HERRAMIENTA MAVEN***
![1](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/logo.jpeg)
## ¿Cuál es su mayor utilidad?
Esta es una herramienta de software que se usa fundamentalemente para la construcción y gestión de proyectos de Java.
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
## ¿Qué es y para qué sirve el repositorio central de maven?
Este tiene una estructura que permite que los archivos tengan versiones distintas, que a través de un mecanismo de denominación bien conocido se descubran los mismos fácilmente. \
Las herramientas de compilación pueden usar estos nombres para extraer dinámicamente las dependencias de la aplicación. En la definición de la aplicación, llamada archivo POM, usando Maven como herramienta de compilación, simplemente nombra las dependencias y el proceso de compilación sabe qué hacer a partir de ahí.
# ***CREAR UN PROYECTO CON MAVEN***
* ¿Cómo se crea un proyecto en Maven con ayuda de arquetipos?
```
mvn archetype:generate -Dfilter=maven-archetype-quickstart 
```
* Esto solicitará:
   - parámetros: Grupo: edu.eci.cvds
   - Id del Artefacto: Patterns
   - Paquete: edu.eci.cvds.patterns
   - archetypeArtifactId: maven-archetype-quickstart

![2](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/arquetipo.png)
![3](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/arquetipo1.png)

* Con tree veremos los archivos creados en mave :
```
tree
```
![4](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/tree.png)

# ***AJUSTAR ALGUNAS CONFIGURACIONES EN EL PROYECTO***

Edite el archivo pom.xml y realize la siguiente actualización:

Hay que cambiar la version delcompilador de Java a la versión 8, para ello, agregue la sección properties antes de la sección de
dependencias: <properties>

![5](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/ajustes.png)

# ***COMPILANDO Y EJECUTANDO***
Objetivo del parámetro "package"-parámetros se podrían enviar al comando mvn.
- Objetivo --> Empaquetar el proyecto que por defecto crea un ejecutable .jar.

Para compilar ejecute el comando:
```
     mvn package
 ```
![6](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/compilar.png)
* cómo ejecutar desde línea de comandos, un proyecto maven y verifique la salida cuando se ejecuta con la clase App.java como parámetro en "mainClass"
 ```
      mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.App"
 ```
* Buscar cómo enviar parámetros al plugin "exec".
 ```
      mvn exec: exec -Dexec.executable = "maven" [-Dexec.workingdir = "/ tmp"] -Dexec.args = "- X myproject: dist"
 ```
* Ejecutar nuevamente la clase desde línea de comandos y verificar la salida: Hello World!
 ![7](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/compilar1.png)
* Ejecutar la clase desde línea de comandos enviando su nombre como parámetro y verificar la salida. Ej: Hello Pepito!
 ![8](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/campiliar2.png)
* Verifique cómo enviar los parámetros de forma "compuesta" para que elsaludo se realice con nombre y apellido.
 ![9](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/compilar3.png)

# ***ESQUELETO DE LA APLICACIÓN***
Ejecute múltiples vecesla clase ShapeMain, usando el plugin exec de maven con lossiguientes parámetros y verifique la salida en consola para cada una:
* Sin parámetros
![10](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/aplicacion1.png)
* Parámetro: qwerty
![11](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/aplicacion2.png)
* Parámetro: pentagon y  Parámetro : Hexagon
![12](https://github.com/Juc28/cvds-lab2/blob/master/pantallazos/aplicacion3.png)

# ***Gitignore***
Es un archivo .gitignore que  permite escribir extensiones de archivo que no quiero en el repositorio, (Archivos basura), como podriasser la clase .class de algún proyecto.
