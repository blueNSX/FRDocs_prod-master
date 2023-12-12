Last login: Mon Dec  4 09:23:56 on console
btroutma@MacBook-Pro ~ % cd repos
btroutma@MacBook-Pro repos % https://github.com/alexander-fischer/browser-bert.git
zsh: no such file or directory: https://github.com/alexander-fischer/browser-bert.git
btroutma@MacBook-Pro repos % clone https://github.com/alexander-fischer/browser-bert.git
zsh: command not found: clone
btroutma@MacBook-Pro repos % git clone https://github.com/alexander-fischer/browser-bert.git
Cloning into 'browser-bert'...
remote: Enumerating objects: 65, done.
remote: Counting objects: 100% (65/65), done.
remote: Compressing objects: 100% (50/50), done.
remote: Total 65 (delta 12), reused 61 (delta 8), pack-reused 0
Unpacking objects: 100% (65/65), done.
btroutma@MacBook-Pro repos % ll
zsh: command not found: ll
btroutma@MacBook-Pro repos % ls
browser-bert
btroutma@MacBook-Pro repos % cd browser-bert
btroutma@MacBook-Pro browser-bert % poetry
zsh: command not found: poetry
btroutma@MacBook-Pro browser-bert % python --version 
Python 2.7.16
btroutma@MacBook-Pro browser-bert % 
btroutma@MacBook-Pro browser-bert % brew install python
zsh: command not found: brew
btroutma@MacBook-Pro browser-bert % xcode-select --install
xcode-select: note: install requested for command line developer tools
btroutma@MacBook-Pro browser-bert % zclear
zsh: command not found: zclear
btroutma@MacBook-Pro browser-bert % clear




btroutma@MacBook-Pro browser-bert % xcrun clang -v

xcode-select: note: no developer tools were found at '/Applications/Xcode.app', requesting install. Choose an option in the dialog to download the command line developer tools.
btroutma@MacBook-Pro browser-bert % /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
==> Checking for `sudo` access (which may request your password)...
Password:
==> You are using macOS 10.15.
==> We (and Apple) do not provide support for this old version.
This installation may not succeed.
After installation, you will encounter build failures with some formulae.
Please create pull requests instead of asking for help on Homebrew's GitHub,
Twitter or any other official channels. You are responsible for resolving any
issues you experience while you are running this old version.

==> This script will install:
/usr/local/bin/brew
/usr/local/share/doc/homebrew
/usr/local/share/man/man1/brew.1
/usr/local/share/zsh/site-functions/_brew
/usr/local/etc/bash_completion.d/brew
/usr/local/Homebrew
==> The following existing directories will be made group writable:
/usr/local/include
/usr/local/lib
/usr/local/share
/usr/local/lib/pkgconfig
/usr/local/share/man
/usr/local/share/man/man1
/usr/local/share/man/man3
/usr/local/share/man/man5
/usr/local/share/man/man7
==> The following existing directories will have their owner set to btroutma:
/usr/local/include
/usr/local/lib
/usr/local/share
/usr/local/lib/pkgconfig
/usr/local/share/man
/usr/local/share/man/man1
/usr/local/share/man/man3
/usr/local/share/man/man5
/usr/local/share/man/man7
==> The following existing directories will have their group set to admin:
/usr/local/include
/usr/local/lib
/usr/local/share
/usr/local/lib/pkgconfig
/usr/local/share/man
/usr/local/share/man/man1
/usr/local/share/man/man3
/usr/local/share/man/man5
/usr/local/share/man/man7
==> The following new directories will be created:
/usr/local/etc
/usr/local/sbin
/usr/local/var
/usr/local/opt
/usr/local/share/zsh
/usr/local/share/zsh/site-functions
/usr/local/var/homebrew
/usr/local/var/homebrew/linked
/usr/local/Cellar
/usr/local/Caskroom
/usr/local/Frameworks

