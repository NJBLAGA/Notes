# Password Store

## Documentation

[Pass Docs](https://www.passwordstore.org/)

## Config G.P.K

`gpg -K` Display `GPG Key`

`gpg --edit-key [key]`

`expire` Set expiration for key

`trust` Assign value to key

## Config Password Store

`pass init [GPG key]` Init `pass`

`pass git init` Init `git` rep

`pass` Displays all password saved within store

`pass insert [directory/filename]` Saves new password

`pass generate [directory/filename]` Generate and saves new password

`pass find [password]` Finds password

`pass show [directory/filename]` Displays password in `std out`

`pass show -c [directory/filename]` Copies password to clipboard

`pass edit [directory/filename]` Edit password

`pass` Allows metadata to be saved to password — `email`

`pass grep "[password phrase]"` Displays all files with phrase

`pass rm -rf [directory/filename]` Removes password within store

`pass git commands` Most `git` commands work with `pass`
