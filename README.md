# TeamCity Theatre

A .NET MVC web application to monitor your TeamCity builds. 
Stick a TV on the wall, open a browser there and enjoy your TeamCity projects in all their red and green glory.

## Screenshot

![The dashboard screen](http://i.imgur.com/izZiWVd.png)

## Features

- First-class support for branches! (This is a feature many others are lacking)
- Create multiple dashboards, one for each team!
- Customizable amount of branches shown per tile
- Customizable labels on tiles
- Customizable polling interval (this uses long polling, you don't need to install any TeamCity plugins)
- Responsive design using Bootstrap, make optimal use of the size of your wall TV!

## Requirements

- A TeamCity server (d'uh)
- A Windows Server with IIS to host the web application, or your Windows dev machine if you just want to try it out.
- Some knowledge on how to add a .NET web application in IIS, or the willingness to learn.
- A nice cup of coffee to drink while you install this. 

## Installation instructions

1. Download the latest release from the releases page
2. Install this web application on a Windows Server in IIS. (See [msdn](https://msdn.microsoft.com/en-us/library/ha2y9493.aspx) for detailed instructions)
3. Modify the web.config. 
    - Look for the `teamCityConnectionSettings` element and enter a valid server-username-password combination.
    - Change appSetting `TeamCityTheatre.Workspace` to an appropriate folder or leave the default
    - Change appSetting `TeamCityTheatre.Workspace.ConfigurationFile` to an appropriate file name or leave the default
    - Change appSetting `TeamCityTheatrwe.PollingTimeOutInMilliSeconds` to an amount of milliseconds or leave the default
4. Open the web application from a browser
    - Open the configuration page from the main menu. 
        - If you see any errors in the console, your server or credentials are probably incorrect.
    - Add a new view
    - Expand your TeamCity projects in the left bottom pane
    - Added builds to your view
    - Open the dashboard from the main menu
    - Click on one your created views
    - Enjoy.