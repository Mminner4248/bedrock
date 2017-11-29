**This boilerplate is a fork of https://github.com/roots/bedrock . Go to that url to get the full README for the stack.**

## This repo is a boilerplate for Tandem's WordPress Sites
### First time run on your WordPress Site utlizing this repo:

_Note: Don't init your repo with a README_

```bash
cd yoursite
git remote add bedrock git@github.com:thinktandem/bedrock.git
git fetch bedrock
git rebase bedrock/master

# Init Your Site
lando init --recipe wordpress

# Install dependencies
lando composer install

# Start up the site
lando start

# copy the env file
cp .env.lando .env
lando wp package install aaemnnosttv/wp-cli-dotenv-command
lando wp dotenv salts regenerate
```
Go into the .env file and change WP_HOME=http://CHANGEME.lndo.site to the proper url.

Go into the package.json and change the setup:db line and replace items that say CHANGEME with your site's information:

```bash
lando wp core install --url=http://CHANGEME.lndo.site --title=CHANGEME --admin_user=CHANGEME --admin_password=CHANGEME --admin_email=CHANGE@ME.com --skip-email```
```

Then run:

```bash
npm run setup
npm start
```

