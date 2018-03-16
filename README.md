The following rule should be followed for each cloud directory.

incr
====
Allow `rsync` sync/write to this folder. Once a file is thrown into this
folder, you usually do not want to modify it, if necessary, modify/delete
files only through WEB interface. `rsync` should be specified to sync files
incrementally to this folder.

proj
====
Web service projects, usually Git managed. And master code is also managed
here. Other than saving code (instead of relying on third-party git hosting
service such as Github), the benefits to collect all code here also include
automatically update code repo easily (because they are all in one place).
But data here are pushed to Github and thus very likely to be public.

sync
====
This file is mirror of usually the Desktop folder of client, to keep a backup
of recent files in one place. This desktop files are typically not ready
to be moved to `incr` folder or you do not have time to organize them into
`incr` folder yet. Do not write to `sync` from WEB interface, doing so will
cause data lost the next time you client synchronizes to master.
