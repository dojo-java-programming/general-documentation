# Dojo Java Programming - Setting up Eclipse, Maven and Git Part 1 - Notes


__INFO:__ These are some quick notes taken during the 1st session. It is more of a reminder, for 
those who where there. And given them guidance, in case they like to lookup things, repeat them.
It is not meant as a guided tour of what is all done during the session.


## Java

Check if Java JDK is already installed:

	C:\Program Files\Java
	C:\Program Files (x86)\Java

Wat is de default Java versie?

	java -version

Indien Java 7 en of Java 8 niet zijn geinstalleerd, installeer dan de ontbrekende versie(s).


## Eclipse

Maak een directory aan `C:\Apps`

Pak de Eclipse archive uit in: `C:\Apps`

Maak `D:\java\` of indien niet mogelijk `C:\java\` aan

Open Eclipse en gef de volgende wrokspace op: `D:\java\eclipse-4.5-ws\dojo-java-ws`


## Aanmaken Eclipse Project

Eclipse project name `hello-world`

Verwijder `src`

Maak de directories aan: `src/main/java`

Voeg `src/main/java` als source directory.

Create New Class 
package:  `org.organisation.dojo.java.helloworld`
name:  `HelloApp`

Maak method main aan, gebruik de Eclipse template `main`

Gebruik de Eclipse template sysout

Voeg de text `Hello World!` toe aan de system out.


De class zou er nu als volgd uit moeten zien

	package org.organisation.dojo.java.helloworld;

	public class HelloApp {

		public static void main(String[] args) {
			System.out.println("Hello World!");
		}

	}

## Eclipse Refactor

Maak variable aan `user`
Gebruik de variable `user`, ipv woord `World`

Check of je een persoonlijke begroeting krijgt

Markeer de tekst `"Hello " + user + "!"`

Gebruik Eclipse _Refactor -> Extract Method..._ om het samenstellen van het bericht als een apparte method te laten plaats vinden.


De class zou er nu als volgd uit moeten zien

	package org.organisation.dojo.java.helloworld;

	public class HelloApp {

		public static void main(String[] args) {
			String user = "Mario"; // Update in case your name is not Mario
			System.out.println(getMessage(user));
		}

		private static String getMessage(String user) {
			return "Hello " + user + "!";
		}

	}


## Eclipse Configure Maven

__INFO:__ Alleen binnen de organisatie nodig, niet voor thuis situatie.

Maak directory aan `$home\.m2`

Copieer de Maven configuratie `settings.xml` naar  `$home\.m2\settnigs.xml`

In mijn geval is dit `C:\Users\<user-id>\.m2`

Hierin staat oa waar de centrale Maven repository van de organisatie te vinden is.



## Eclipse Configure Maven Project

Eclipse view Package Explorer RMB menu: _Configure > Convert to Maven Project_

__WARNING__ 

- De 2 volgende waardes altijd in lower case.
- group-id, alleen lower-case, puntjes en eventueel streepjes (te vergelijken met Java package names)
- artifact-id, alleen lower-case en streepjes (te vergelijken met Java class name)

Voor nu gebruik deze waardes:

groupd-id: `org.organisation.dojo.java.hello-world`

artifact-id: `hello-world`

## Maven Package

Via Eclipse project RMB menu: _Run As... > Maven build_

Dit zal de java sources file compileren

Via Eclipse project RMB menu: _Run As... > Maven test_

Dit zal de java sources file compileren en de unit tests uitvoeren (echter unit testen, zijn nu nog niet in dit project aanwezig)


Via Eclipse project RMB menu: _Run As... > Maven build..._

Creates a new Maven build.
Update name: `hello-world - package`
Fill in Goal: `package`

Use button _Run_ to execute this new Maven build job.

This will compile the source, run unit tests and create the projects jar file.

Refresh the project in view _Package Explorer_

There should now be a `target` directory with some content.


## Test Executable Jar

Open een shell (command terminal) en ga naar de project directory `D:\java\eclipse-4.5-ws\dojo-java-ws\hello-world`

	D:
	cd \java\eclipse-4.5-ws\dojo-java-ws\hello-world

Ga naar de `target` directory binnen het project.
En kijk of de jar gestart kan worden.
	
	cd target
	java -jar hello-world-0.0.1-SNAPSHOT.jar

Each Java jar file, is actually a zip file, with a different extension.

Open the project jar file and look at the content.

Go into the directory `META-INF`

Open the file `MANIFEST.MF`

Search on internet (google) who to make jar executable

What is said about it?


## Update Maven Project Configuration

Search on internet for the `maven-jar-plugin`

In the left menu, is an link _Creating an Executable JAR File_

Look for how to set the `<mainClass>fully.qualified.MainClass</mainClass>` configuration

In Eclipse open the Maven Project file `pom.xml`

Add the `maven-jar-plugin` to the `pom.xml`, with the required configuration.

Now update the project jar, by invoking again the Maven jon `hellow-world - package`

Test again if the jar is now executable!

	java -jar hello-world-0.0.1-SNAPSHOT.jar
	Hello Mario!
