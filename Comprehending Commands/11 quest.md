# An Epic Filesystem Quest
The challenge asks us to follow a chain of clues scattered around the filesystem by using ls, cat, and cd as directed. Start at /, read the first hint file, then keep following each clue (some hidden, some delayed, some trapped) until you locate the final file containing the flag.

***

## My solve
**Flag:** `pwn.college{oFkzX_Fe2XuuLbMuqnsmchR65Lg.QX5IDO0wCNzEzNzEzW}`

I started at /, listed and read the clue files, followed the clues through many directories (using ls -a to reveal dotfiles, cd when a clue became readable only after entering a directory(delayed) and avoided cd when a clue warned it would self-destruct if entered(trapped)). I kept following the clues and finally found the flag after a few steps.
```
hacker@commands~an-epic-filesystem-quest:~$ ls / -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  WHISPER     boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:~$ cat /WHISPER
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/video/fbdev/mmp/hw

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/linux/linux-5.4/drivers/video/fbdev/mmp/hw
Kconfig  Makefile  mmp_ctrl.c  mmp_ctrl.h  mmp_spi.c
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/linux/linux-5.4/drivers/video/fbdev/mmp/hw -a
.  ..  .MESSAGE  Kconfig  Makefile  mmp_ctrl.c  mmp_ctrl.h  mmp_spi.c
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/linux/linux-5.4/drivers/video/fbdev/mmp/hw/.MESSAGE
Tubular find!
The next clue is in: /opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:~$ cd /opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ ls -a
.    Makefile        clock-sh7706.c  clock-sh7712.c  pinmux-sh7720.c  serial-sh7710.c  setup-sh7705.c  setup-sh7720.c
..   clock-sh3.c     clock-sh7709.c  entry.S         probe.c          serial-sh7720.c  setup-sh770x.c  swsusp.S
CUE  clock-sh7705.c  clock-sh7710.c  ex.S            serial-sh770x.c  setup-sh3.c      setup-sh7710.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ cat ./CUE
Lucky listing!
The next clue is in: /usr/share/javascript/mathjax/fonts/HTML-CSS/TeX

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ ls /usr/share/javascript/mathjax/fonts/HTML-CSS/TeX
MEMO-TRAPPED  otf  svg  woff
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ cat /usr/share/javascript/mathjax/fonts/HTML-CSS/TeX/MEMO-TRAPPED
Tubular find!
The next clue is in: /usr/lib/R/library/translations/en/LC_MESSAGES

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ ls /usr/lib/R/library/translations/en/LC_MESSAGES
R.mo  TIP-TRAPPED
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ cat /usr/lib/R/library/translations/en/LC_MESSAGES/TIP-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/htdp-lib/lang/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/kernel/cpu/sh3$ cd /usr/share/racket/pkgs/htdp-lib/lang/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/lang/compiled$ ls
INFO                                     htdp-intermediate-lambda_rkt.dep     info_rkt.zo
error_rkt.dep                            htdp-intermediate-lambda_rkt.zo      plt-pretty-big-text_rkt.dep
error_rkt.zo                             htdp-intermediate-reader_rkt.dep     plt-pretty-big-text_rkt.zo
htdp-advanced-reader_rkt.dep             htdp-intermediate-reader_rkt.zo      plt-pretty-big_rkt.dep
htdp-advanced-reader_rkt.zo              htdp-intermediate_rkt.dep            plt-pretty-big_rkt.zo
htdp-advanced_rkt.dep                    htdp-intermediate_rkt.zo             posn_rkt.dep
htdp-advanced_rkt.zo                     htdp-langs-interface_rkt.dep         posn_rkt.zo
htdp-beginner-abbr-reader_rkt.dep        htdp-langs-interface_rkt.zo          prim_rkt.dep
htdp-beginner-abbr-reader_rkt.zo         htdp-langs-save-file-prefix_rkt.dep  prim_rkt.zo
htdp-beginner-abbr_rkt.dep               htdp-langs-save-file-prefix_rkt.zo   r5rs_rkt.dep
htdp-beginner-abbr_rkt.zo                htdp-langs_rkt.dep                   r5rs_rkt.zo
htdp-beginner-reader_rkt.dep             htdp-langs_rkt.zo                    run-teaching-program_rkt.dep
htdp-beginner-reader_rkt.zo              htdp-reader_rkt.dep                  run-teaching-program_rkt.zo
htdp-beginner_rkt.dep                    htdp-reader_rkt.zo                   stepper-language-interface_rkt.dep
htdp-beginner_rkt.zo                     imageeq_rkt.dep                      stepper-language-interface_rkt.zo
htdp-intermediate-lambda-reader_rkt.dep  imageeq_rkt.zo
htdp-intermediate-lambda-reader_rkt.zo   info_rkt.dep
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/lang/compiled$ cat ./INFO
Yahaha, you found me!
The next clue is in: /usr/lib/firefox/browser/chrome/icons
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/lang/compiled$ ls /usr/lib/firefox/browser/chrome/icons -a
.  ..  SPOILER  default
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/lang/compiled$ cat /usr/lib/firefox/browser/chrome/icons/SPOILER
Yahaha, you found me!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl-base/IPC

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/lang/compiled$ cd /usr/lib/x86_64-linux-gnu/perl-base/IPC
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl-base/IPC$ ls -a
.  ..  Open2.pm  Open3.pm  REVELATION
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl-base/IPC$ cat ./REVELATION
Yahaha, you found me!
The next clue is in: /usr/share/help/el/gedit/figures
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl-base/IPC$ ls /usr/share/help/el/gedit/figures -a
.  ..  TEASER  gedit-html-snippet.png  gedit-icon.png  gedit3-screenshot.png
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl-base/IPC$ cat /usr/share/help/el/gedit/figures/TEASER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{oFkzX_Fe2XuuLbMuqnsmchR65Lg.QX5IDO0wCNzEzNzEzW}
```

***

## What I learned
learned how to combine ls, cat, and cd to follow clues across the filesystem. I also learned that some files can only be accesed if your working directory is the same as the one the file is in and some files can be destroyed if you cd into their directory.
***

## References 
*No references used*