Press RETURN/ENTER to continue or any other key to abort:
==> /usr/bin/sudo /bin/chmod u+rwx /usr/local/include /usr/local/lib /usr/local/share /usr/local/lib/pkgconfig /usr/local/share/man /usr/local/share/man/man1 /usr/local/share/man/man3 /usr/local/share/man/man5 /usr/local/share/man/man7
==> /usr/bin/sudo /bin/chmod g+rwx /usr/local/include /usr/local/lib /usr/local/share /usr/local/lib/pkgconfig /usr/local/share/man /usr/local/share/man/man1 /usr/local/share/man/man3 /usr/local/share/man/man5 /usr/local/share/man/man7
==> /usr/bin/sudo /usr/sbin/chown btroutma /usr/local/include /usr/local/lib /usr/local/share /usr/local/lib/pkgconfig /usr/local/share/man /usr/local/share/man/man1 /usr/local/share/man/man3 /usr/local/share/man/man5 /usr/local/share/man/man7
==> /usr/bin/sudo /usr/bin/chgrp admin /usr/local/include /usr/local/lib /usr/local/share /usr/local/lib/pkgconfig /usr/local/share/man /usr/local/share/man/man1 /usr/local/share/man/man3 /usr/local/share/man/man5 /usr/local/share/man/man7
==> /usr/bin/sudo /bin/mkdir -p /usr/local/etc /usr/local/sbin /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Frameworks
==> /usr/bin/sudo /bin/chmod ug=rwx /usr/local/etc /usr/local/sbin /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Frameworks
==> /usr/bin/sudo /bin/chmod go-w /usr/local/share/zsh /usr/local/share/zsh/site-functions
==> /usr/bin/sudo /usr/sbin/chown btroutma /usr/local/etc /usr/local/sbin /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Frameworks
==> /usr/bin/sudo /usr/bin/chgrp admin /usr/local/etc /usr/local/sbin /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Frameworks
==> /usr/bin/sudo /bin/mkdir -p /usr/local/Homebrew
==> /usr/bin/sudo /usr/sbin/chown -R btroutma:admin /usr/local/Homebrew
==> /usr/bin/sudo /bin/mkdir -p /Users/btroutma/Library/Caches/Homebrew
==> /usr/bin/sudo /bin/chmod g+rwx /Users/btroutma/Library/Caches/Homebrew
==> /usr/bin/sudo /usr/sbin/chown -R btroutma /Users/btroutma/Library/Caches/Homebrew
==> Downloading and installing Homebrew...
remote: Enumerating objects: 250680, done.
remote: Counting objects: 100% (461/461), done.
remote: Compressing objects: 100% (327/327), done.
remote: Total 250680 (delta 159), reused 380 (delta 116), pack-reused 250219
Receiving objects: 100% (250680/250680), 74.13 MiB | 8.82 MiB/s, done.
Resolving deltas: 100% (182717/182717), done.
From https://github.com/Homebrew/brew
 * [new branch]      dependabot/bundler/Library/Homebrew/addressable-2.8.6 -> origin/dependabot/bundler/Library/Homebrew/addressable-2.8.6
 * [new branch]      master     -> origin/master
 * [new tag]             0.1        -> 0.1
 * [new tag]             0.2        -> 0.2
 * [new tag]             0.3        -> 0.3
 * [new tag]             0.4        -> 0.4
 * [new tag]             0.5        -> 0.5
 * [new tag]             0.6        -> 0.6
 * [new tag]             0.7        -> 0.7
 * [new tag]             0.7.1      -> 0.7.1
 * [new tag]             0.8        -> 0.8
 * [new tag]             0.8.1      -> 0.8.1
 * [new tag]             0.9        -> 0.9
 * [new tag]             0.9.1      -> 0.9.1
 * [new tag]             0.9.2      -> 0.9.2
 * [new tag]             0.9.3      -> 0.9.3
 * [new tag]             0.9.4      -> 0.9.4
 * [new tag]             0.9.5      -> 0.9.5
 * [new tag]             0.9.8      -> 0.9.8
 * [new tag]             0.9.9      -> 0.9.9
 * [new tag]             1.0.0      -> 1.0.0
 * [new tag]             1.0.1      -> 1.0.1
 * [new tag]             1.0.2      -> 1.0.2
 * [new tag]             1.0.3      -> 1.0.3
 * [new tag]             1.0.4      -> 1.0.4
 * [new tag]             1.0.5      -> 1.0.5
 * [new tag]             1.0.6      -> 1.0.6
 * [new tag]             1.0.7      -> 1.0.7
 * [new tag]             1.0.8      -> 1.0.8
 * [new tag]             1.0.9      -> 1.0.9
 * [new tag]             1.1.0      -> 1.1.0
 * [new tag]             1.1.1      -> 1.1.1
 * [new tag]             1.1.10     -> 1.1.10
 * [new tag]             1.1.11     -> 1.1.11
 * [new tag]             1.1.12     -> 1.1.12
 * [new tag]             1.1.13     -> 1.1.13
 * [new tag]             1.1.2      -> 1.1.2
 * [new tag]             1.1.3      -> 1.1.3
 * [new tag]             1.1.4      -> 1.1.4
 * [new tag]             1.1.5      -> 1.1.5
 * [new tag]             1.1.6      -> 1.1.6
 * [new tag]             1.1.7      -> 1.1.7
 * [new tag]             1.1.8      -> 1.1.8
 * [new tag]             1.1.9      -> 1.1.9
 * [new tag]             1.2.0      -> 1.2.0
 * [new tag]             1.2.1      -> 1.2.1
 * [new tag]             1.2.2      -> 1.2.2
 * [new tag]             1.2.3      -> 1.2.3
 * [new tag]             1.2.4      -> 1.2.4
 * [new tag]             1.2.5      -> 1.2.5
 * [new tag]             1.2.6      -> 1.2.6
 * [new tag]             1.3.0      -> 1.3.0
 * [new tag]             1.3.1      -> 1.3.1
 * [new tag]             1.3.2      -> 1.3.2
 * [new tag]             1.3.3      -> 1.3.3
 * [new tag]             1.3.4      -> 1.3.4
 * [new tag]             1.3.5      -> 1.3.5
 * [new tag]             1.3.6      -> 1.3.6
 * [new tag]             1.3.7      -> 1.3.7
 * [new tag]             1.3.8      -> 1.3.8
 * [new tag]             1.3.9      -> 1.3.9
 * [new tag]             1.4.0      -> 1.4.0
 * [new tag]             1.4.1      -> 1.4.1
 * [new tag]             1.4.2      -> 1.4.2
 * [new tag]             1.4.3      -> 1.4.3
 * [new tag]             1.5.0      -> 1.5.0
 * [new tag]             1.5.1      -> 1.5.1
 * [new tag]             1.5.10     -> 1.5.10
 * [new tag]             1.5.11     -> 1.5.11
 * [new tag]             1.5.12     -> 1.5.12
 * [new tag]             1.5.13     -> 1.5.13
 * [new tag]             1.5.14     -> 1.5.14
 * [new tag]             1.5.2      -> 1.5.2
 * [new tag]             1.5.3      -> 1.5.3
 * [new tag]             1.5.4      -> 1.5.4
 * [new tag]             1.5.5      -> 1.5.5
 * [new tag]             1.5.6      -> 1.5.6
 * [new tag]             1.5.7      -> 1.5.7
 * [new tag]             1.5.8      -> 1.5.8
 * [new tag]             1.5.9      -> 1.5.9
 * [new tag]             1.6.0      -> 1.6.0
 * [new tag]             1.6.1      -> 1.6.1
 * [new tag]             1.6.10     -> 1.6.10
 * [new tag]             1.6.11     -> 1.6.11
 * [new tag]             1.6.12     -> 1.6.12
 * [new tag]             1.6.13     -> 1.6.13
 * [new tag]             1.6.14     -> 1.6.14
 * [new tag]             1.6.15     -> 1.6.15
 * [new tag]             1.6.16     -> 1.6.16
 * [new tag]             1.6.17     -> 1.6.17
 * [new tag]             1.6.2      -> 1.6.2
 * [new tag]             1.6.3      -> 1.6.3
 * [new tag]             1.6.4      -> 1.6.4
 * [new tag]             1.6.5      -> 1.6.5
 * [new tag]             1.6.6      -> 1.6.6
 * [new tag]             1.6.7      -> 1.6.7
 * [new tag]             1.6.8      -> 1.6.8
 * [new tag]             1.6.9      -> 1.6.9
 * [new tag]             1.7.0      -> 1.7.0
 * [new tag]             1.7.1      -> 1.7.1
 * [new tag]             1.7.2      -> 1.7.2
 * [new tag]             1.7.3      -> 1.7.3
 * [new tag]             1.7.4      -> 1.7.4
 * [new tag]             1.7.5      -> 1.7.5
 * [new tag]             1.7.6      -> 1.7.6
 * [new tag]             1.7.7      -> 1.7.7
 * [new tag]             1.8.0      -> 1.8.0
 * [new tag]             1.8.1      -> 1.8.1
 * [new tag]             1.8.2      -> 1.8.2
 * [new tag]             1.8.3      -> 1.8.3
 * [new tag]             1.8.4      -> 1.8.4
 * [new tag]             1.8.5      -> 1.8.5
 * [new tag]             1.8.6      -> 1.8.6
 * [new tag]             1.9.0      -> 1.9.0
 * [new tag]             1.9.1      -> 1.9.1
 * [new tag]             1.9.2      -> 1.9.2
 * [new tag]             1.9.3      -> 1.9.3
 * [new tag]             2.0.0      -> 2.0.0
 * [new tag]             2.0.1      -> 2.0.1
 * [new tag]             2.0.2      -> 2.0.2
 * [new tag]             2.0.3      -> 2.0.3
 * [new tag]             2.0.4      -> 2.0.4
 * [new tag]             2.0.5      -> 2.0.5
 * [new tag]             2.0.6      -> 2.0.6
 * [new tag]             2.1.0      -> 2.1.0
 * [new tag]             2.1.1      -> 2.1.1
 * [new tag]             2.1.10     -> 2.1.10
 * [new tag]             2.1.11     -> 2.1.11
 * [new tag]             2.1.12     -> 2.1.12
 * [new tag]             2.1.13     -> 2.1.13
 * [new tag]             2.1.14     -> 2.1.14
 * [new tag]             2.1.15     -> 2.1.15
 * [new tag]             2.1.16     -> 2.1.16
 * [new tag]             2.1.2      -> 2.1.2
 * [new tag]             2.1.3      -> 2.1.3
 * [new tag]             2.1.4      -> 2.1.4
 * [new tag]             2.1.5      -> 2.1.5
 * [new tag]             2.1.6      -> 2.1.6
 * [new tag]             2.1.7      -> 2.1.7
 * [new tag]             2.1.8      -> 2.1.8
 * [new tag]             2.1.9      -> 2.1.9
 * [new tag]             2.2.0      -> 2.2.0
 * [new tag]             2.2.1      -> 2.2.1
 * [new tag]             2.2.10     -> 2.2.10
 * [new tag]             2.2.11     -> 2.2.11
 * [new tag]             2.2.12     -> 2.2.12
 * [new tag]             2.2.13     -> 2.2.13
 * [new tag]             2.2.14     -> 2.2.14
 * [new tag]             2.2.15     -> 2.2.15
 * [new tag]             2.2.16     -> 2.2.16
 * [new tag]             2.2.17     -> 2.2.17
 * [new tag]             2.2.2      -> 2.2.2
 * [new tag]             2.2.3      -> 2.2.3
 * [new tag]             2.2.4      -> 2.2.4
 * [new tag]             2.2.5      -> 2.2.5
 * [new tag]             2.2.6      -> 2.2.6
 * [new tag]             2.2.7      -> 2.2.7
 * [new tag]             2.2.8      -> 2.2.8
 * [new tag]             2.2.9      -> 2.2.9
 * [new tag]             2.3.0      -> 2.3.0
 * [new tag]             2.4.0      -> 2.4.0
 * [new tag]             2.4.1      -> 2.4.1
 * [new tag]             2.4.10     -> 2.4.10
 * [new tag]             2.4.11     -> 2.4.11
 * [new tag]             2.4.12     -> 2.4.12
 * [new tag]             2.4.13     -> 2.4.13
 * [new tag]             2.4.14     -> 2.4.14
 * [new tag]             2.4.15     -> 2.4.15
 * [new tag]             2.4.16     -> 2.4.16
 * [new tag]             2.4.2      -> 2.4.2
 * [new tag]             2.4.3      -> 2.4.3
 * [new tag]             2.4.4      -> 2.4.4
 * [new tag]             2.4.5      -> 2.4.5
 * [new tag]             2.4.6      -> 2.4.6
 * [new tag]             2.4.7      -> 2.4.7
 * [new tag]             2.4.8      -> 2.4.8
 * [new tag]             2.4.9      -> 2.4.9
 * [new tag]             2.5.0      -> 2.5.0
 * [new tag]             2.5.1      -> 2.5.1
 * [new tag]             2.5.10     -> 2.5.10
 * [new tag]             2.5.11     -> 2.5.11
 * [new tag]             2.5.12     -> 2.5.12
 * [new tag]             2.5.2      -> 2.5.2
 * [new tag]             2.5.3      -> 2.5.3
 * [new tag]             2.5.4      -> 2.5.4
 * [new tag]             2.5.5      -> 2.5.5
 * [new tag]             2.5.6      -> 2.5.6
 * [new tag]             2.5.7      -> 2.5.7
 * [new tag]             2.5.8      -> 2.5.8
 * [new tag]             2.5.9      -> 2.5.9
 * [new tag]             2.6.0      -> 2.6.0
 * [new tag]             2.6.1      -> 2.6.1
 * [new tag]             2.6.2      -> 2.6.2
 * [new tag]             2.7.0      -> 2.7.0
 * [new tag]             2.7.1      -> 2.7.1
 * [new tag]             2.7.2      -> 2.7.2
 * [new tag]             2.7.3      -> 2.7.3
 * [new tag]             2.7.4      -> 2.7.4
 * [new tag]             2.7.5      -> 2.7.5
 * [new tag]             2.7.6      -> 2.7.6
 * [new tag]             2.7.7      -> 2.7.7
 * [new tag]             3.0.0      -> 3.0.0
 * [new tag]             3.0.1      -> 3.0.1
 * [new tag]             3.0.10     -> 3.0.10
 * [new tag]             3.0.11     -> 3.0.11
 * [new tag]             3.0.2      -> 3.0.2
 * [new tag]             3.0.3      -> 3.0.3
 * [new tag]             3.0.4      -> 3.0.4
 * [new tag]             3.0.5      -> 3.0.5
 * [new tag]             3.0.6      -> 3.0.6
 * [new tag]             3.0.7      -> 3.0.7
 * [new tag]             3.0.8      -> 3.0.8
 * [new tag]             3.0.9      -> 3.0.9
 * [new tag]             3.1.0      -> 3.1.0
 * [new tag]             3.1.1      -> 3.1.1
 * [new tag]             3.1.10     -> 3.1.10
 * [new tag]             3.1.11     -> 3.1.11
 * [new tag]             3.1.12     -> 3.1.12
 * [new tag]             3.1.2      -> 3.1.2
 * [new tag]             3.1.3      -> 3.1.3
 * [new tag]             3.1.4      -> 3.1.4
 * [new tag]             3.1.5      -> 3.1.5
 * [new tag]             3.1.6      -> 3.1.6
 * [new tag]             3.1.7      -> 3.1.7
 * [new tag]             3.1.8      -> 3.1.8
 * [new tag]             3.1.9      -> 3.1.9
 * [new tag]             3.2.0      -> 3.2.0
 * [new tag]             3.2.1      -> 3.2.1
 * [new tag]             3.2.10     -> 3.2.10
 * [new tag]             3.2.11     -> 3.2.11
 * [new tag]             3.2.12     -> 3.2.12
 * [new tag]             3.2.13     -> 3.2.13
 * [new tag]             3.2.14     -> 3.2.14
 * [new tag]             3.2.15     -> 3.2.15
 * [new tag]             3.2.16     -> 3.2.16
 * [new tag]             3.2.17     -> 3.2.17
 * [new tag]             3.2.2      -> 3.2.2
 * [new tag]             3.2.3      -> 3.2.3
 * [new tag]             3.2.4      -> 3.2.4
 * [new tag]             3.2.5      -> 3.2.5
 * [new tag]             3.2.6      -> 3.2.6
 * [new tag]             3.2.7      -> 3.2.7
 * [new tag]             3.2.8      -> 3.2.8
 * [new tag]             3.2.9      -> 3.2.9
 * [new tag]             3.3.0      -> 3.3.0
 * [new tag]             3.3.1      -> 3.3.1
 * [new tag]             3.3.10     -> 3.3.10
 * [new tag]             3.3.11     -> 3.3.11
 * [new tag]             3.3.12     -> 3.3.12
 * [new tag]             3.3.13     -> 3.3.13
 * [new tag]             3.3.14     -> 3.3.14
 * [new tag]             3.3.15     -> 3.3.15
 * [new tag]             3.3.16     -> 3.3.16
 * [new tag]             3.3.2      -> 3.3.2
 * [new tag]             3.3.3      -> 3.3.3
 * [new tag]             3.3.4      -> 3.3.4
 * [new tag]             3.3.5      -> 3.3.5
 * [new tag]             3.3.6      -> 3.3.6
 * [new tag]             3.3.7      -> 3.3.7
 * [new tag]             3.3.8      -> 3.3.8
 * [new tag]             3.3.9      -> 3.3.9
 * [new tag]             3.4.0      -> 3.4.0
 * [new tag]             3.4.1      -> 3.4.1
 * [new tag]             3.4.10     -> 3.4.10
 * [new tag]             3.4.11     -> 3.4.11
 * [new tag]             3.4.2      -> 3.4.2
 * [new tag]             3.4.3      -> 3.4.3
 * [new tag]             3.4.4      -> 3.4.4
 * [new tag]             3.4.5      -> 3.4.5
 * [new tag]             3.4.6      -> 3.4.6
 * [new tag]             3.4.7      -> 3.4.7
 * [new tag]             3.4.8      -> 3.4.8
 * [new tag]             3.4.9      -> 3.4.9
 * [new tag]             3.5.0      -> 3.5.0
 * [new tag]             3.5.1      -> 3.5.1
 * [new tag]             3.5.10     -> 3.5.10
 * [new tag]             3.5.2      -> 3.5.2
 * [new tag]             3.5.3      -> 3.5.3
 * [new tag]             3.5.4      -> 3.5.4
 * [new tag]             3.5.5      -> 3.5.5
 * [new tag]             3.5.6      -> 3.5.6
 * [new tag]             3.5.7      -> 3.5.7
 * [new tag]             3.5.8      -> 3.5.8
 * [new tag]             3.5.9      -> 3.5.9
 * [new tag]             3.6.0      -> 3.6.0
 * [new tag]             3.6.1      -> 3.6.1
 * [new tag]             3.6.10     -> 3.6.10
 * [new tag]             3.6.11     -> 3.6.11
 * [new tag]             3.6.12     -> 3.6.12
 * [new tag]             3.6.13     -> 3.6.13
 * [new tag]             3.6.14     -> 3.6.14
 * [new tag]             3.6.15     -> 3.6.15
 * [new tag]             3.6.16     -> 3.6.16
 * [new tag]             3.6.17     -> 3.6.17
 * [new tag]             3.6.18     -> 3.6.18
 * [new tag]             3.6.19     -> 3.6.19
 * [new tag]             3.6.2      -> 3.6.2
 * [new tag]             3.6.20     -> 3.6.20
 * [new tag]             3.6.21     -> 3.6.21
 * [new tag]             3.6.3      -> 3.6.3
 * [new tag]             3.6.4      -> 3.6.4
 * [new tag]             3.6.5      -> 3.6.5
 * [new tag]             3.6.6      -> 3.6.6
 * [new tag]             3.6.7      -> 3.6.7
 * [new tag]             3.6.8      -> 3.6.8
 * [new tag]             3.6.9      -> 3.6.9
 * [new tag]             4.0.0      -> 4.0.0
 * [new tag]             4.0.1      -> 4.0.1
 * [new tag]             4.0.10     -> 4.0.10
 * [new tag]             4.0.11     -> 4.0.11
 * [new tag]             4.0.12     -> 4.0.12
 * [new tag]             4.0.13     -> 4.0.13
 * [new tag]             4.0.14     -> 4.0.14
 * [new tag]             4.0.15     -> 4.0.15
 * [new tag]             4.0.16     -> 4.0.16
 * [new tag]             4.0.17     -> 4.0.17
 * [new tag]             4.0.18     -> 4.0.18
 * [new tag]             4.0.19     -> 4.0.19
 * [new tag]             4.0.2      -> 4.0.2
 * [new tag]             4.0.20     -> 4.0.20
 * [new tag]             4.0.21     -> 4.0.21
 * [new tag]             4.0.22     -> 4.0.22
 * [new tag]             4.0.23     -> 4.0.23
 * [new tag]             4.0.24     -> 4.0.24
 * [new tag]             4.0.25     -> 4.0.25
 * [new tag]             4.0.26     -> 4.0.26
 * [new tag]             4.0.27     -> 4.0.27
 * [new tag]             4.0.28     -> 4.0.28
 * [new tag]             4.0.3      -> 4.0.3
 * [new tag]             4.0.4      -> 4.0.4
 * [new tag]             4.0.5      -> 4.0.5
 * [new tag]             4.0.6      -> 4.0.6
 * [new tag]             4.0.7      -> 4.0.7
 * [new tag]             4.0.8      -> 4.0.8
 * [new tag]             4.0.9      -> 4.0.9
 * [new tag]             4.1.0      -> 4.1.0
 * [new tag]             4.1.1      -> 4.1.1
 * [new tag]             4.1.10     -> 4.1.10
 * [new tag]             4.1.11     -> 4.1.11
 * [new tag]             4.1.12     -> 4.1.12
 * [new tag]             4.1.13     -> 4.1.13
 * [new tag]             4.1.14     -> 4.1.14
 * [new tag]             4.1.15     -> 4.1.15
 * [new tag]             4.1.16     -> 4.1.16
 * [new tag]             4.1.17     -> 4.1.17
 * [new tag]             4.1.18     -> 4.1.18
 * [new tag]             4.1.19     -> 4.1.19
 * [new tag]             4.1.2      -> 4.1.2
 * [new tag]             4.1.20     -> 4.1.20
 * [new tag]             4.1.21     -> 4.1.21
 * [new tag]             4.1.22     -> 4.1.22
 * [new tag]             4.1.23     -> 4.1.23
 * [new tag]             4.1.24     -> 4.1.24
 * [new tag]             4.1.25     -> 4.1.25
 * [new tag]             4.1.3      -> 4.1.3
 * [new tag]             4.1.4      -> 4.1.4
 * [new tag]             4.1.5      -> 4.1.5
 * [new tag]             4.1.6      -> 4.1.6
 * [new tag]             4.1.7      -> 4.1.7
 * [new tag]             4.1.8      -> 4.1.8
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (11/11), done.
remote: Total 18 (delta 11), reused 11 (delta 11), pack-reused 7
Unpacking objects: 100% (18/18), done.
From https://github.com/Homebrew/brew
 * [new tag]             4.0.29     -> 4.0.29
 * [new tag]             4.1.9      -> 4.1.9
