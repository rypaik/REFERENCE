Host * 
	AddKeystoAgent yes	
	# UseKeychain yes



# Ryan Github
Host github.com-ryanpaik2002
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_work_rp2002_github
   IdentitiesOnly yes


# Swingology Github
Host github.com-swingology
   Hostname github.com
   User git
   IdentityFile ~/.ssh/id_rsa_gh_swing
   IdentitiesOnly yes


# Swingology DOCSETS REPO
Host DOCSETS.github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_gh_swing
   IdentitiesOnly yes
	
Host origin.github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_work_rp2002_github
   IdentitiesOnly yes