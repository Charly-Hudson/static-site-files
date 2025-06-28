1. # Fork This repo
    - Go to the following link and click the fork button located in the top right next to star
    ```
    https://github.com/Charly-Hudson/static-site-files.git
    ```
    - Then name your repo, you can keep the same name to make things easy
2. # Login to Azure and create a Static Web App
    - you should log into your azure account at 
    [login.microsoft](https://go.microsoft.com/fwlink/p?linkid=2165195&clcid=0x409)
    - In the search bar look for **Static Web Apps** NOT **App Services**
    - Click the Create Button where you will be presented with some Options:
        * ## Basics:
            * **Subscription:** *Any Subscription you choose*.
            * **Resource Group:** *Create a new one called* .
            ```
            portfolio-rg
            ```
            * **Name:** 
            ```
            Portfolio
            ```
            * **Hosting Plan:** Free for hobby or personal projects.
            * **Source:** GitHub.
                - You should log in to your git hub account here (The same one you forked this repo in).
            * **Organization:** Select your profile name.
            * **Repository:** Selects the **static-site-files** repo you created earlier.
            * **Branch:** Keep this to main.

            * **Build Presets:** Keep this Custom (detected)
            * **App Location:** This should automatically default to 
            ```
            ./site-files
            ```
            * **API location:** Keep this bank you dot have an API yet
            * **Output location:** Keep this as . 

        * ## Deployment configuration:
            * **Deployment authorization policy:** Select Github.
        * ## Advanced:
            * Keep This As Is.
        * # Tags:
            * Tag this if you want to.
        * # Review and create
            * Now you can review and create, this will take a second to build the creation script so wait for the view to become active and click create and make your Static Web App.
            * You will be redirected to a status page showing you the creation status just wait for that to finish.
            * Click the **Go To Resource** button and copy the URL from the overview tab this will open your site in a new tab.
            * You will be presented with a page asking you to wait while your app is being built if you wish to see the status of your app return to your fork of the Github Repository and click the actions tab located on the top left (4th icon) where you can view the workflow run.
            * As soon at the workflow finishes you can refresh the page for your Static Web App, and voula, you have a portfolio,
    - # Changing the site:
        * If you wish to change the site you can use git to do this, just clone your repo locally make some changes and upload, you will see that the workflow will trigger every time you push an update to the main branch, juts be sure that you only change files in the **site-files** folder as this is where you actual site files are the rest of the files and folders are for GIT and VSCode, containing the following:
            ```
            - .gitaributes
            - .github/
                ¬ workflows/
                    ¬ azure-static-web-apps-<web-app-name>.yaml
            - .vscode/
                    ¬ settings.json
            - README.md
            ```