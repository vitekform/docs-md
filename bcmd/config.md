# BCMD Configuration

**What will we learn in this chapter?**
- [What is Execution Service](#execution_service)
- [Which functions require different service than INTERNAL](#functions)
- [How to configure Execution Service](#config)

<div id="execution_service">
## What is Execution Service
Execution Service is a way how the BCMD will attempt to execute specific commands.
Default is INTERNAL that means that BCMD will only have access to default Bukkit methods like Bukkit.shutdown() or similar. While using PTERODACTYL will allow us (if you are actually using it) to perform actions using the panel itself just like you would.
</div>
<br/>

<div id="functions">
## Which functions require different service than INTERNAL
Those functions require the Execution Service not to be set to INTERNAL.
- /timedrestart
- /restart
</div>
<br/>

<div id="config">
## How to configure Execution Service
1) Go to /plugins folder inside your server folder.<br/>
2) Go to BCMD folder inside the plugins folder<br/>
3) Open the config.yml (I recommend using Atom for editing YAML)<br/>
4) Find those "execution_service" variable and set it to:<br/>
- PTERODACTYL if using [Pterodactyl Panel](https://pterodactyl.io) or some forks of it like [Pelican Panel](https://pelican.dev)
- INTERNAL if none of the above suit your fancy.
5) If using INTERNAL you can skip this step.<br/>
Create API key for you account on your panel's page (Normally https://*PanelURL*/account/api)<img src="https://code.repos.vitekform.cz/docs/imgs/pic_apikey_setup.png" alt="API Key Setup" width="50%"/><br/>
Copy your API Key and paste it into the value of "service_api_ley"<br/>
6) Save the file<br/>
7) Restart server (!!!DON'T USE /reload PLUGIN WON'T WORK IF YOU USE /reload!!!)<br/>
</div>

<br/>
<footer>Last edited by [ganamaga](https://github.com/vitekform) on 20.01.2025 (BCMD 2.0)</footer>
