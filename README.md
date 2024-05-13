# kubectl-commander

This script uses the `fzf` command-line tool to create an interactive menu for selecting and manipulating Kubernetes objects.

When you run this script, it will create an interactive menu that allows you to select one of these options for each object in your Kubernetes cluster. The selected option will be executed on the current object, and any relevant output (e.g., logs or events) will be displayed in a new terminal window.

Conveniant like a gui, quick and responsive like a cli ;)
<img width="1451" alt="image" src="https://github.com/schabrolles/kubectl-commander/assets/19491077/4353f385-4fce-421f-897f-18a6cb90fc29">


## Key Bindings:

| key Binding     | Actions                                                        |
|-----------------|----------------------------------------------------------------|
| ctrl-h          | print this help menu                                           |
| ctrl-q          | Quit                                                           |
| ctrl-r          | Reload                                                         |
| TAB             | select items                                                   |
| ctrl-a          | select all items                                               |
| ctrl-alt-a      | deselect all items                                             |
| ctrl-y          | preview YAML.<br>* press this key several time to cycle between preview mode (right,top,hidden)<br>* press 'Enter' to add/change the yq query (default is '.') .           |
| ctrl-v          | preview and follow Events (for objects which have events)<br>* press this key several time to cycle between preview mode (top 50%,top 80%,hidden)<br>* press 'Enter' to follow the events in full screen |
| ctrl-l          | preview and follow Logs (for pods)<br>* press this key several time to cycle between preview mode (top 50%,top 80%,hidden)<br>* press 'Enter' to follow the events in full screen            |
| ctrl-x          | Enter into container (for pods, deployments)                   |
| ctrl-d          | /!\\\\\ delete object /!\\\\\ (works with multi selection)     |
| ctrl-e          | edit object                                                    |
| ctrl-s          | edit secret (decrypt/encrypt)<br>-> (need 'modify-secret' krew plugin)|
| ctrl-w          | toggle watch mode (automatic refresh 2s)                       |
| alt-l           | toggle wrap line in preview (default off)                      |


## Installation

Put the kubctl-commander into a directory that is part of your PATH environement variable. (like /usr/local/bin).

- check the directries part of your PATH
```
echo $PATH
```

- Copy the plugin into the chosen directory and set the execute permission on it.
```
cp kubectl-commander /usr/local/bin
chmod +x /usr/local/bin/kubectl-commander
```

## Usage

