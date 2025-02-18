# Janus Code Distribution

Janus Code Distribution can be started from a CDROM or an USB stick on a computer and being used to sign secure transactions. The Janus Code Distribution is the equivalent of the mobile version of [Janus Code](https://github.com/januscod/januscode), use the mobile app [Janus Code Wallet](https://github.com/januscod/Janus-Code-Wallet) to broadcast transactions.

## Setup Janus Code Distribution
### Copy Janus Code Distribution to a CDROM or USB stick

**CDROM:**  
use your favorite program to burn the ISO to CDROM.
Nothing special. CDROMs are naturally read-only and tamper resistant.

**USB:**  
If you don't burn Janus to a CDROM, writing Janus Code to a
USB stick with a hardware read-write toggle (e.g., Kanguru FlashBlu) is
the next best thing.

On USB sticks without write protection, you can remove the Janus Code USB after
booting as an additional security measure. Janus loads into RAM so
after booting you no longer need the USB.

1) Insert USB stick and detect the device path::
```
$ dmesg|grep Attached | tail --lines=1
[583494.891574] sd 19:0:0:0: [sdf] Attached SCSI removable disk
```
2) Write ISO to USB::
```
$ lsblk | grep sdf
sdf                                8:80   1   7.4G  1 disk  
└─sdf1                             8:81   1   444M  1 part 
```

### How to build from source

Janus is built with `Vagrant`

1) Install Vagrant

```
```

## How to create and sign transactions

1) Import your mnemonic phrase or generate a new one
2) Add a new wallet ex. Ethereum with the standard or your desired derivation path
3) Sync the wallet address over QR with your Janus Wallet app
4) Create a new transaction within the Janus Wallet app
5) Scan the transaction QR code with the Janus Code Distribution
6) Sign the transaction within Janus Code Distribution
7) Scan the signed transaction QR code with Janus Wallet
8) Confirm and broadcast the transaction with Janus Wallet

## Credits

This project was inspired by BitKey. The distribution as well as this readme have been created based on their work.
