To prevent conflicting data write, the following rule should be followed
in terms of putting files on different folders.

(Example usage of each folder is created under each folder)

incr
====
Allow `rsync` sync/write to this folder. Once a file is thrown into this
folder, you usually do not want to modify it, if necessary, modify/delete
files only through WEB interface. `rsync` should be used to sync files
incrementally to this folder in order to secure data in this folder.

proj
====
Git managed repo should be here. And master service code is also managed
here. Other than saving code (instead of relying on third-party git hosting
service such as Github), the benefits to collect all code here also include
automatically update code repo easily (because they are all in one place).
But data here are open pushed to Github and thus very likely to be public.

pub
===
The whole point of cloud is to sharing date to me whenever I can access
Internet. However, sharing data does also mean I can let other people send
me files, or send people my file for their convenience. This folder will
be opened to public/guest and be hosted by file service such as Droppy openly
or open to guest who has the account/password I have told him.

var
===
Files under this folder should **not** be written by `rsync`. Only WEB interface
should be used to modify data here. The so-called variable files are those
often written by clients from possibly different devices. Also, some private
data are not supposed to reside with Github repo in proj folder. And it is also
easier to find and backup these data when they are all in the same place. The
typical usage of this folder is editing TODO or TO-BUY list (text file).
