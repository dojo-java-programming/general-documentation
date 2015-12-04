# Dojo Java Programming - Setting up Eclipse, Maven and Git Part 2 - Notes


__INFO:__ These are some quick notes taken during the 1st session. It is more of a reminder, for 
those who where there. And given them guidance, in case they like to lookup things, repeat them.
It is not meant as a guided tour of what is all done during the session.


## Remove Project from Eclipse



## Move project from eclipse-ws to $home/git

Create an git directroy, here all git repositories will be placed.

	mkdir D:\git
	
__INFO__ In case you have no `D:` drive, use `C:`

	mkdir C:\git

Copy the Java project `hello-world` from `D:\java\eclipse-4.5-ws\dojo-java-ws` to `D:\git`

	copy  D:\java\eclipse-4.5-ws\dojo-java-ws\hello-world  D:\git


## Set Eclipse default git directory

Use Eclipse menu: _Windows > Preferences_

The dialog _Preferences_ is now open

From teh tree select _Team > Git_

Update _Default repository folder_ to `D:\git` (or `C:\git` in case you have no `D:` drive.) 


## Open in Eclipse project from it's new location



## Create git Repository

Add account details

## Add git ignore files



## Add content to git



## Modify HelloApp use StringBuilder DateFormat



## Use compare



## Add changes to git



## Show git history



## Create BitBucket account



## Create BitBucket project



## Connect remote repository



## Push commits



## Check if files are in BitBucket



## Remove local project



## Clone project from BitBucket



## Maven verify



## Run jar





	TIP: Eclipse overview short cuts  Ctrl - Shift - L
	
	
	Update Eclipse Preferences
	
	xxxx
	
	import org.slf4j.Logger;
	import org.slf4j.LoggerFactory;
	
		private static Logger logger = LoggerFactory.getLogger(HelloApp.class);
	
	
			logger.info("inside getMessage(" + user + ")");
	
	
			
			
	launch Eclipse menu Windows Preferences
	Run/Debug > Launching
	Launch Operations
	lways
	
	
	Bitbucket Personal Account
	
	
	
	http://ontgrnap780.ota.duo.nl/download/net.sourceforge.cntlm/cntlm-0.92.3-setup.exe
	
	General > Network Connections
	
	Active Provider: __Manual__
	
	Enable HTTP; HTTPS; SOCKS
	  localhost  3128
	  
	  
	Restart Eclipse



### Chat messges

	16:39Verhagen, TjeerdWelkom
	
	
	16:39Vries, Marten deik kom eraan
	
	
	16:41Bosma, AlexanderGraag 1,50 overmaken op NL43 ABNA 0561 9917 90 of contant.
	
	
	16:57Verhagen, Tjeerdmkdir D:\git
	
	
	17:17Berg, Gerben van den# Maven configuration
	
	target/
	
	
	# Eclipse configuration
	
	.settings/
	
	.classpath
	
	.project
	
	filename: .gitignore
	
	
	17:36Verhagen, Tjeerd<dependencies>
	
	<dependency>
	
	<groupId>org.slf4j</groupId>
	
	<artifactId>slf4j-api</artifactId>
	
	<version>1.7.13</version>
	
	</dependency>
	
	</dependencies>
	
	
	
	17:37Bosma, Alexandervoor Willem
	<dependencies>
	
	<dependency>
	
	<groupId>org.slf4j</groupId>
	
	<artifactId>slf4j-api</artifactId>
	
	<version>1.7.13</version>
	
	</dependency>
	
	</dependencies>
	
	
	
	17:46Verhagen, Tjeerdimport org.slf4j.Logger;
	import org.slf4j.LoggerFactory;
	
	 private static Logger logger = LoggerFactory.getLogger(HelloApp.class);
	
	
	  logger.info("inside getMessage(" + user + ")");
	
	
	
	17:53Verhagen, TjeerdTIP: Eclipse overview short cuts  Ctrl - Shift - L
	<dependency>
	
	<groupId>org.slf4j</groupId>
	
	<artifactId>slf4j-simple</artifactId>
	
	<version>1.7.13</version>
	
	<scope>runtime</scope>
	
	</dependency>
	
	
	
	18:58Verhagen, Tjeerdhttp://ontgrnap780.ota.duo.nl/download/net.sourceforge.cntlm/
	Locatie C:\Program Files (x86)\Cntlm
	edit cntlm.ini
	Toevoegen
	Username in637ver
	Domain      DUO
	
	PassNTLMv2
	# Use 'cntlm -H' to generate password hash
	PassNTLMv2
	Proxy  172.30.227.151:8080
	NoProxy  localhost, 127.0.0.*, 10.*, 192.168.*, *ota.duo.nl
	
	
	19:07Verhagen, TjeerdGa naar C:\Program Files (x86)\Cntlm
	Tik daar:
	cntlm.exe -H
	cd C:\Program Files (x86)\Cntlm
	
	
	19:18Verhagen, TjeerdGeneral > Network Connections
	
	Active Provider: __Manual__
	
	Enable Manual
	Edit  HTTP   localhost  3128 
	Edit  HTTPS  localhost  3128
	  
