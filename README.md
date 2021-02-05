DROPBEAR w/ RSA Key

Sebagai alternatif menggunakan ssh untuk melakukan koneksi ke server:

__generate the public and private keys:__

*dropbearkey -t rsa -f ~/.ssh/id_rsa*

__get output Public Key__
*dropbearkey -y -f "id_rsa" | grep "^ssh-rsa " > "id_rsa.pub"*

Setelah itu masukkan hasil output public key tersebut ke ~/.ssh/authorized_keys di server.

Example:

dbclient -y -i ~/.ssh/id_rsa user@site/ip