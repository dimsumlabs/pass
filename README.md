DimSumLabs Password Store
=========================

Get [pass](http://www.passwordstore.org/). You will want to get a fairly recent version, so you can make use of sub directoris.

Getting Started
---------------

If you are a new user of pass, initialize your store with `pass init`

Then clone this password store into your local store:

`git clone https://github.com/dimsumlabs/pass.git ~/.password-store/dsl`

Check available passwords
-------------------------
`pass ls dsl`

Show a paswword
---------------
`pass show dsl/<the rest of the password path>`

For example, to get the doorlock password, do

`pass show dsl/door.lan`


If you are adding a new entry, please make sure to sign the commit before pushing the changes.
