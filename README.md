pesterupdate is a command line tool designed to be placed at the end of a .bashrc to remind the user to run pacman -Syu

pesterupdate does not automatically perform any updgrades or see which specific packages need updating (if any). However, as Arch is a rolling release, there's likely something to do at least once a day.
by default, the command checks to see when the last update was by reading reading the pacman log at /var/log/pacman.log.

command line arguments exist to modify function and output as desired
```
-t set a time (in seconds) as the desired maximum update
-f specify a path to an alternate pacman log
-y decide when the last 'update' was based on the last sync (pacman -Sy). default behavior is -yu
-u decide when the last 'update' was based on the last upgrade (pacman -Su). default behavior is -yu
-p print an all clear if it has been less then the desired time since an update
```

TODO: format into package, more options
