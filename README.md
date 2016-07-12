# highnoon

> “Shall there be truth between us? 
> Not as friends, but as enemies and equals?” ― Stephen King, The Gunslinger

Simulates the typical Overwatch experience [playing against McCree](http://docs.highnoon.apiary.io/)

## How to Play

Battle with a cunningly simulated McCree AI using [public API endpoints](http://docs.highnoon.apiary.io/#reference/0/start-a-new-game/start-a-new-game?console=1) using your preferred client


## Build instructions
1. Download the [google-python sdk](https://cloud.google.com/appengine/downloads#Google_App_Engine_SDK_for_Python)
2. Install to your local librarie path `unzip -d /usr/local/lib/python2.7/dist-packages/google_appengine google_appengine.zip`
3. Add library path to system path `export PATH=$PATH:/usr/local/lib/python2.7/dist-packages/google_appengine`
4. (optional) add the previous command to your `~/.bashrc` to persist across logins
 
### dev

1.  Run the app locally with `dev_appserver.py $app_folder`
1.  Test by visiting the [API Explorer on your local box](https://localhost:8080/_ah/api/explorer`)
2.  (optional) make `curl` requests to API endpoints at localhost

 
### deploy

1.  Create a new application ID in [app-engine](https://console.cloud.google.com)
1.  Set `application` in app.yaml to the app ID you registered above
2.  Deploy to AppEngine using `appcfg.py update $app_folder`
> note: include the `--noauth_local_webserver` flag to authenticate from a headless box
> note: account credentials will be saved by default to `~/.appcfg_oauth2_tokens` - delete this file to be re-prompted to login as a different account
3. (optional) View and test endpoints at `$appname-appspot.com/_ah/api/explorer` 

![highnoon](http://img.ifcdn.com/images/8b3e2b0811fd853e566f1c06b54de1368dc8efb5faba84144f4839ed41e64cdc_1.jpg)

