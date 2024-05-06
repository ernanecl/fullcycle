### signing commits
#### check if there is a secret key on the machine
```
gpg --list-secret-key --keyid-form LONG
```
#### generate key
```
gpg --full-generate-key
```
#### configure subscription key with generated ID
```
git config --global user.signingkey <id_code>
```
#### configure environment variable <GPG_TTY=$(tty)> on bash
```
export GPG_TTY=$(tty)
vim ~/.bash_profile
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