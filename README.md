# Send Encrypted Messages
Use GPG to communicate securely.

- [ ] Problem
- [ ] Solution
- [ ] How To Guide

## Generate GPG Keys

**Use Interactive Dialog to Create a Key Pair**
```shell
gpg --full-generate-key
```
### Select Type of Key
Enter `1`
```shell
Please select what kind of key you want:
    (1) RSA and RSA (default)
    (2) DSA and Elgamal
    (3) DSA (sign only)
    (4) RSA (sign only)
```

**Enter `4096` for key size.**

Enter a name, email address, and comment to associate with the key pair. Any one of these three values can be used to identify the keypair for future use

### Construct a User ID to Identify Your Key
```shell
Real name: [NAME]
```

```shell
Email address: [EMAIL]
```

#### Confirm Identity
Verify the user identity entered is correct. Enter `0` for Okay to confirm.
```shell
Change (N)ame, (E)mail, or (O)kay/(Q)uit?
```

### Protect Key with Passphrase
Enter a passphrase to protect the new key. You will be prompted to enter the passphrase twice.

## List Keys

**List Public Keys**
```shell
gpg --list-keys
```

**List Private Keys**
```shell
gpg --list-secret-keys
```

## Export Keys

**Export Public Key**
```shell
gpg --export -a "John Doe" > public.key
```

```shell
 gpg --armor --output public-key.gpg --export user@example.com
 ```

**Export Private Key**
```shell
gpg --export-secret-key -a "John Doe" > private.key
```

## Import Keys

**Import Public Key**
```shell
gpg --import public.key
```

**Import Private Key**
```shell
gpg --allow-secret-key-import --import private.key
```

## Delete Keys

**Delete Public key**
```shell
gpg --delete-key [REAL_NAME]
```

```shell
gpg --delete-key "John Doe"
```

**Delete Private Key**
```shell
gpg --delete-secret-key [REAL_NAME]
```

```shell
gpg --delete-secret-key "John Doe"
```

## Generate Fingerprint
```shell
gpg --fingerprint
```

## Encrypt Data

## Decrypt Data

- [ ] What's next?

**Reference Material**
https://www.howtogeek.com/427982/how-to-encrypt-and-decrypt-files-with-gpg-on-linux/
1. https://www.digitalocean.com/community/tutorials/how-to-use-gpg-to-encrypt-and-sign-messages
2. https://source.opennews.org/articles/how-lose-friends-and-anger-journalists-pgp/
3. https://privacyforjournalists.org.au/guides/generating-pgp-keys-windows
4. https://askubuntu.com/questions/186805/difference-between-pgp-and-gpg
5. https://www.linode.com/docs/security/encryption/gpg-keys-to-send-encrypted-messages/
6. https://easyengine.io/tutorials/linux/gpg-keys/
7. https://www.goanywhere.com/blog/2019/03/28/pgp-vs-gpg-whats-the-difference
8. https://www.gnupg.org/gph/en/manual/x110.html
9. https://gnupg.org/
10. https://news.bitcoin.com/how-to-encrypt-messages-with-pgp-when-using-darknet-markets/
11. https://howchoo.com/g/nddkztqzmty/how-to-send-and-receive-encrypted-messages-using-gpg
