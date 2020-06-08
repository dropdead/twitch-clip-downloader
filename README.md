# Twitch Clips Downloader
NodeJS tool to download every clip (and it's metadata) from a Twitch channel

## Dependencies
  - NodeJS
  - NPM
  - Twitch App Client-ID
  
## How to use

##### Create an app on Twitch Console

Register another application on [Twitch Console](https://dev.twitch.tv/console/apps), click **Manage** and copy the **Client ID**.

##### Copy .env.example

Just manually copy (or rename it) the provided `.env.example` to `.env`


##### Fill .env information

You must fill the `CLIENT_ID` with your newly created Client ID from Twitch Console.

That's it, nothing else is needed, but if you want to tweak some stuff, here are the descriptions for each variable:

  - `DEBUG`: print some extra information, just keep it false;
  - `PAGINATION_SIZE`: how many clips to fetch per API call, I don't see a reason to set to 100;
  - `YOUTUBEDL_INSTANCES`: how many concurrent youtube-dl instances should be used to download clips. Don't go too high because youtube-dl is pretty CPU intensive, and if you are storing in a HDD, it's just not worth it.

##### Install NodeJS dependencies

Run on your console:
```bash
npm install
```


##### Run via NPM

Run the script via NPM with (this is needed to get `dotenv` loaded):
```bash
npm run start
```
