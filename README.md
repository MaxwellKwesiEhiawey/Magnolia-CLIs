# Magnolia-CLIs  Happy Coding  👨🏾‍💻👨🏾‍💻👨🏾‍💻😄😀👨🏾‍💻 🤗

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

========================================================================
-------------------------Cors--------------------------------------------
Note: The downladable configurations text file should be converted to a yaml file before uploading.
Kindly ensure to save the configuration as a yaml file before uploading.

================ Sample fetch for pages  ====================================
Test for the cross platform configuration in the browser 
async function getPage(url) {
  try{
    let response = await fetch(url);
      const result =  await response.json();
      console.log(result);
  }catch(err){
    console.error(err);
    // Handle errors here
  }
}

getPage('http://localhost:8080/magnoliaAuthor/.rest/pages');

============================ <Tag> <Tag/>  rendering alongside content ===================================
When fetching pages or components you would realize that Magnolia stores tags with it's contents in the JCR. To avoid rendering the tags to your views:
- add "html-react-parser" package to your project.
- Import the added package.
- Wrap the  tags with it's content with your import.

Sample solution:
import parser from "react-router-parser"
	
const Text = () => <div> {parser(element)} </div>;
