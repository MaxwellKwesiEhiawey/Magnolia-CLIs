 Happy Coding  👨🏾‍💻👨🏾‍💻👨🏾‍💻😄😀👨🏾‍💻 🤗

# Magnolia-CLIs 

----MAGNOLIA UTILS

Start the Tomcat server.
--------In Command Prompt, change directory to: magnolia-dx-core-demo-6.2.x/apache-tomcat-9.x/bin

--------Run the command: magnolia_control.bat start
Know how to stop the server.
---------In Command Prompt, change back the directory to: magnolia-dx-core-demo-6.2.x/apache-tomcat-9.x/bin

---------Run the command: magnolia_control.bat stop

New Magnolia Project 
---------mgnl jumpstart

Start a project
	cd magnolia
---------mgnl start

New Module
	cd light-modules
---------mgnl create-light-module my-training-module

create a page template
---------mgnl create-page my-homepage
create a component template 
---------mgnl create-component banner -a pages/my-homepage

the three FreeMarker directives that you can use in Magnolia
----[@cms.page /]
----[@cms.area name="areaName" /]
----[@cms.component content=componentNode /]

To create component into a component(eg. Footer)  use @

----------------  mgnl create-component mainFooter  -a pages/my-single@pages  

This creates area (mainfooter) into footer component
