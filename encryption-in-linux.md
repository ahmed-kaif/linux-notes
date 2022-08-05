# Encrypt Files using passphrase protection

To encrypt files using a password, use the “gpg” command with the “-c” option specifying that you want to use a symmetric encryption for your file. After that, specify the name of the file that you want to encrypt.
**The “gpg” command will create a file with a “.gpg” extension which is the encrypted file that you want to store.**

```sh
$ gpg -c <file>
```

## Decrypt Encrypted File on Linux

```sh
$ gpg -d <file>.gpg
```

# Encrypt Directory using gpg

To create an archive, use the “tar” command along with the “-cvf” options that stand for “create a file in verbose mode”. Now that your archive is created, you can encrypt it using the “gpg” command with the “-c” option.

```sh
$ tar -cvf archive.tar <directory>

$ gpg -c archive.tar
```

# Encrypt Directory using zip

```sh
$ zip -r --encrypt secure.zip <directory>

$ zip --encrypt secure.zip <file>...<file10>
```

# Encrypt Files using private key (Efficient Way) [RSA Recommended]

To encrypt files on Linux using a private key, you have to execute the “gpg” command with the “–full-gen-key” option. You have multiple options for key generation (such as “–quick-generate-key”) but the full one gives you more options.

```sh
$ gpg --full-gen-key
```
To encrypt your file using your created key, you have to use the “gpg” command with the “-e” option for “encrypt” and specify the key to be used with the “–recipient” option.

```sh
$ gpg -e --recipient <email or name> <file>
```

## Decrypt File using key

```sh
$ gpg -d <file>.gpg
```

### Useful Links:

- [How To Encrypt File on Linux](https://devconnected.com/how-to-encrypt-file-on-linux/)
- [5 Best ways to encrypt files in Linux](https://www.fosslinux.com/27018/best-ways-to-encrypt-files-in-linux.htm)


