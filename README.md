 <!-- - Create SSH keys on your local machine.
    - Add a custom Arch Linux image using the web console
    - Create a Droplet running Arch Linux using the DigitalOcean web console.
    - Use a cloud-init configuration file to automate initial setup tasks (e.g., user -->
# <center> Creating and using Arch Linux Droplets.</center>
#### <center> By Michael Flood</center>

### Creating SSH keys on your ***local*** machine.
---
:memo: **Note** SSH keys are an authentication tool that acts as a special password, mainly used for connecting to a remote computer.

---

1. create a new folder named .ssh in a directory of your choosing.
![ if theres no image here fail me](/assets/sshfolder.png)

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
<img src="assets/Settings.png" alt="i must have made a whoopsy" height="300" width="300">
<br>
<br>

5. Click the security tab at the top of your page
![ security image](/assets/security.png)

6. click add SSH key and paste the contents of you do-key.pub into the first box, and make an easy to remember name for the second box.

    * :memo: **note** make the name simple, it is used later.

### Add your custom Operating System Image
---
:memo: **Note** in order to have a functional enviorenmnet to work with we need to choose and upload an image of whatever OS we want to play with. I will be demonstrating with Arch Linux.

---
1. navigate to the following link.
    * <a href="https://gitlab.archlinux.org/archlinux/arch-boxes/-/packages" target="_blank" rel="noopener noreferrer">Arch Linux gitlab Repo</a>
2. Open the most **recently** published images link.

3. We want to download the cloudimg qcow2 link.
![cloudimg qcow2 arch image](/assets/archlinuximage.png)

### Creating your first droplet

---
:memo: **Note** Droplets are similar to running a virtual machine on your computer with the exception that we deploy the Virtual Machine (Droplet) through DigitalOceans cloud servers negating the need for our own hardware to do any work. The Trade off is that we spend monthly amounts for our active droplets.

---

1. 

