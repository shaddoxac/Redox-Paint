# Redox-Paint

Here's how to compile a new binary program in Redox:

-Go to the redox source files

-Drop the rpaint folder into redox/programs

-Go to redox/Cargo.toml

-Look for the line:

"programs/userutils",

-Add the line:

"programs/rpaint", 

on the line below it.

-Go to redox/mk/userspace/mod.mk

-There's a block of target directories for binaries. Add a \ after the last one, and on the next line add:

filesystem/bin/rpaint

without a slash.

You should be able to run make then make qemu after this.

After this point u can just type rpaint into the Redox shell to open it