HEAD is now at 4c20298ea Merge pull request #16310 from EricFromCanada/dependency-warn-false
fatal: Cannot force update the current branch.
==> Downloading https://ghcr.io/v2/homebrew/portable-ruby/portable-ruby/blobs/sha256:02180ca8b8295422ae84921bcf034b7ee8ce5575488bd5e6a37a192e53cd5d34
######################################################################### 100.0%
==> Pouring portable-ruby-3.1.4.el_capitan.bottle.tar.gz
==> Installation successful!

==> Homebrew has enabled anonymous aggregate formulae and cask analytics.
Read the analytics documentation (and how to opt-out) here:
  https://docs.brew.sh/Analytics
No analytics data has been sent yet (nor will any be during this install run).

==> Homebrew is run entirely by unpaid volunteers. Please consider donating:
  https://github.com/Homebrew/brew#donations

==> Next steps:
- Run these two commands in your terminal to add Homebrew to your PATH:
    (echo; echo 'eval "$(/usr/local/bin/brew shellenv)"') >> /Users/btroutma/.zprofile
    eval "$(/usr/local/bin/brew shellenv)"
- Run brew help to get started
- Further documentation:
    https://docs.brew.sh

btroutma@MacBook-Pro browser-bert % brew -v
Homebrew 4.1.25
btroutma@MacBook-Pro browser-bert % brew install python
==> Downloading https://formulae.brew.sh/api/formula.jws.json
#=#=#                                                                          
==> Downloading https://formulae.brew.sh/api/cask.jws.json
#=#=#                                                                          
Warning: You are using macOS 10.15.
We (and Apple) do not provide support for this old version.
It is expected behaviour that some formulae will fail to build in this old version.
It is expected behaviour that Homebrew will be buggy and slow.
Do not create any issues about this on Homebrew's GitHub repositories.
Do not create any issues even if you think this message is unrelated.
Any opened issues will be immediately closed without response.
Do not ask for help from Homebrew or its maintainers on social media.
You may ask for help in Homebrew's discussions but are unlikely to receive a response.
Try to figure out the problem yourself and submit a fix as a pull request.
We will review it but may or may not accept it.

