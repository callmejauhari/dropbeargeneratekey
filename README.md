DROPBEAR w/ RSA Key

Sebagai alternatif menggunakan ssh untuk melakukan koneksi ke server:

__generate the public and private keys:__

*dropbearkey -t rsa -f ~/.ssh/id_rsa*

__get output Public Key__
*dropbearkey -y -f "${KEY_DIR}/id_rsa" | grep "^ssh-rsa " > "${KEY_DIR}/id_rsa.pub"*


Example:

dbclient -y -i ~/.ssh/id_rsa user@site/ip