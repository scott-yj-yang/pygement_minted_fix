# pygement_minted_fix

# Some Caveat about minted

Minted use a package Pygmentize. When download it either using `pip` or `brew`, we facing the issue of those formula are not copying the exec file to the `usr/local/bin` or `usr/bin` for the root bin.

Therefore, for each new system that we needs setup, first:

1. find the location of the pygmetize exec. Usually under the folder of the `/opt/homebrew/Cellar/pygments/ver_num/libexec/bin/pygmentize` if using brew. Easier way to find the exec path is `opt/homebrew/opt/pygments/bin` and right click, show original for this file.

2. Copy and paste the `pygmentize` exec to the PATH file. `usr/local/bin`.

3. Re compile see whether the issue cleared.
