 <!-- - Create SSH keys on your local machine.
    - Add a custom Arch Linux image using the web console
    - Create a Droplet running Arch Linux using the DigitalOcean web console.
    - Use a cloud-init configuration file to automate initial setup tasks (e.g., user -->
# <center> Creating and using Arch Linux Droplets.</center>
#### <center> By Michael Flood</center>

## Creating SSH keys on your ***local*** machine.
:memo: **Note** SSH keys are an authentication tool that acts as a special password, mainly used for connecting to a remote computer.

1. create a new folder named .ssh in a directory of your choosing.
![ if theres no image here fail me](/assets/sshfolder.png).

2. Open up your windows terminal and input the below text, changing **~/.ssh/do-key** to your .ssh folders path. and **youremail** to your preferred email account.

    * :memo: **note** if you are on windows you  will need to use your full path. i.e  
     C:\Users\your-user-name\.ssh\do-key

``` 
    ssh-keygen -t ed25519 -f ~/.ssh/do-key -C <youremail@email.com>
```
3. You will be given the choice of either having a password or not.
    * typing ** Enter ** twice  will result in you having no password for your SSH key.

    * whatever you enter into the field will  become your password going forward.
4. visit DigitalOcean and navigate to the **settings** menu which is located in the lefthand side of your screen.
![ im sorry this is all getting done in one day im still catching up on everything from missing a class](/assets/Settings.png 200x300).