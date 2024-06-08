---

### Announcing AutoSetGen: Revolutionizing Setlist Creation with AI

We are thrilled to introduce **AutoSetGen**, a groundbreaking tool designed to automate the creation of music setlists tailored to specific demographics. Leveraging the power of GPTScript, AutoSetGen generates multi-genre setlists based on zip code and average age data, making it an invaluable resource for musicians and event planners.

#### Key Features:
- **Automated Setlist Generation**: Create setlists for different music genres using real-time data.
- **Customizable**: Easily edit genres and song selections to fit your needs.
- **Integration with OpenAI and Census APIs**: Fetch demographic data to tailor your setlists accurately.

#### Getting Started:
1. **Install GPTScript**:
   ```bash
   brew install gptscript
   git clone https://github.com/gptscript-ai/gptscript
   cd gptscript
   gptscript ./announce.gpt
   ```
2. **Clone AutoSetGen**:
   ```bash
   git clone https://github.com/michaelcolletti/AutoSetGen
   cd AutoSetGen
   ```
3. **Configure Your Environment**:
   - Edit the `autosetgen.gpt` file to customize genres.
   - Add your OpenAI and Census API keys.

4. **Run the Script**:
   ```bash
   gptscript autosetgen 12401
   ```

#### Future Plans:
- Develop a frontend UI for easier access.
- Explore serverless deployment options.

For more details, visit our [GitHub repository](https://github.com/michaelcolletti/AutoSetGen) and start automating your setlists today!

---

Stay tuned for more updates and enhancements. Happy music-making!

---
