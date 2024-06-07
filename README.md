## AutoSetGen 

*This repo is the start of a series of projects designed specifically for musician worklflows and a subset of work using AI toolings to reduce toil for artists. 

Below we will automate the creation of setlists. Beyond this, charts/notation, lead-sheets, transpositions, streaming playlists, etc. IOW Automate all the things!! Preparation for the gig including:*

### Setup with GPTScript 

- GPTScript rocks! This is partially a fanboy post!
- GPTScript will be used to script complex tasks and make them repeatable 

### AutoSetGen: Use GPTScript and Generate a multi genre setlist based on Age, Zip Code 


- Install [gptscript](https://github.com/gptscript-ai/gptscript) now. Visit [GPTScript.ai](https://gptscript.ai) .
- Prereq: Git `brew install git` 
```bash
brew install gptscript 
git clone [https://github.com/gptscript-ai/gptscript
cd gptscript
gptscript ./announce.gpt
```
- Now git clone this repo, cd into the project
```
git clone https://github.com/michaelcolletti/AutoSetGen
cd AutoSetGen
```

- Edit the [autosetgen](./autosetgen.gpt) file to change the values or leave my defaults of: jazz, bebop, jazz fusion, and philly soul. 3 Songs will be selected.
- Be sure to add your OpenAI API Key by either a env variable `export OPENAI_API_KEY=XXXXXXXXXXXXX` or set in your .env file.
- The same applies to the Census Key easily obtained [here](https://api.census.gov/data/key_signup.html).
- **Be sure to not commit any keys in your repo. A great way to handle this is to use Github secrets or a vault for secrets.**
- After your environment and API keys are rockin, you're ready to start using your [autosetgen script](autosetgen.gpt)

### Running AutoSetGen 

- At a Bash command run the following: `gptscript autosetgen 12401` 
- Using US Census data, this will fetch the average age `average_age` for men and women for Kingston, NY. This with the current year so (2024 - average_age + 17). I added 17 years so I could get the music listened to when 17 years old. This is the `target_year`.
- Then the top 40 for each genre will be provided with the number of selections provided in `max_songs_per_genre` 
- The script can be automated locally (via cron or scheduler or as github action when the setlist in git is updated).  

#### Next steps

- A service with a front end for musicians to run imperatively.
- Test of using it with a serverless/Cloud Run or Lambda
  