==> Fetching dependencies for python@3.11: mpdecimal, ca-certificates, openssl@3, readline, sqlite, xz and pkg-config
==> Fetching mpdecimal
==> Downloading https://ghcr.io/v2/homebrew/core/mpdecimal/manifests/2.5.1
######################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/mpdecimal/blobs/sha256:1a831442
######################################################################### 100.0%
==> Fetching ca-certificates
==> Downloading https://ghcr.io/v2/homebrew/core/ca-certificates/manifests/2023-
######################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/ca-certificates/blobs/sha256:a3
######################################################################### 100.0%
==> Fetching openssl@3
==> Downloading https://raw.githubusercontent.com/Homebrew/homebrew-core/9d3c3ba
######################################################################### 100.0%
==> Downloading https://github.com/openssl/openssl/commit/cafccb768be5b8f5c21852
######################################################################### 100.0%
==> Downloading https://www.openssl.org/source/openssl-3.2.0.tar.gz
######################################################################### 100.0%
==> Fetching readline
==> Downloading https://raw.githubusercontent.com/Homebrew/homebrew-core/9d3c3ba
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2-patches/readline82
######################################################################### 100.0%
==> Downloading https://ftp.gnu.org/gnu/readline/readline-8.2.tar.gz
######################################################################### 100.0%
==> Fetching sqlite
==> Downloading https://raw.githubusercontent.com/Homebrew/homebrew-core/9d3c3ba
######################################################################### 100.0%
==> Downloading https://www.sqlite.org/2023/sqlite-autoconf-3440200.tar.gz
######################################################################### 100.0%
==> Fetching xz
==> Downloading https://raw.githubusercontent.com/Homebrew/homebrew-core/9d3c3ba
######################################################################### 100.0%
==> Downloading https://downloads.sourceforge.net/project/lzmautils/xz-5.4.5.tar
==> Downloading from https://phoenixnap.dl.sourceforge.net/project/lzmautils/xz-
######################################################################### 100.0%
==> Fetching pkg-config
==> Downloading https://ghcr.io/v2/homebrew/core/pkg-config/manifests/0.29.2_3
######################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/pkg-config/blobs/sha256:80f141e
######################################################################### 100.0%
==> Fetching python@3.11
==> Downloading https://raw.githubusercontent.com/Homebrew/homebrew-core/9d3c3ba
######################################################################### 100.0%
==> Downloading https://raw.githubusercontent.com/Homebrew/formula-patches/6d2fb
######################################################################### 100.0%
==> Downloading https://raw.githubusercontent.com/Homebrew/formula-patches/a1618
######################################################################### 100.0%
==> Downloading https://github.com/Bo98/cpython/commit/96d015e375135e5ebc387a55e
######################################################################### 100.0%
==> Downloading https://files.pythonhosted.org/packages/c4/e6/c1ac50fe3eebb38a15
######################################################################### 100.0%
==> Downloading https://files.pythonhosted.org/packages/ef/cc/93f7213b2ab5ed383f
######################################################################### 100.0%
==> Downloading https://files.pythonhosted.org/packages/1f/7f/4da15e07ccd11c84c1
######################################################################### 100.0%
==> Downloading https://files.pythonhosted.org/packages/fb/d0/0b4c18a0b85c20233b
######################################################################### 100.0%
==> Downloading https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tgz
######################################################################### 100.0%
==> Installing dependencies for python@3.11: pkg-config, mpdecimal, ca-certificates, openssl@3, readline, sqlite and xz
==> Installing python@3.11 dependency: pkg-config
==> Downloading https://ghcr.io/v2/homebrew/core/pkg-config/manifests/0.29.2_3
Already downloaded: /Users/btroutma/Library/Caches/Homebrew/downloads/ac691fc7ab8ecffba32a837e7197101d271474a3a84cfddcc30c9fd6763ab3c6--pkg-config-0.29.2_3.bottle_manifest.json
==> Pouring pkg-config--0.29.2_3.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/pkg-config/0.29.2_3: 11 files, 623.9KB
==> Installing python@3.11 dependency: mpdecimal
==> Downloading https://ghcr.io/v2/homebrew/core/mpdecimal/manifests/2.5.1
Already downloaded: /Users/btroutma/Library/Caches/Homebrew/downloads/f367c2ee08c56b88be0662703a8e4275f8657608a268c8c44e845154b0cea543--mpdecimal-2.5.1.bottle_manifest.json
==> Pouring mpdecimal--2.5.1.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/mpdecimal/2.5.1: 71 files, 2.1MB
==> Installing python@3.11 dependency: ca-certificates
==> Downloading https://ghcr.io/v2/homebrew/core/ca-certificates/manifests/2023-
Already downloaded: /Users/btroutma/Library/Caches/Homebrew/downloads/ee5843c6049b06251f85ff5520afc763b2d62190ebee334b78115b8bebac8885--ca-certificates-2023-08-22-1.bottle_manifest.json
==> Pouring ca-certificates--2023-08-22.all.bottle.1.tar.gz
==> Regenerating CA certificate bundle from keychain, this may take a while...
🍺  /usr/local/Cellar/ca-certificates/2023-08-22: 3 files, 221.7KB
==> Installing python@3.11 dependency: openssl@3
==> Patching
==> Applying cafccb768be5b8f5c21852764f7b2863b6f5e204.patch
patching file crypto/x509/by_file.c
==> perl ./Configure --prefix=/usr/local/Cellar/openssl@3/3.2.0_1 --openssldir=/
==> make
==> make install MANDIR=/usr/local/Cellar/openssl@3/3.2.0_1/share/man MANSUFFIX=
==> make test
==> Downloading https://formulae.brew.sh/api/formula.jws.json
######################################################################### 100.0%
🍺  /usr/local/Cellar/openssl@3/3.2.0_1: 6,798 files, 32.5MB, built in 35 minutes 20 seconds
==> Installing python@3.11 dependency: readline
==> Patching
==> Applying readline82-001
patching file nls.c
patching file patchlevel
==> Applying readline82-002
patching file display.c
patching file patchlevel
==> Applying readline82-003
patching file colors.c
patching file patchlevel
==> Applying readline82-004
patching file input.c
patching file patchlevel
==> Applying readline82-005
patching file callback.c
patching file patchlevel
==> Applying readline82-006
patching file input.c
Hunk #1 succeeded at 805 (offset -7 lines).
Hunk #2 succeeded at 816 (offset -7 lines).
Hunk #3 succeeded at 895 (offset -7 lines).
Hunk #4 succeeded at 938 (offset -7 lines).
patching file patchlevel
==> Applying readline82-007
patching file display.c
Hunk #1 succeeded at 3391 (offset -3 lines).
patching file patchlevel
==> ./configure --with-curses
==> make install SHLIB_LIBS=-lcurses
🍺  /usr/local/Cellar/readline/8.2.7: 50 files, 1.7MB, built in 1 minute
==> Installing python@3.11 dependency: sqlite
==> ./configure --enable-dynamic-extensions --enable-readline --disable-editline
==> make install
🍺  /usr/local/Cellar/sqlite/3.44.2: 11 files, 4.7MB, built in 3 minutes 19 seconds
==> Installing python@3.11 dependency: xz
==> ./configure --disable-silent-rules
==> make check
==> make install
🍺  /usr/local/Cellar/xz/5.4.5: 163 files, 2.6MB, built in 1 minute 50 seconds
==> Installing python@3.11
==> Patching
==> Applying 3.11-sysconfig.diff
patching file Lib/sysconfig.py
==> Applying 3.10-distutils-scheme.diff
patching file Lib/distutils/command/install.py
==> Applying 96d015e375135e5ebc387a55ed838d00d963dc8a.patch
patching file Modules/readline.c
patching file configure
patching file configure.ac
patching file pyconfig.h.in
==> ./configure --enable-ipv6 --datarootdir=/usr/local/Cellar/python@3.11/3.11.6
==> make
==> make install PYTHONAPPSDIR=/usr/local/Cellar/python@3.11/3.11.6_1
==> make frameworkinstallextras PYTHONAPPSDIR=/usr/local/Cellar/python@3.11/3.11
==> /usr/local/Cellar/python@3.11/3.11.6_1/bin/python3.11 -m venv /private/tmp/p
==> /private/tmp/pythonA3.11-20231211-94453-ez3p14/Python-3.11.6/whl_build/bin/p
==> /private/tmp/pythonA3.11-20231211-94453-ez3p14/Python-3.11.6/whl_build/bin/p
==> /private/tmp/pythonA3.11-20231211-94453-ez3p14/Python-3.11.6/whl_build/bin/p
==> /private/tmp/pythonA3.11-20231211-94453-ez3p14/Python-3.11.6/whl_build/bin/p
==> /private/tmp/pythonA3.11-20231211-94453-ez3p14/Python-3.11.6/whl_build/bin/p
==> Downloading https://formulae.brew.sh/api/formula.jws.json
######################################################################### 100.0%
==> /usr/local/Cellar/python@3.11/3.11.6_1/bin/python3.11 -Im ensurepip
==> /usr/local/Cellar/python@3.11/3.11.6_1/bin/python3.11 -Im pip install -v --n
==> Caveats
Python has been installed as
  /usr/local/bin/python3

Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
`python3`, `python3-config`, `pip3` etc., respectively, have been installed into
  /usr/local/opt/python@3.11/libexec/bin

