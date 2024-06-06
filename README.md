## AutoSetGen 

- Automate the creation of setlists: Musician worklflows
- Automate the preparation for the gig including
* All songs alphabetized into a coherent readable songlist with metadata in a song.json format
* The artists the songs are by and all artifacts of the music

### Create the Code to Scaffold the WorkSpace 

- GPTScript will be used to script complex tasks and make them repeatable 
- Code will be in repo 


### Use Case: Age, Zip Code the Generate a Setlist

- Install [gptscript](https://github.com/gptscript-ai/gptscript) now. Visit [GPTScript.ai](https://gptscript.ai) .
- Prereq: Git `brew install git` 
```bash
brew install gptscript 
git clone [https://github.com/gptscript-ai/gptscript
cd gptscript
gptscript ./announce.gpt
```
- Now git clone this repo 
```
git clone https://github.com/michaelcolletti/AutoSetGen
cd AutoSetGen
```
- Edit the file to change the values or leave my defaults of jazz bebop jazz fusiona and  philly soul. 3 Songes will be selected 
- Be sure to add your OpenAI API Key by either a env variable `export OPENAI_API_KEY=XXXXXXXXXXXXX` or set in your .env file.
- Same applies to the Census Key easily obtained [here](https://api.census.gov/data/key_signup.html).
- **Be sure to not commit any keys in your repo. A great way to handle this is to use Github or a vault for secrets.**
