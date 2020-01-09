
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
    * Folllowing yesterdays tests made me realize why eddy decided to use typescript (i love the dude but would it have killed him to write a proper readme) - i guess following the breadcrumbs forced me to really explore the code and the relevant ts parts are somewhat commented. I also started compiling a list of questions for AAA as well as a list of modules/packages/plugins that i will be using for this project. (worked from 10-345)
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
   *  Today im working on building correctly structured packages in typescript and properly hosting the lambda for a demo skill because the ask cli is frustrating to upload with. Ok So I have found some very good tutorials specifically about creating and deploying packages for ask so i have been following those all day. I wil continue following up those tutorials over the weekend because I would like to deploy packages to make the future development of acessible skills easier/ deployment of similar skills easier for anyone who might take on this project or something similar in future. (worked 1130-5)
   *  Write a week summary and clarify intents etc
   *  map out decision tree for skill based on previous one
   *  get a proper working javascript prototype using the basic eventfinda api. 
   *  Work out a better developmment and testing timeline
* ##### 24 Nov
    * I came in to uni for a few hours on sunday to make up time and do some more work on the projec. I basically did some more work building node packages and different methods of building the Alexa skill. I made some progress but still got a bunch of errors. (worked 12-4) Week was 37 hours total

### 25/11/19 - 29/11/19
#### Week Two Questions/Concerns:
* What to do about the lack of Arts Access Aotearoa API
* Build a separate skill or develop Ed's Further
* Build with jovo to add google assistant to the scope?
* Potentially expand other event databases if Arts Access isn't an option
* Meet with Gillian
  
* ##### 25 Nov
  * Today the goal is to organize a progress meeting with Gillian and develop a basic alexa skill using Jovo and the Eventfinda API to test its viability. Also look into other event database API's in case the Arts Access Aotearoa one does not eventuate. Jovo looks like a potential option but it depends if expansion beyond the alexa speakers/apps is within the scope of this project. It would also require a fair amount of rewrites to ed's code. I also spent the day trying to debug thelocal package from github in order to deploy it to my aws for testing purposes but it seems that since it was last edited some of the dependencies are broken/not working. Of the initial 19 errors, I have one left that seems to persist and it appears to be to do with the moment-timezone package. (worked from 1030-530)

* ##### 26 Nov
  * Today I will debug and hopefully deploy the local to my aws so i can really test it, add other functionalities to it.
  * New EXCITING update! The AAA API now exists and i have a key for it:  ($6$rounds=5000$GMB8PxknLlCqpCjk$Bb5TarwHO4J7wUjZMbuFlTQn8yAqnrFtBN41jgK4Jkf8fGbGQgxAr7lQn.boKQOPLIr0RB2W3aYPoiD9CgF85/), Im putting it in here just in case i manage to lose it somehow) I have already run some test API searches and it works like a dream so now its just a matter of doing the hard work of building a skill. (worked from 11-8)

