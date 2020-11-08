## SSH Linux

The ssh command provides a secure encrypted connection between two hosts over an insecure network. This connection can also be used for terminal access, file transfers, and for tunneling other applications. Graphical X11 applications can also be run securely over SSH from a remote location.

### What is a public key authentication?

OpenSSH server supports various authentication schema. The two most popular are as follows:

1. Passwords based authentication

2. Public key based authentication. It is an alternative security method to using passwords. This method is recommended on a VPS, cloud, dedicated or even home based server.


### How to set up SSH keys

1. Create the ssh key pair using ssh-keygen command.

2. Copy and install the public ssh key using ssh-copy-id command on a Linux or Unix server.

3. Add yourself to sudo or wheel group admin account.

4. Disable the password login for root account.

5. Test your password less ssh keys login using ssh user@server-name command.


### Create the key pair

``` ssh-keygen -t rsa ```

1. $HOME/.ssh/id_rsa– contains your private key.

2. $HOME/.ssh/id_rsa.pub – contain your public key.

<b>Optional syntax for advance users</b>

The following syntax specifies the 4096 of bits in the RSA key to creation (default 2048):

``` $ ssh-keygen -t rsa -b 4096 -f ~/.ssh/vps-cloud.web-server.key -C "My web-server key" ```

Where,


-   -t rsa : Specifies the type of key to create. The possible values are “rsa1” for protocol version 1 and “dsa”, “ecdsa”, “ed25519”, or “rsa” for protocol version 2.

-    -b 4096 : Specifies the number of bits in the key to create

-    -f ~/.ssh/vps-cloud.web-server.key : Specifies the filename of the key file.

-    -C "My web-server key" : Set a new comment.


### Install the public key in remote server

Use scp or ssh-copy-id command to copy your public key file (e.g., $HOME/.ssh/id_rsa.pub) to your account on the remote server/host (e.g., nixcraft@server1.cyberciti.biz). To do so, enter the following command on your client1.cyberciti.biz:

``` ssh-copy-id -i $HOME/.ssh/id_rsa.pub user@server1.cyberciti.biz ```

OR just copy the public key in remote server as authorized_keys in ~/.ssh/ directory:

``` scp $HOME/.ssh/id_rsa.pub user@server1.cyberciti.biz:~/.ssh/authorized_keys ```

On some system ssh-copy-id command may not be installed, so use the following commands (when prompted provide the password for remote user account called vivek) to install and append the public key:


First create .ssh directory on server ##

``` ssh vivek@server1.cyberciti.biz "umask 077; test -d .ssh || mkdir .ssh" ```
 
cat local id.rsa.pub file and pipe over ssh to append the public key in remote server ##

``` cat $HOME/.ssh/id_rsa.pub | ssh vivek@server1.cyberciti.biz "cat >> .ssh/authorized_keys" ```

The syntax is as follows for the ssh command:

``` ssh user@server1.cyberciti.biz ```
``` ssh user@your-server-ip-address ```
``` ssh -i ~/.ssh/your-key user@your-server-ip-address ```

Or copy a text file called foo.txt:

``` scp foo.txt user@server1.cyberciti.biz:/tmp/ ```

You will be prompted for a passphrase. To get rid of passphrase whenever you log in the remote host, try ssh-agent and ssh-add commands.



https://www.cyberciti.biz/faq/how-to-set-up-ssh-keys-on-linux-unix/
