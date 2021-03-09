# Instalasi NVM agar mudah menggunakan versi node
```
[lenovothinkpad ~]# pacman -Sy nvm
:: Synchronizing package databases...
 core is up to date
 extra is up to date
 community is up to date
 multilib is up to date
resolving dependencies...
looking for conflicting packages...

Packages (1) nvm-0.37.2-1

Total Download Size:   0,03 MiB
Total Installed Size:  0,13 MiB

:: Proceed with installation? [Y/n] Y
:: Retrieving packages...
 nvm-0.37.2-1-any                                                          29,4 KiB   640 KiB/s 00:00 [############################################################] 100%
(1/1) checking keys in keyring                                                                        [############################################################] 100%
(1/1) checking package integrity                                                                      [############################################################] 100%
(1/1) loading package files                                                                           [############################################################] 100%
(1/1) checking for file conflicts                                                                     [############################################################] 100%
(1/1) checking available disk space                                                                   [############################################################] 100%
:: Processing package changes...
(1/1) installing nvm                                                                                  [############################################################] 100%

You need to source nvm before you can use it. Do one of the following
or similar depending on your shell (and then restart your shell):

  echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc
  echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.zshrc

You can now install node.js versions (e.g. nvm install 10) and
activate them (e.g. nvm use 10).

init-nvm.sh is a convenience script which does the following:

[ -z "$NVM_DIR" ] && export NVM_DIR="$HOME/.nvm"
source /usr/share/nvm/nvm.sh
source /usr/share/nvm/bash_completion
source /usr/share/nvm/install-nvm-exec

You may wish to customize and put these lines directly in your
.bashrc (or similar) if, for example, you would like an NVM_DIR
other than ~/.nvm or you don't want bash completion.

See the nvm readme for more information: https://github.com/creationix/nvm

Optional dependencies for nvm
    bash: bash completion [installed]
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
```