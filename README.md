# This site is a boilerplate for our WordPress Sites
## To utilize this boilerplate locally, do the following within your WordPress Site

```bash
cd yoursite
git remote add bedrock git@github.com:thinktandem/bedrock.git
git fetch bedrock
git rebase bedrock/master

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

**This boilerplate is a fork of https://github.com/roots/bedrock . Go to that url to get the full README for the stack.***
