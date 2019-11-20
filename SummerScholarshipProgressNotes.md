
# Alexa Summer Scholarship Progress notes.

## Start Project to do list/notes 18/11/19:

* Amazon Access
* Github Repo fork n' stuff
* Email Eddeee about Access to Eventfinda API
* Get Timesheet from Office (Gonna do it here for now
* Come up with questions for access Aotearoa on Wednesday


## Current Timeline:

1. Meet Gillian 18/11
2. Get together list of questions and development points for the project.
3. Meet with Access Aotearoa 20/11

## Weekly Updates:
### 18/11/19 - 22/1/11/19
#### Week One Questions/Concerns:
* Need access to amazon things.
* Eventfinda api things
* Develop custom backend lambda thing (find out correct terminology) integrate with a stable external api && cross compare with edee's version
* ##### 18 Nov
	* Met with Gillian, clarified the scope of the project and got the necessary logins to gain access to amazon developer things etc. Sorting out mac location with administrator access so I can install my preferred development environments etc. Started building a Hello World to get familliar with the alexa development environment. Finished a basic hello world and started on a more complex one involving outisde (non lambda) post requests. Today worked from 11am-530pm will move all of this to timesheets as soon as i get the chance . Tomorrows immediate to do lists are:
		* Email Eddee
		* Get Computer Admin Access to install vs code or something similar.
		* Compile List of questions for Access people
		* make second skill that gets jokes from the chuck norris REST api (easy and pretty dang reliable) but could use animal facts or something equally stupid and simple

* ##### 19 Nov
	* Forgot to save my notes from yesterday -_- but in order i followed along with a basic tutorial to execute HTTP Get requests to an external api in an alexa skill. I followed along a tutorial using a chuck norris jokes API. I then applied the same logic to the TronaldDump API to get alexa to tell random donald trump jokes. I then spent some time trying to upgrade that to sort quotes into lists I worked from 10am to 6:30pm
  
*  ##### 20 Nov
    * Folllowing yesterdays tests made me realize why eddy decided to use typescript (i love the dude but would it have killed him to write a proper readme) - i guess following the breadcrumbs forced me to really explore the code and the relevant ts parts are somewhat commented. I also started compiling a list of questions for AAA as well as a list of modules/packages/plugins that i will be using for this project. 
    	* ASK-CLI self explanitory really - required to make the entire operaton work
    	* jest for debug
    	* yarn for package management
    	* typescript (project will be written in typescript because it makes organizing logic easier)
    	* visual studio code because the integrated debug and terminal windows make the workflow nice and easy
    	* typings because it makes organizing the types easier
   	* List for AAA in a separate File
	* After the meeting with arts access aotearoa and the flightdec head we found out that they do not currently have an api but rather that they will have to build one in order for the alexa skill to make GET requests and search the relevant index. Because of this I need to write a concise email explaining what the alexa skill will do and how I would ideally like the get request to work. I need to write all of this out in an email by tomorrow morning. The basic paramaters that i need to search by are:
		* Location
		* Venue
		* Time/Date
		* Accessibility
		* paid/free
		* Category (type of event)
	* these search terms are based on the information/keywords used by the AAA events search webpage. Tomorrows workflow includes writing an email to the flightdec guys. Getting an OTP from gillian and trying to change the phone number for the uni alexa account once and for all. Building a skill that searches apis like the eventfinda one throug ask-cli, typescript etc (follow along tutorials)
* ##### 21 Nov
	* Today i'm stuck at home for at least a few hours (flat plumbing problems) so the plan is to follow along with the typescript tutorial and then send off the email once im clearer on how to structure a typescript skill. Typescript does appear to be the best way forward here.