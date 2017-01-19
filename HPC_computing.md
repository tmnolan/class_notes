#HPC computing 	


##ssh into hpc cluster
can login to systems on campus like speedy

ssh name@speedy.ent.iastate.edu
Password:
Last login...
name@speedy $ 

above promt shows that you are now on the system

*	often need to check what other ppl are doing on the hpc cluster before you run your job. use top or htop to check. 
* once you start your job then you can see what the ETA for being done is. Good to check this to make sure how long/how many resources you are using. 

##Getting faster access to hpc
* Navigate to hidden directory:

	~/.ssh/config
	
	alter the file:
	
		Host speedy
   		Hostname speedy.ent.iastate.edu
   		 
* generate a passphrse: public key (put on remote machine. And private key (on your laptop). The two match up and don't need your password. 

		Trevors-MacBook-Pro-3:~ TrevorNolan$ ssh-keygen-t rsa
		Generating public/private rsa key pair.
		Enter file in which to save the key (/Users/		TrevorNolan/.ssh/id_rsa): 
		Enter passphrase (empty for no passphrase): 
		Enter same passphrase again: 
		########################
		 #don't share this key#
		Your identification has been saved in /Users/		TrevorNolan/.ssh/id_rsa.
		########################
		#can copy this into github or hpc#
		Your public key has been saved in /Users/		TrevorNolan/.ssh/id_rsa.pub. 
		########################
		The key fingerprint is:
		SHA256:B01Caty+31gdvRItOU3MRrbZ0CCMA3ustS0vxPhtiSE 		TrevorNolan@Trevors-MacBook-Pro-3.local
		The key's randomart image is:
		+---[RSA 2048]----+
		|       .+..o. o= |
		|     . o *o ..=.=|
		|      + + =.   B.|
		|     . . B o  *. |
		|        E B .=.o.|
		|         * * o+..|
		|        . + *... |
		|         . *  .  |
		|          o .    |
		+----[SHA256]-----+
	* now should be able to type ssh tmnolan@speedy to login

