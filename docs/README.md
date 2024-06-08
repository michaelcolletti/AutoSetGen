## AutoSetGen 

*This repo is the start of a series of projects designed specifically for musician worklflows and a subset of work using AI toolings to inject real-time data into everyday work and reduce toil for artists.*
</p>

  **Below, we will automate the creation of setlists. It starts with GPTScript.** 

### Setup with GPTScript 

*GPTScript rocks! This is partially a fanboy post.* 
- The GPTScript framework will be used to automate and make repeatable complex tasks.

### AutoSetGen: Use GPTScript and Generate a multi genre Setlist based on Age, Zip Code 


- Install [gptscript](https://github.com/gptscript-ai/gptscript) now. Get started by visiting [GPTScript get started](https://github.com/gptscript-ai/gptscript?tab=readme-ov-file#getting-started).
- Prereq: Git `brew install git` 
</p>

```sh
brew install gptscript 
git clone [https://github.com/gptscript-ai/gptscript
cd gptscript
gptscript ./announce.gpt
```

- Now git clone this repo, cd into the project

```bash
git clone https://github.com/michaelcolletti/AutoSetGen
cd AutoSetGen
```

- Edit the [autosetgen](./autosetgen.gpt) file to change the values or leave my defaults of: jazz, bebop, jazz fusion, and philly soul. 3 Songs will be selected.
- Be sure to add your OpenAI API Key by either a env variable `export OPENAI_API_KEY=XXXXXXXXXXXXX` or set in your .env file. 
- The same applies to the Census API key easily obtained [here](https://api.census.gov/data/key_signup.html).
- **Be sure to not commit any keys in your repo. A great way to handle this is to use local .env files, Github secrets or a vault for secrets.**
- After your environment and API keys are rockin, you're ready to start using your [autosetgen script](autosetgen.gpt)

### Running AutoSetGen 

- At a Bash command in your project run: `gptscript autosetgen 12401` 
- Using US Census data, this will fetch the average age `average_age` for men and women for Kingston, NY. This with the current year so (2024 - average_age + 17). *I added seventeen years so I could get the music listened at seventeen and all tha brings.* This is the `target_year`. 
- Will need to experiment with tweaking this number for prime nostalgia.
- Then the top 40 for each genre will be provided with the number of selections provided in `max_songs_per_genre` 
- See a Asciinema demo [here](https://asciinema.org/connect/dacc4acc-5c7d-4774-a644-4c8c868c0d72)
- The script can be automated locally (via cron or scheduler or as github action when the setlist in github is updated).

*This is just a small capability of the powerful GPTScript framework. I remember creating my first infrastructures in Terraform. OMG! How giddy I was when writing automation using providers and modules. GPTScript is like that but 10x with the new stack of completely different tools, tasks and capabilities.* 


### Looking for Open Standards: Towards a  Music-Packaging-Format: 
- I was looking to create a package around these artifacts as way to share, distribute and improve them. 
- Design/Run a small pipeline via containers or github actions to create a multi-modal media  package for the date treating similar to a complex software package release.  Maybe this would or is already working for touring artists technical support. Another possibility is using the publish/subscribe architectural model and the ability to manage and scale dynamic change easily. 
  
#### Next steps

- A service with a frontend UI for musicians to run imperatively or scheduled.
- Test of using it with a serverless/Cloud Run or Lambda
  