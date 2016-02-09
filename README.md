# pvc
### :snake: python version controller.
pvc is a shell script for managing multiple python versions. You can easily install, remove, and switch between multiple installs of python. This is incredibly useful for testing scripts out in different versions, as well as porting 2.7 code to 3.4. 


## state
pvc is currently in the alpha stages of development. Every piece of functionality is subject to a complete rewrite. This version is only meant to be a preview of things to come.


    pvc activate #looks for p.vc in the cwd and loads configuration
    pvc use [version] #use a specified python version
    pvc default #echo the system python version
    pvc default use [version] #set the user's default python version


The [version] string must be in the format 0.0.0. Currently there is no version index, so until that is added, there is no way to validate whether the user has entered a real python version. Because of this, you will receive a "failed to download" error for entering in a non-existent version.

## todo
- ~~write `install` function~~
- ~~write `uninstall` function~~
- write `default` function
    - The `default` function will be used for setting the user's default python version. The python version should be passed to the default command in the format `3.4.2`
- write `use` function
    - The `use` function will be used for changing the python version for the current session. This does not make permanent changes, and will revert back to the default python version upon opening a new session.
- write `activate` function
    - The `activate` function will be used to activate a python version specified in the `./p.vc` file. If there is no `p.vc` file in the current directory, it will display an error.
    - Activate should play nicely with virtual environments.