You can install Python packages with
  pip3 install <package>
They will install into the site-package directory
  /usr/local/lib/python3.11/site-packages

tkinter is no longer included with this formula, but it is available separately:
  brew install python-tk@3.11

gdbm (`dbm.gnu`) is no longer included in this formula, but it is available separately:
  brew install python-gdbm@3.11
`dbm.ndbm` changed database backends in Homebrew Python 3.11.
If you need to read a database from a previous Homebrew Python created via `dbm.ndbm`,
you'll need to read your database using the older version of Homebrew Python and convert to another format.
`dbm` still defaults to `dbm.gnu` when it is installed.

For more information about Homebrew and Python, see: https://docs.brew.sh/Homebrew-and-Python
==> Summary
🍺  /usr/local/Cellar/python@3.11/3.11.6_1: 8,329 files, 196.9MB, built in 21 minutes 43 seconds
==> Running `brew cleanup python@3.11`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
Removing: /Users/btroutma/Library/Caches/Homebrew/python@3.11--flit-core--3.9.0.tar.gz... (40.9KB)
Removing: /Users/btroutma/Library/Caches/Homebrew/python@3.11--patch--2164a7ba4fd7b934514e87681908bb3e36cfd28ba53511ea631c6e24aa356a21.patch... (3.0KB)
Removing: /Users/btroutma/Library/Caches/Homebrew/python@3.11--patch--8bfe417c815da4ca2c0a2457ce7ef81bc9dae310e20e4fb36235901ea4be1658.diff... (1.8KB)
Removing: /Users/btroutma/Library/Caches/Homebrew/python@3.11--patch--d1a29b3c9ecf8aecd65e1e54efc42fb1422b2f5d05cba0c747178f4ef8a69683.diff... (637B)
Removing: /Users/btroutma/Library/Caches/Homebrew/python@3.11--wheel--0.41.3.tar.gz... (96.6KB)
==> Caveats
==> python@3.11
Python has been installed as
  /usr/local/bin/python3

Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
`python3`, `python3-config`, `pip3` etc., respectively, have been installed into
  /usr/local/opt/python@3.11/libexec/bin

You can install Python packages with
  pip3 install <package>
They will install into the site-package directory
  /usr/local/lib/python3.11/site-packages

tkinter is no longer included with this formula, but it is available separately:
  brew install python-tk@3.11

gdbm (`dbm.gnu`) is no longer included in this formula, but it is available separately:
  brew install python-gdbm@3.11
`dbm.ndbm` changed database backends in Homebrew Python 3.11.
If you need to read a database from a previous Homebrew Python created via `dbm.ndbm`,
you'll need to read your database using the older version of Homebrew Python and convert to another format.
`dbm` still defaults to `dbm.gnu` when it is installed.

For more information about Homebrew and Python, see: https://docs.brew.sh/Homebrew-and-Python
btroutma@MacBook-Pro browser-bert % poetry
zsh: command not found: poetry
btroutma@MacBook-Pro browser-bert % poetry install

