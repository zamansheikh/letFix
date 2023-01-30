# zsh: permission denied: reading anyway



this is the error its showing now

enter image description here

I was installing "Laravel" through a tutorial and now i am facing this error "zsh: locking failed for /users/vishnu.zsh_history: permission denied: reading anyway"

macos:- catalina v10.15

I am using macbook air, I don't have any idea what happened it happened while I was installing composer and a file was missing to get that file I ran some "chown" command and now I cant even open my chrome browser

Please Help




You can run this command :

    sudo chown -R ${LOGNAME}:staff $HOME

to make sure the owner is correct for your files.


