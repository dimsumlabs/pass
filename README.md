DimSumLabs Password Store
=========================

Get [pass](http://www.passwordstore.org/). You will want to get a fairly recent version, so you can make use of sub directories.

Getting Started
---------------

If you are a new user of pass, initialize your store with `pass init`

Then clone this password store into your local store:

`git clone https://github.com/dimsumlabs/pass.git ~/.password-store/dsl`


Check available passwords
-------------------------

```shell
pass ls dsl
```

Show a paswword
---------------

```shell
pass show dsl/<the rest of the password path>
```

For example, to get the doorlock password, do

```shell
pass show dsl/door.lan
```

If you are adding a new entry, please make sure to sign the commit before pushing the changes.

List encryption key owners
--------------------------

```shell
xargs --arg-file ~/.password-store/dsl/.gpg-id gpg --list-keys
```

Reencrypt passwords to new keys
-------------------------------

Edit `~/.password-store/dsl/.gpg-id` to add or remove keys.

Run

```shell
pass init -p dsl `tr '\n' ' ' < ~/.password-store/dsl/.gpg-id`
```
