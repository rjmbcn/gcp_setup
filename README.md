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
