**This boilerplate is a fork of https://github.com/roots/bedrock . Go to that url to get the full README for the stack.**

## This repo is a boilerplate for Tandem's WordPress Sites
### First time run on your WordPress Site utlizing this repo:

_Note: Don't init your repo with a README_

```bash
cd yoursite
git remote add bedrock git@github.com:thinktandem/bedrock.git
git fetch bedrock
git pull bedrock master --rebase

# Run the setup
npm run setup
```
