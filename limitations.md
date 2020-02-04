# List of Limitations encountered while building an alexa skill
So like most summer research projects (i'm assuming) this particular endevour involved a fairly steep learning curve initially. Because, although when signing up for this project i had experience with javascript, nodeJS, RESTful APIs databases etc. I had very little experience with AWS (amazon web services). Initially the limitations I was encountering were fairly straight forward, setting up the development computer and workflow, looking at other skills and how best to structure them around databases and different API's and how best to translate Ed's work from last year into this project. 
* Something that isn't exactly a technical limitation but nonetheless frustrating was the way in which AWS documents the functionality of its services (Alexa Skills kit command line interface, Alexa requirements, skill requirements, lambda permissions, dynamo DB permissions) All of these things have separate web pages and at times it felt like looking for a needle in a haystack when looking for an answer to a question. Although there is plenty of information provided by lord bezos and his underlings about their resources it is really poorly organized. To the point at which for some things the cynical part of my brain wonders if it was done on purpose to encourage people to take their pricey courses or online qualifications. The most helpful resource I found was not actually the direct documentation but rather their github hosted skills cookbook that has direct examples as well as how to set them up. 
## The main reason I went on the above rant was for a few hard limits that exist for alexa that i ended up encountering at different points in development because they dont really have a compiled list of limits or things not to do.
### 1. Alexa has a working memory of 24 KB
* *(this is not mentioned in the session attributes section or anywhere else where it would be directly relevant to impeding performance but instead is only mentioned briefly in DYNAMO DB documentation [i found this out from stack overflow beacuse other people encountered similar issues with very little documentation])*
* #### What this actually means is that for the purposes of this project alexa can hold a maximum of 24 events in her working memory at any one time - this is a problem for API reasons that I will get to later. 
### 2. Skill Names cannot have connecting words such as the, a, and, but etc. They also must be at least two words.
* *Not a big problem, just annoying*
### 3. Skills must have a version of the model for the locale where the back end is hosted not just the intended use locale 
* The back end of the skill is hosted on the east coast of the US (because default settings), this means the skill requires both AU and US models. On top of this since I started work on this project they expanded the special slot type lists for AU to include city names. BUT she still can't really deal with ***Māori*** pronunciations so someone searching for Tauranga, Rotorua (depending on pronunciation) still struggles not to get errors
### 4. Alexa can't pronounce non locale language words without correct phonemes this means there is no real practicable way to ensure her pronounciation is correct
* phonemes arent completely standardised across locales so AU has diffferent accepted letters to US
### 5. Responses time out after 8 seconds
* This means all skill requests, back end processing etc has to be completed in 8 seconds or less which created some problems with paginated API requests
### 6. Alexa has to have finished her response inside of 90 seconds 
* This isn't likely to be a huge issue but it could cause bugs if any of the full descriptions of events are very very loooong
  

## The next part in what is turning into a list of my grievances are issues caused/exacerbated/compounded by a lack of design when the arts access aotearoa event database was created.
### 1. Locations. The locations are just entered as a string when the event is entered into the system
* This means that there is no standard list of locations i.e. towns regions cities but rather whatever the user thinks works. It also means there is no child system so you cant look for north island and get results for every location in the north island instead you would only get results for something with a location listed as "north island". It also means that if you search wellington you only get results that list wellington so if an event is listed as lower hutt a search for wellington will not pick it up unless the user specifies wellington, lower hutt etc.
### 2. Categories. The categories are also just entered as random strings.
* This essentially means that any time someone creates an event they could add new categories that arent indexed by the skill
### 3. The events dont have an acessibility type checklist or anything
* If an event is NZSL interpreted this can only be advertised in the event title or description because there isn't a specific field that people creating the event can check - it would make indexing events easier and entering events easier. Basically having checkboxes or dropdowns where events can be listed as NZSL, Relaxed, Audio Described, Touch Tour etc. Because The events do say if they are wheelchair accessible, have accessible parking or accessible toilets. So there is definitely something.
### 4. NO CONTACT FIELD
* There is no field where the event organizer can enter contact details for event bookings i.e.[name, telephone, email] This means that there is no way for the skill to parse out or save contact details for event bookings
### 5. Multiple Sessions arent listed efficiently
* If an event has multiple sessions it is inconsistently listed in the database, most commonly just thrown into the full event description somewhere

## These Issues are more to do with the API itself but are compounded by the database issues. Which for the most part I think come down to a lack of design/planning in the building of the arts access aotearoa events database

### 1. The API hooks into the database function as a string search
* This means you can search for locations or categories individaully, but you cant search the api by listed event id, or by date or by accessibility types
### 2. API responses are paginated
* Its not a big deal by itself but coupled with a lack of pagination pointer (most paginated apis include an element called next that includes the  url for the next page of results) and the alexa's 8 second timeout means that getting multiple pages of results in one go can be very difficult. 
### 3. You cant search more than one term "string" at a time
* you can search the api for wellington or for music but you cant search for events that contain both music and wellington
### 4. Because of the way dates are stored you cant search the API for dates at all
* And even the date fields for an event just list a start and stop date /time 
### 5. No contact details included in the response body at all
### 6. Venue information (name + address) is not included in the response body just a general location
### 7. You cant search for an event by its event id
