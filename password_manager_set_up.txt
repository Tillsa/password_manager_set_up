List gpg keys

```
$ gpg --list-keys
```

If you don't have a gpg key, create one
```
$ gpg --full-generate-key
```

List the keys again and copy the key-id (second line)
```
$ gpg --list-keys
```
```
pub   rsa4096 2018-11-30 [SC]
      1A35565C9FE601446AC30BDE55238D2674A7BAD4
uid           [ultimate] Test User <test@test.com>
sub   rsa4096 2018-11-30 [E]
```

Initialize the password-store
```
$ pass init 1A35565C9FE601446AC30BDE55238D2674A7BAD4
```

Create a folder web.de that contains a file pw, where you can store the password for web.de
```
$ pass insert web.de/pw
```
Copy a password to the clipboard without showing it

```
$ pass -c web.de/pw
```

Show a password in the command line
```
$ pass web.de/pw
```

Create a random password of length 15
```
$ pass generate web.de/pw 15
```
