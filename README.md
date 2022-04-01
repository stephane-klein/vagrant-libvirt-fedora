# Install Vagrant + libvirt provider on Fedora

## Prepare your computer

```
$ sudo dnf install vagrant libvirt
$ vagrant plugin install vagrant-libvirt
$ sudo systemctl start libvirtd
$ sudo usermod -aG libvirt $USER
```

Open a new terminal.

## Troubleshooting

If you have this error:

```sh
$ vagrant up
Bringing machine 'default' up with 'libvirt' provider...
==> default: Checking if box 'fedora/35-cloud-base' version '35.20211026.0' is up to date...
Error while activating network: Call to virNetworkCreate failed: internal error: Network is already in use by interface vboxnet2.    
```

Execute:

```
$ VBoxManage hostonlyif remove vboxnet2 
```

## Start and enter in guest VM

```sh
$ vagrant up
$ vagrant ssh
```

