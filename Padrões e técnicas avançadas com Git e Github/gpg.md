### signing commits
#### check if there is a secret key on the machine
```
gpg --list-secret-key --keyid-form LONG
```

#### generate key
```
gpg --full-generate-key
```

#### export public key
```
gpg --armor --export <id_rsa>
```


### configuring environment with new id_rsa
#### configure subscription key with generated id rsa
```
git config --global user.signingkey <id_rsa>
```

#### automatic commit signing per repository
```
git config commit.gpgsign true
```

#### automatic global signing of commits
```
git config --global commit.gpgsign true
```

#### automatic global tag signing
```
git config --global tag.gpgsign true
```

#### configure environment variable <GPG_TTY=$(tty)> on bash
```
export GPG_TTY=$(tty)
```
```
vim ~/.bash_profile
```


### configuring agent on Linux when it is not working automatically
#### on Linux create gpg.conf in the gnupg directory and add <use-agent>
```
vim ~/.gnupg/gpg.conf
```

#### activate agent to not request validation key again
```
gpgconf --launch gpg-agent
```


### check signature after first commit
```
git log --show-signature -1
```


### create new profile for rsa key
#### edit settings gpg
```
gpg --edit-key <id_rsa>
```

#### add new id
```
adduid
```

#### select id
```
uid <number>
```

#### make credentials trustworthy
```
trust
```