* ##### 27 Nov
  * So I spent a lot of yesterday trying to fix what I thought was my broken code - turns out the API returns broken json. I talked to steven about it to see if he knew of any JSON linters or such that would be able to parse it properly but unfortunately the format is broken enough that the only solution is for logan to fix the api output from his end or loose a few more days to write regex functions and build a parser. My current plan is to take a few results JSON and format them correctly, then spend the rest of the day building a dummy skill using jovo or alexa that accesses those results to demonstrate to gillian. 
  * Update so after a back and forth and a few false starts the api is supposedly fixed and returning parseable JSON files (but I can't check them e becuase the network is down) Im going to log out of the computer now and try logging back in and see if that solves everything. I need to get my materials ready for gillian this afternoon.
  * After playing with the API a bit more i started working more on my mind maps/ docmuentation to give myself a better idea of what im going to build based on todays meeting. (today i worked from 10 till 6)

* ##### 28 Nov
  * Today i built a parser to make sure the results from the AAA api are properly encoded when being called by a skill. If the api doesn't undergo any changes then I will probably end up uploading it to npm for final build and deployment, it is fairly basic, it takes the object returned by the get request to the AAA server, stringifies it, clears up any remaining typos/format issues and then outputs that as a json object. It will also end up importing the get request from the get request constructor that i have yet to build. The other option is to process the entire events library myself but we will see if it comes to that later. Still to do today is try to figure out the error in ed's thelocal code in the momentUtil.ts file. It would appear that the syntax he uses to construct the timeframe (moment package) calls are depreciated. Im going to spend the rest of the afternoon building a basic skill that calls and processes to the api without building the get request separately, just a proof of concept to integrate the returned api information into the alexa speech to text thing. The first search will be for events in dunedin because i know there is currently only a single result, the next search will be to look for Kapiti because that returns fewer results and the final method will return audio described events in kapiti. (worked from 10- 5)

* ##### 29 Nov
  * Still working on the prototype skill because it makes more sense to build something that can be further developed into the final skill. Today I built a scraper module to scrape the missing data from the events (currently still missing address, cost and accessibility). I also finished off the parser module that can verify the data being recieved from the api. (Both of these modules exist only in js right now because there is no point in public deployment until  i know the api and skill are finalised). I need to work on building the skill intent that will construct and execute the search to the database, because it needs to be modular and also needs to save queries. I also further developed the mind map/ documentation i have been using to give myself a better reference for how to structure the skill (will upload those when i write up the week). today was a shorter day and i worked from 1130 - 430 (had to go dentist). week was 36 hours total

### 2/12/19 - 7/12/19
#### Week Three Questions/Concerns:
* Can I get Logan to add the rest of the functionality to the API or will i have  to continue using the scraper modules?
* Can I get a basic skill up and running - scrapping the whole dummy skill idea and going straight into building one that can be developed into a full skill because why waste time/energy I'm going to run into enough roadblocks/technical issues without adding extra steps
* How am I going to generate the speech model/ organize the search mode
* How do I organize/refine the search
* Storing bookmarked events
* tutorial mode (how what where when)
* Do I even bother with typescript if it isn't necessary for this?
  
* ##### 2 Dec
  * I ended up being very busy over the weekend so I think im going to just end up putting in some extra hours during the week this week. Today Im going to start on a serious skill - looking to put in the right intents for future development. Also going to see if i can get the version of the skill that ed built to upload at all - given that i should now have access to the relevant alexa and lambda environments.  Im going to email Logan requesting that he add wheelchair access and potentially contact details to the response body if possible. Also started looking int o best practice for developing tutorials for apps, alexa utterance models, non visual user interfaces etc. (worked from 11 -5)

* ##### 3 Dec
  * Today ended up being very busy. So the first thing I did when I came in was to start what I will be referring to as my Pepe Silvia wall. Basically a wall of post its - this one is for my dev process because it helps me to visualise the different parts of the project that need to be worked on . The UI part at the moment is very small but it will get bigger as the functionality of the skill increases beyond its current basic set up. Green post its are headings, Bright pink  post its are things in the process that are done or require very little development right now, blue post its are for code/tech things, Peach are for comments or intentions, orange is for needs develoment or work now. I deployed a good version of the test skill that can be developed further, had some good communication with Logan about adding to the existing api and started work on the search handler. (worked from 11 to 8)
  * Here is the Wall at the start of the day
  * ![pepe silvia wall image](images/dayOneStart.jpg "wall at the start of the day")
  * Here is the wall at the end of the day
  * ![pepe silvia wall image](images/dayOneEnd.jpg "wall at the end of the day")

* ##### 4 Dec
  * Today worked more on starting up the skill proper. Logan fixed the API (no Json parser necessary now) and added all of the information that he has accesible through the search function to the api. This means that I re worked my plans again but this time they are significantly more concrete. I now have the queries that i can send to the api as well as the terms I can refine by after the intial search (as well as a list of information that can only be retrieved from the individualized event pages). I updated the wall in response to these changes.
  * ![pepe silvia wall image](images/dayTwo.jpg "wall day two")
  * I then spent the rest of the day working on getting the basic first part search done for the skill. I didn't finish but it shouldnt take too long tomorrow. Once i have that sorted i can work on passing information from custom slot responses to the get requests. (today i worked from 11:30 till 7:30)

* ##### 5 Dec
  * Today I just kept working on various scripts to build the skill, specifically one that would get a list of the current categories and locations on listed events to build the model and the other the actual search intent that executes the search request. Also had a meeting with Gillian today and she reminded me to keep notes of the limitations of the api and skill, the major one at the moment is that the only searches executable by the API are; Category, Location, Month, Year, Free, Touch Tour, Touch Talk, Audio Described and Described. The keys that are returned by the reqest are id, name, url, description, type, image(not useful here), category, location, notes, wheelchair access, accessible toilets, mobility parking, start time and stop time. All other data like cost, contact details, organizer and full description are only returned when a node scrape is done of the specific event page. This is annoying but it informs the structure of the skill. Basically I have to structure it so that it requests event information based on a few basic things and then the results can be refined by the rest of the terms. Its really annoying that the api cant return any contact details but this seems to be a limitation of the arts access aotearoa events listings. Tomorrow I need to build further so that I have my basic search function that stores the given result data (as a JSON) and then can parse through and refine results from that using session attributes. This added functionality will also allow users to store specific event information.

* ##### 6 Dec
* Today i ust did more work on the model builder , get reques builder and session attribute handler.

### 9/12/19 - 13/12/19
#### Week Three Questions/Concerns:
* How will i get the session attrributes to store and work properly
  

* ##### 9 Dec
  * Today was more work on the model builder, request builder etc. I wrote a package that writes two lists; on that gets all of the locations of every event listed and the other one that gets the categories of  all of the events listed. this package also contains other modules that wll be usefull for development

* ##### 10 Dec
  * My write ups for the last few days have been pretty sparse, mostly because im still working on the same modules as before. Today I finished the language model builder which is nice because it makes updating and working on the skill a lot easier for now and also in future. I also made some progress on storing the current session attributes however i will have to do more experimentation as to wether or not i can store the entire search request bodyin attributes or if i have to parse it somehow. im thinking dynamo db is my best option. 

* ##### 11 Dec
  * So I know my documentation for the last few days has been brief but it is becuase I have been really in the weeds getting the core scripts for this project to work. Basically I have a model builder script now that i can expand by just building out the dictionary (list of combinations of words and phrases) that generates the utterances. I have built a get request cnnstructor and a way of saving the returned search bodies.

* ##### 12 Dec
  * So I let my documentation for this project get away from me again because i keep getting stuck into writing the code and by the time i am done for the day i cant form full sentences anymore, tell myself that i will write about it in the morning and then for get to do so. Today I built the search request handler and started on the search refine handler, neither is fully functional but both are actively accessing the database.
  
* ##### 13 Dec
  * Alright so today I worked more on the search constructor intent, making sure that every time you call "search events" it wipes the assigned session attributes and re inserts the new one to avoid a bug I was encountering when you searched, refined then listed events and if you tried to execute a different search it could only search from the existing list. The next thing i worked on was making sure all of the possible categories for refinement were available as a part of the search functionality. I also created the read events intent then shortly thereafter changed it so that it would become the list event details intent instead so that it can list the current refined search list names, details, categories, locations or combinations thereof. I also need to add a list possible locations and categories to search by intent. The most pressing one is to create an intent that selects a specific event and then scrapes all of the body text data from the specific event inside of the given timeframe. I also need to create a library script to translate the given dates and times for events into versions that amazon.date.time.month can parse correctly. I also need to create a tutorial skill that can guide the user through the search, refine, list select process. I will do a proper write up on the last two weeks process on monday morning for real. I also need to go bakc and fix a bunch of the scripts because it currently cant get past the pagination for the api results and the memory size and timeout of the lambda function because i already upped them but i dont think it was enough. I need to add dynamo db to this so that i can make the search process run a lot smoother.
  
## Post Break Notes Catch up.

### Week Four: 16/12/19 - 19/12/19

* So in the last four days before break, I got very in the weeds about fixing technical issues and getting the skill running properly and as a result i completely blanked on writing up reports about my progress and decision making over the course of those days so I will now do my best to summarise them. The major hurdle that I kept running into with the skill was the pagination of results from the server and the resulting timeouts from alexa when trying to navigate these issues. In short Alexa has an 8-10 second timeout for all skills requests. This means that if the called intent cannot complete its processes within that time frame she returns an error message by default. After initial research I found that aside from some very sketchy (buggy/unstable) workarounds involving having alexa play an mp3 of  3-4 seconds of silence (which would result in the user not having access to the microphone for that period) There isn't any way around the timeout issue. This meant that I had to shift my focus to "cutting the fat" or ensuring that my api requests and subsequent functions run as quickly as possible. 
    * The first thing I did was start checking how long different types of API calls took and basically what i found was that search functions take significantly longer than basic empty calls (returning the entire list of events) which makes sense, and the subsequent pages of any result always take longer than the first page. Basically the results were: simple call to the api 1 -2 seconds , simple call to the second page of the api 3-4 seconds, simple call for an event search 2 -4 seconds, simple call for second page of an event search 3-4 seconds. These times also appeared erratic.
    * The varying response times for the api meant that the first thing i started to look at were ways to speed up/ensure that my api calls were executing as fast as possible, the second was to make sure that different intents were using the correct type of event call for their function - so a blank or fallback search for all events actually executes a simple api call rather than a search for "" because it executes quicker. It also highlighed the necessity for a get next page intent as there was no way to make the search retrieve and store all pages of results in one go. 
    * The creation of a get next intent also necessitated a second get request script as it would execute the searches including page numbers.
    * It also highlighted the need for a clear all intent to clear the list of searched events should the user wish to start again for whatever reason. 
    * it also highlighted the need for an addition to the original get function to differentiate between a simple call and a specific search. This change also had to be made to the get next function.
  
  #### List of intents/things implemented before the break:
  * Initiate Search intent
  * Refine By intent
  * Read list intent
  * get next intent
  * clear all intent
  * get request script
  * get next script
  * list generator for the model builder
  * model builder
  * session attribute getter/editor
  * Proper help message

### Week five: 6/1/20 -10/1/20

* So in coming back from break I have quite a few things to get ready for user testing next week. My main focus right now is to get all of the technical aspects of the skill running while avoiding timeout errors as much as possible. 
##### The list of things to do this week are as follows:
 * Ensure the Get Next page functions properly without timeouts
 * Run the rest of the skill a few times to find tests and shanghai friends into doing some pre user testing debug/bugfinding , (this is mostly to ensure that the AU language model is the best option) and to find potential syntactical errors
 * Make the Help function run as smoothly as possible
 * Create and run a scraper function correctly
 * add event bookmarking using dynamo DB
 * MAKE A TUTORIAL Function(all caps for importance)
 * Clarify the UX journey / decision making process
 * MOVE SKILL TO VUW ALEXA DEVELOPER ACCOUNT, AWS LAMBDA AND DB AS WELL AS TESTING ON THE ACUTAL ALEXA (which i have been avoiding because loading and testing the skill onto the real alexa takes ages and feels like screeching into the abyss while debugging)

##### January 6
* Today I spent the day refamiliarisng myself with the project (coming back from the break gave me a sort of fresh eyes perspective to the technical issues) I spent some of the break thinking about the technical issuse  and protential UI/UX solutions to the technical limitations and i think the best option is to essentially talk the user through it. So most of today was just going through my game plan, establishing what the welcome message should actually say to the user, and solidifying my idea that alexas responses should be as concise as possible while still elaborating user options. I want to make sure that when the user says "help me" etc that they are prompted with a reminder of all the different intents available to them such as clear all, search and get next, refine by, read list. When time allows i would also like the help function to suggest to users what to do based on the intent they had accesed prior to asking for help but it is pretty low on the priority list right now. I shortened my Get requests to as few lines as possible because while using class constructors felt nice and smort, the plain requests executed faster and at the moment quick execution of functions is the highest priorty. I also spent time over the break thinking about the best way to construct a tutorial function for the user, and i think the best way is to construct a guided search for the user that refines by another searchable term and then reads the name, location and category of the first requested event. I also would like to add an intent that lists things you can search by (Free, Touch Tour, Audio Described, list of Locations, list of categories), as well as a list of things that the search can be refined by (list of locations, list of categories, wheelchair access, accessible toilets, mobility parking) and the list of things that can unfortunately only be accessed by listening to the full event description. I think that the best way to go about delivering this skill is to be upfront with the users about the limitations ("at this time these particular data points can only be found in full event descriptions when provided").

##### January 7 
* Todays first task was to make sure I write up as much of the process as I can remember from the days i missed as well as get down some of the thoughts i had over the break that coalesced properly yesterday. The next task is to ensure both get functions run smoothly and begin adding a scraper function to look at specific events.
* I am now including a photo of the sticky wall - this is the form it was in when I left for break and by the end of today it should hopefully look very different. 
* ![breakwall image](images/breakWall.jpg "The Pepe Silvia Wall in all of its glory before break")

##### January 8
* Although i have not/cannot resolve the current timeout/datasize issue that i have been facing with the skill i decided to pivot  my focus in order to come back fresh. I spent today looking at Dynamo DB in order to implement bookmarking and storage of events for users as well as to use a separate dynamo db table as a workaround/fall back should users want to search the entire database. structuring the database builder correctly took a while but i have included a database builder script in the model builder function.

##### January 9 
* today i did more work implementing the dynamodb systems and testing write to databases from within the skill itself. One of the biggest issues i have is that the alexa skill can not store more tha 24 events worth of data in the session attributes area at any one time (nor should she). What this means though is that once the database expands beyond only having 30 ish events listed the skill will no longer work properly even if the users search for specific terms. This means that for now although im focusing on getting the entire skill to work from session attributes, I would like to ensure i can move the majority of the skill to DynamoDB so it is less influenced by data size. Because 24 KB is a small amount of data to be working with. And although dynamoDB write limit is approximately 25 MB the pagination means that the biggest size a results page can be is about 15 KB and the max size of a Dynamo Table is SIGNIFICANTLY larger than that. This afternoon I will focus on re writing the skill to prompt the user to search by a specific term and leave it open to fix with dynamo later. I will integrate the data scraper by the end of today and hopefully will have the user able to bookmark specific events by the end of tomorrow.


