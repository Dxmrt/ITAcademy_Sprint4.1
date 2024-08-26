NIVELL 2

Aquest exercici és un primer contacte amb Spring Boot i Gradle com a gestor de dependències. El projecte genera una API REST simple amb dues rutes que responen a peticions GET. Creació del Projecte

Per començar, accedeix a la pàgina Spring Initializr i genera un projecte Spring Boot amb les següents característiques:

Tipus de Projecte: Gradle
Llenguatge: Java
Versió de Spring Boot: La darrera versió estable

Metadades del Projecte

Group: cat.itacademy.s04.t01.n02
Artifact: S04T01N02
Nom: S04T01N02
Descripció: S04T01N02
Package Name: cat.itacademy.s04.t01.n02
Packaging: Jar
Versió de Java: Mínim versió 11

Dependències Incloses

Spring Boot DevTools
Spring Web

Importació a l'IDE

Després de generar el projecte, importa'l a Eclipse amb l'opció: File > Import > Existing Gradle Project. Configuració

Edita l'arxiu application.properties i configura la variable server.port amb el valor 9001. Creació del Controller

Dins del package principal, crea un subpackage anomenat controller. En aquest subpackage, afegeix una classe anomenada HelloWorldController amb dos mètodes:

String saluda: Aquest mètode respondrà a una petició GET i haurà de ser configurat per a rebre el paràmetre nom com un RequestParam. Si no es proporciona cap nom, es retornarà "Hola, UNKNOWN. Estàs executant un projecte Gradle". Respondrà a les següents URL:
    http://localhost:9001/HelloWorld
    http://localhost:9001/HelloWorld?nom=El meu nom

String saluda2: Aquest mètode també respondrà a una petició GET, però el paràmetre nom serà una PathVariable opcional. Respondrà a les següents URL:
    http://localhost:9001/HelloWorld2
    http://localhost:9001/HelloWorld2/el meu nom

