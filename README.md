
### Automation for Tableau Bridge on Linux Docker Containers

### Terms of Use
This repo contains source code and example files for creating Tableau bridge Linux containers.
These scripts may be useful but are unsupported. Please get help from other users on the Tableau Community Forums.


### High-Level Steps
1. Collect the required information: tableau cloud site_name, pool_id, PAT token
2. Download Bridge Linux .rpm installer file
3. Download Database drivers
4. Create a Bridge container image
5. Run the Bridge container


### Prerequisites
1. Docker
2. Bash shell
3. For Database Drivers, you'll need a bash script to download and install them in the container.


### Project Contents:
#### /build_docker_basic
Basic example of building a Tableau Bridge Linux container image and running a container.
1. download.sh - bash script to download Tableau Bridge Linux .rpm installer file and database drivers.
2. Dockerfile - Definition for creating Tableau Bridge Linux container.
3. start-bridgeclient.sh - script copied into container and used to start the bridge client when the container starts.
4. build_image.sh - bash script for executing docker build to create a container image.
5. run_container.sh - bash script for executing docker run to run a container.


### Documentation for Tableau Bridge
See official Tableau documentation for creating bridge containers on Linux
https://help.tableau.com/current/online/en-us/to_bridge_linux_install.htm


### BridgeCTL Setup
Automatic Setup
An automated setup script, which you can run with the following commands:
Note that this utility is a prototype, not supported by Tableau, and may change in the future.
```
curl -L https://github.com/tableau/bridgectl/releases/download/setup/bridgectl_setup.py --output bridgectl_setup.py
python bridgectl_setup.py
```

**Auto-updates:** 
Each time BridgeCTL is started, it will check for updates and give the option to apply the latest updates.
