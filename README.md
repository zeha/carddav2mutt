make-aliases
============

This hack exports Contacts from a CardDAV server and writes a mutt aliases
file.

To use:

echo 'machine contacts.icloud.com login sjobs@me.com password APPLE' >> ~/.netrc
./make-aliases

If you have a NICKNAME in your vCards, this will become the alias. Else, the
local part of the email address is used.

CAVEATS
-------

1. This is a hack.
2. You must have curl installed.
3. Only tested with iCloud.
4. As no XML parser is used, changes in server replies will break this.
5. No dupe checking for aliases.
