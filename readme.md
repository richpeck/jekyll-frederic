# Frederic Website

This is a `Jekyll` website for Frederic, to replace his old one that used PHP.

As Jekyll creates a set of static HTML pages, it's far more effective to use it than having a large set of files which need to be loaded by the server each time.

---

The site is deployed via [Github Actions](https://github.com/richpeck/jekyll-frederic/blob/main/.github/workflows/deploy.yml). 

It uses the [SamKirkland/FTP-Deploy-Action@4.3.0](https://github.com/SamKirkland/FTP-Deploy-Action) action to push a built version of Jekyll to the server.

The following secrets are used: -

 - `FTP_SERVER`
 - `FTP_USERNAME`
 - `FTP_PASSWORD`
 - `FTP_DIRECTORY`

The first three should be self explanatory. The last requires a trailing slash (it's currently set to `./httpdocs/`).

Once the action runs, the deployment should happen automatically.

I originally tried to build it on the server but it took too long and Plesk's Ruby support is patchy at best.
