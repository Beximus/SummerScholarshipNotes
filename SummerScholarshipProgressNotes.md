
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
	* Today i'm stuck at home for at least a few hours (flat plumbing problems) so the plan is to follow along with the typescript tutorial and then send off the email once im clearer on how to structure a typescript skill. Typescript does appear to be the best way forward here. So yesterday didn't feel super productive however without an API to structure my requests for im still basically running blind. My experiments yesterday however did make me question how necessary typescript will be if this project were to be adapted or developed in the future. The app is not so large scale that it necessarily needs typescript and there is far more documentation on javascript built skills than there is on typescript ones. That being said if i were to create a package for api database get requests so this could be applied for google home or other voice based interfaces then typescript may have an advantage. I will keep working with typescript for now but I will keep js as my backup. I worked from 9:30 till about 6:30 but its a lot harder to work efficiently at home.
      * Sent out emails to Eddy (most on brand eddy non reply ever so not gonna bother asking for input unless absolutely necessary later)
      * Sent Email to flight dec guys - waiting on a reply.
*  ##### 22 Nov
   *  Today im working on building correctly structured packages in typescript and properly hosting the lambda for a demo skill because the ask cli is frustrating to upload with. Ok So I have found some very good tutorials specifically about creating and deploying packages for ask so i have been following those all day. I wil continue following up those tutorials over the weekend because I would like to deploy packages to make the future development of acessible skills easier/ deployment of similar skills easier for anyone who might take on this project or something similar in future.
   *  Write a week summary and clarify intents etc
   *  map out decision tree for skill based on previous one
   *  get a proper working javascript prototype using the basic eventfinda api. 
   *  Work out a better developmment and testing timeline
* ##### 24 Nov
    * I came in to uni for a few hours on sunday to make up time and do some more work on the projec. I basically did some more work building node packages and different methods of building the Alexa skill. I made some progress but still got a bunch of errors. 

### 25/11/19 - 29/11/19
#### Week Two Questions/Concerns:
* What to do about the lack of Arts Access Aotearoa API
* Build a separate skill or develop Ed's Further
* Build with jovo to add google assistant to the scope?
* Potentially expand other event databases if Arts Access isn't an option
* Meet with Gillian
  
* ##### 25 Nov
  * Today the goal is to organize a progress meeting with Gillian and develop a basic alexa skill using Jovo and the Eventfinda API to test its viability. Also look into other event database API's in case the Arts Access Aotearoa one does not eventuate. Jovo looks like a potential option but it depends if expansion beyond the alexa speakers/apps is within the scope of this project. It would also require a fair amount of rewrites to ed's code. I also spent the day trying to debug thelocal package from github in order to deploy it to my aws for testing purposes but it seems that since it was last edited some of the dependencies are broken/not working. Of the initial 19 errors, I have one left that seems to persist and it appears to be to do with the moment-timezone package.

* ##### 26 Nov
  * Today I will debug and hopefully deploy the local to my aws so i can really test it, add other functionalities to it.
  * New EXCITING update! The AAA API now exists and i have a key for it:  ($6$rounds=5000$GMB8PxknLlCqpCjk$Bb5TarwHO4J7wUjZMbuFlTQn8yAqnrFtBN41jgK4Jkf8fGbGQgxAr7lQn.boKQOPLIr0RB2W3aYPoiD9CgF85/), Im putting it in here just in case i manage to lose it somehow) I have already run some test API searches and it works like a dream so now its just a matter of doing the hard work of building a skill.

* ##### 27 Nov
  * So I spent a lot of yesterday trying to fix what I thought was my broken code - turns out the API returns broken json. I talked to steven about it to see if he knew of any JSON linters or such that would be able to parse it properly but unfortunately the format is broken enough that the only solution is for logan to fix the api output from his end or loose a few more days to write regex functions and build a parser. My current plan is to take a few results JSON and format them correctly, then spend the rest of the day building a dummy skill using jovo or alexa that accesses those results to demonstrate to gillian. 
  * Update so after a back and forth and a few false starts the api is supposedly fixed and returning parseable JSON files (but I can't check them e becuase the network is down) Im going to log out of the computer now and try logging back in and see if that solves everything. I need to get my materials ready for gillian this afternoon.
