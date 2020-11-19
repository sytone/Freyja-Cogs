# Athena-Cogs
Random cogs I have created for [Red-DiscordBot](https://github.com/Cog-Creators/Red-DiscordBot).

## Working Cogs
These are at a point where you can actually use them.
* kankaview - Access your [Kanka](https://kanka.io) campaigns from Discord.

## Installation Notes

### General
I haven't gotten around to applying for cogs.red listing yet so you won't be able to install them through there. Instead you'll want to run these two commands (`[p]` should be replaced with the bot's command prefix):

1. `[p]load downloader`
2. `[p]repo add Freyja-Cogs https://github.com/sytone/Freyja-Cogs`
3. `[p]cog install Freyja-Cogs <cogname>`
4. `[p]load <cogname>`

### KankaView

For this to work you'll need an Personal Access Token for Kanka. You can get this on your profile page, but you will need to contact the dev for API permissions first.

1. `[p]kankaset token <Personal Access Token>`
2. `[p]reload kankaview`
3. `[p]kanka campaign <Campain ID>`

**Tips**

Your most used command will likely be the search command. I recommend setting up an alias for this command. I use 'dnd' since I am using Kanka for my D&D campaign, and that is a command that my players will easily recognize.
1. `[p]load alias`
2. `[p]alias add dnd kanka search`

Whenever you add a large number of entities to the campaign, you can significantly reduce loading times for the bot by running the refresh command `[p]kanka refresh`


## Dev Environment

```pwsh
python -m venv .\redenv
.\redenv\Scripts\Activate.ps1
python -m pip install -U pip setuptools wheel
python -m pip install -U Red-DiscordBot
```

## Docker Setup

Update docker compose with the token for your Discord Application first then run the following commands.

```pwsh
docker-compose pull
docker-compose up -d --remove-orphans
docker image prune -f
```