## Administracion de servidores

# Segunda linea

# Steps

#### 1.- Generate idrsa private key and add a passphrase if needed with:
`ssh-keygen -t rsa -b 4096 -C email@example.com`

#### 2.- Generate public ssh key and enter the passphrase for the private key with:
`ssh-keygen -y -f ~/.ssh/id_rsa > ~/.ssh/id_rsa.pub`

#### 3.- Add key to ssh-agent with:
`eval "$(ssh-agent -s)"`

#### 4.- Add ssh key to system:
`ssh-add ~/.ssh/id_rsa`

#### 5.- Copy public key and paste it into your SSH keys in github:
`cat ~/.ssh/id_rsa.pub`

#### 6.- Now all local repositories with github as remote version controller can be pushed via SSH.
