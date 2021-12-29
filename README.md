# Project setup in google cloud compute engine 


# Install and initialize Cloud SDK in local machine
Cloud SDK is a set of tools that you can use to manage resources and applications hosted on Google Cloud. Download installer and follow instructions outlined here https://cloud.google.com/sdk/docs/install


Open a terminal and navigate to the directory containing the new “google-cloud-sdk” directory. Run the following command and follow the on-screen instructions. Hitting enter for all prompts should generally be sufficient.

    ./google-cloud-sdk/install.sh

Initialize the SDK

Open a new terminal and run the command

    gcloud init

Log in when prompted (the login window will pop up in your browser, log in using your Google account). Pick the cloud project to use, using the unique id assigned to the project you created above. 


*Cheat sheet*: https://cloud.google.com/sdk/docs/cheatsheet 

# VM-instance setup 

First install Anaconda 

``` 
wget https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh
bash Anaconda3-2021.05-Linux-x86_64.sh 
```  
reload your terminal, or run `source ~/.bashrc`

Then `ssh` into instance if you have not

Create environment, install programs, etc

Run `jupyter notebook --generate-config` and add the following in config file 

```
c = get_config()
c.NotebookApp.ip = '*'
c.NotebookApp.open_browser = False
c.NotebookApp.port = <YourPort>
```

## Launch Jupyter notebook 
In the remote terminal run 
```
jupyter notebook
```

Then in your local browser 

```
http://<external-ip-address>:enter< your port number>
```


# VS Code setup 

Follow this [note](https://towardsdatascience.com/unleash-the-power-of-visual-studio-code-vscode-on-google-cloud-platform-virtual-machine-f75f78f49aee).  
