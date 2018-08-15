## Delete NODEJS
### You may need to do the additional instructions as well:

```
sudo rm -rf /usr/local/{lib/node{,/.npm,_modules},bin,share/man}/{npm*,node*,man1/node*}
```

which is the equivalent of (same as above)...
```
sudo rm -rf /usr/local/bin/npm /usr/local/share/man/man1/node* /usr/local/lib/dtrace/node.d ~/.npm ~/.node-gyp 
```

or (same as above) broken down...

### To completely uninstall node + npm is to do the following:

```
go to /usr/local/lib and delete any node and node_modules
go to /usr/local/include and delete any node and node_modules directory
```

if you installed with brew install node, then run brew uninstall node in your terminal
check your Home directory for any local or lib or include folders, and delete any node or node_modules from there
```
go to /usr/local/bin and delete any node executable
```

### You may also need to do:
```
sudo rm -rf /opt/local/bin/node /opt/local/include/node /opt/local/lib/node_modules
sudo rm -rf /usr/local/bin/npm /usr/local/share/man/man1/node.1 /usr/local/lib/dtrace/node.d
```
Additionally, NVM modifies the PATH variable in $HOME/.bashrc, which must be reverted manually.

Then download nvm and follow the instructions to install node. The latest versions of node come with npm, I believe, but you can also reinstall that as well.
