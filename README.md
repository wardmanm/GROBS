# GROBS (Grand Raggidy OBS)
A mono-repo of assorted tools I've created to making streaming roller derby easier, more dynamic, and automated.  

---
## OBS Producer *(in development)*
A locally hosted web app for producing roller derby streams in OBS:
- **Builders** for teams, themes, and overlay screens. Screens are loaded into OBS as browser sources.
- **Live Mode** for events with multiple games and tracks running at once, with producer dashboards that preview and control what's on air.
- **Integrations** with OBS (scene switching, hotkeys) and the [CRG scoreboard](https://github.com/rollerderby/scoreboard). CRG is read-only: the app listens to it and never writes to it.

Start at the [OBS Producer wiki](obs-producer/docs/README.md).

---
## Simple IP Camera Controls
A simple tool for adding IP Camera controls to a browser window.  Set up to be easily accessible in an OBS dock or a separate browser window.
Gives the ability to export camera configurations and import them later if needed.  Uses pure javascript and does not require the user to run or build anything.

**Currently only supports AXIS cameras using the VAPIX API**

*Big shoutout to [Homer911](https://obsproject.com/forum/members/homer911.300179/) on the OBS forums for providing the original button code [here.](https://obsproject.com/forum/threads/ptz-control-for-axis-camera.117728/)*

---
