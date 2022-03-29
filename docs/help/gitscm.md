# Guide for installing Git SCM

1.  Go to: <https://git-scm.com/>

2.  Download and install:

    A.  For PC:
    -  Run the installer and go through the installation wizard. 
    -  ![](./media/gitInstall.png){: style="max-width:500px"}

    B.  For Mac:
!!! note
    Make sure you have [Homebrew installed](https://brew.sh/). If you can run the command 'brew' then you are good to go.



 - Open launcher and search 'Terminal':
 ![](./media/gitcsm_mac_terminal.jpg){: style="max-width:500px"}

 - In the terminal then type `brew install git`:
 ![](./media/terminalup.png){: style="max-width:500px"}
 


3.  Launch the command prompt (PC) or stay inside the terminal (Mac) and run:
```bash
git --version
```
This tests the installation: 
    ![](./media/image5.png){: style="max-width:500px"}
     - If it is working, move to **step 4**
     - If it is not working, send an email or post on the GitHub discussion board.

4.  Set our identity to our GitHub username for Git by running:  
```bash
git config --global user.name "YOUR_GITHUB_USERNAME"
```
!!! important
    Remember to change `"YOUR_GITHUB_USERNAME"` to your actual GitHub Username and include the double quotes `" "`

1.  Now set your email to the email you signed up with GitHub by running :

```bash
git config --global user.email YOUR@EMAIL.COM
```

!!! important
    Remember to change `YOUR@EMAIL.COM` to your actual GitHub email

<!-- -->

1.  Once finished, run the following to check your email and username:
`git config --list`

7.  If you had any issues, please check this documentation for more
    details or reach out for help.

8.  Now you are ready to [clone a repository](git_cloning.md) in [VS Code](https://code.visualstudio.com/)!
