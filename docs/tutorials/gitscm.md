# How to install GitSCM

1.  Go to: <https://git-scm.com/>

## Download and install

### Installing for PC

- Run the installer and go through the installation wizard. 

<img src="..\media\gitInstall.png" style="width:4.09743in;height:3in" />

### Installing for Mac

- Make sure you have [Homebrew installed](https://brew.sh/)  
- Open launcher and search “terminal”:

<img src="..\media\gitcsm_mac_terminal.jpg" style="width:6in;height:4in" />

- In the terminal then type the following:

``` bash
run brew install git
```
<img src="..\media\terminalup.png" style="width:6in;height:4in" />

## Test installation

Launch the command prompt (PC) or stay inside the terminal (Mac) and run the following to test the installation:
``` bash
git --version
```

<img src="..\media\image5.png" style="width:4.09743in;height:0.98616in" />
     
- If it is working, move to **step 4**

- If it is not working, send an email, ask on the [Discord server](https://discord.gg/BpWSHYNsZA), or post on the [GitHub discussion board](https://github.com/albertkun/22S-ASIAAM-191A/discussions).

<!-- -->

1.  Set our identity to our GitHub username for Git by running:  
    `git config --global user.name "YOUR_GITHUB_USERNAME"`
    - Remember to change `"YOUR_GITHUB_USERNAME"` to your actual GitHub Username and include the double quotes `" "`

2.  Now set your email to the email you signed up with GitHub by running :
`git config --global user.email YOUR@EMAIL.COM`
    - Remember to change `YOUR@EMAIL.COM` to your actual GitHub email

<!-- -->

6.  Once finished, run the following to check your email and username:
`git config --list`

7.  If you had any issues, please check this documentation for more
    details or reach out for help.

8.  Now you are ready to clone a repository!
