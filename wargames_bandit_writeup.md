# Overthewire.com Wargame Write Up

## Bandit Level 0
* just login to bandit.labs.overthewire.org:2220 via ssh with password bandit0

## Bandit Level 1
* cat readme -> shows the password for the next level
* boJ9jbbUNNfktd78OOpsqOltutMc3MY1
* use the password to login into bandit1

## Bandit Level 2
* executing ls just lists a file named "-"
* just use mktemp -d to create your temp folder
* cp - /tmp/tmp.yourfoler/dashed
* cat /tmp/tmp.yourfoler/dashed -> CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
* or just use cat ./-

## Bandit Level 3
* cat ./spaces\ in\ this\ filename -> UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
* just cat ./sp and press tab several times

## Bandit Level 4
* cat inhere
* ls -a 
* cat .hidden -> pIwrPrtPN36QITSp3EQaw936yaFoFgAB


