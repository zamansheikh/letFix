how to setup github ssh key and use it from another devices, give me details guideline

Setting up an SSH key for GitHub and using it on multiple devices involves the following steps:

Generate an SSH key on the primary device:

Open a terminal window and run the command ssh-keygen.
Press Enter to accept the default location and file name.
Choose a strong passphrase to protect the key.
The key will be generated and saved in the ~/.ssh directory.
Add the SSH key to your GitHub account:

Open the public key file, typically located at ~/.ssh/id_rsa.pub, in a text editor.
Go to your GitHub settings and select "SSH and GPG keys" from the left sidebar.
Click on the "New SSH key" button and give it a descriptive title.
Copy and paste the contents of the public key file into the key field and click "Add SSH key".
Copy the SSH key to the other devices:

On the primary device, open the private key file, typically located at ~/.ssh/id_rsa.
Copy the contents of the private key file to your clipboard.
On the other devices, open the ~/.ssh directory and create a file named id_rsa.
Open the id_rsa file in a text editor and paste the contents of the private key file into it.
Save and close the file.
Configure the SSH key on the other devices:

On each device, run the command ssh-add ~/.ssh/id_rsa to add the key to the SSH agent.
Verify that the key has been added by running the command ssh-add -l, it should display the fingerprint of the key.
Test the connection:

Try to connect to GitHub by running the command ssh -T git@github.com on each device.
If prompted, accept the GitHub host key.
You should see a message indicating that you've successfully authenticated.
You should now be able to use the same SSH key on multiple devices to securely access your GitHub repositories. Remember to keep your private key safe and secure, and not to share it with anyone.
