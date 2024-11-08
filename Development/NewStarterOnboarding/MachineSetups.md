## Software installation
To get going, install the following software:
* Visual Studio 2022 (community edition is fine)
* Visual Studio Code
* SQL Server Developer Edition
* SSMS
* .Net 8
* .Net 7 (although this is out of support * currently)
* .Net Framework 4.7.1
* git
* Node (14, 18, 20)
* ng-rok
* eventstore

## Cloning the repositories
[The repository list is here](CloningRepositories.md)

[Branching strategy](Branching.md)

# Setup eventstore
Copy the eventstore folder to your local machine
suggested: `C:\eventstore` or within your user folder

Edit the EventStore - v2_0.cmd file to reflect the folder that you just created
```
cd C:\EventStore\EventStore-OSS-Win-v5.0.10
EventStore.ClusterNode.exe --run-projections=all --db C:\eventstore\picup-db --log C:\Users\{userName}\DB\EventStore\picup-logs
```

# Setup ng-rok
## Step 1:
Create a folder in your user for ngrok:
c:\users\{username}\.ngrok

* Create a blank yaml file and paste the following code in it:
* replace the {username} with your local user name
```
authtoken: 1rnFABsv1oQKClUT0qM3rBEemco_nV3nKjajYg5FES5iQrdh
region: eu
tunnels:
  {username}:
    proto: http
    addr: 54321
    host_header: localhost:54321
    subdomain: {username}picup
 ```
    
## Step 2:
Once you have extracted the content of the ngrok2 zip folder hosted in this repository, 
Copy the ngrok 2 folder to your user folder
the structure should look like this:
`C:\users\{username}\ngrok2\ngrok`

Alternatively create a folder in your user folder:
`C:\users\{username}\ngrok2`
Paste the ngrok folder from the extracted zip file in the folder above

Edit the `ngrok.cmd` file
Change the top line to reference the local folder you created above:

```
cd\users\{username}\ngrok2\ngrok
ngrok.exe start {username}
```

# Initial run
When you run the solution the first time, there might be some errors and warnings in the IDE regarding nuget packages.
Add the picup nuget package to the Nuget Package Manager
The URI is: `picupnuget.azurewebsites.net/api/v2`

To resolve the types error, mentioned above, run the following from the Nuget Package manager console:
`Update-Package -reinstall`

At this point, you should already have a configuration created for you, if you don't ask someone for assitance.

Choose a default configuration for the first run i.e. `Debug`