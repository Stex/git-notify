git-notify
========

See original README at the bottom. This script is different to the original one as it currently can be only used for a certain git repository specified in the file itself.
This was necessary as the original script only saw changes which were already known to the local repository (through git-rev-parse). However, it might
happen in some repositories, that this command does not return the most current commit. 
My version uses the git-ls-remote command which actually asks the remote repository for the latest branch head.

Usage:
----------

    1. Update the script and fill in your repository details at the very top
    2. Run the script with ./git-notify

    The script accepts 2 operation parameters:
       ./git-notify start   (the default one which starts the script)
       ./git-notify stop    (which stops a running notifier)

TODO:
------------

Let the script accept additional parameters for repository and branch AND/OR take the remote repository from the current git directory?

Original Readme:
------------

This little bash script will watch your origin/master for updates every 60 seconds and uses notify-send to alert you of new commits.

I asked [this question](http://stackoverflow.com/questions/5082001/is-there-a-tool-to-watch-a-remote-git-repository-on-ubuntu-and-do-popup-notificat) on StackOverflow to find out if there was a tool to notify me of commits to remote git repositories, and the answer came back no!

Thus, git-notify was born!

