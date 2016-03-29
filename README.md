# MagicMirror V2
This version of the Magic Mirror software focusses on a modular plugin system. Besides that, the Magic Mirror software now also uses [Electron](http://electron.atom.io/), so no more webserver or browser installs necessary. 

#WARNING: THIS VERSION IS IN A VERY EARLY STAGE. IT IS NOT COMPLETED YET. PLEASE USE THE MASTER BRANCH.

##Usage 
1. Install [Node.js](https://nodejs.org/en/)
2. Execute `npm install && npm start`.

##Configuration
1. Duplicate `config/config.js.sample` to `config/config.js`.
2. Modify your required settings.

##Todo
Things that still have to be implemented or changed.
####Loader
- Loading of module uses `eval()`. We might want to look into a better solution. [loader.js#L112](https://github.com/MichMich/MagicMirror/blob/v2-beta/js/loader.js#L112).

####Helper scripts
- Only start helper scripts of modules that are actually loaded in the UI (config.js)
- Notification system, so that not every helper scripts needs it's own socket to the UI.
- `modules/newsfeed/node_helper.js` now spawns it's own epxress webserver on port 8080. We need to create a solution for every module that needs a server side url.


