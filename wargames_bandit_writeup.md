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

## Bandit Level 5
* find . -exec cat {} + -> koReBOKuIDDepwhWk7jZC0RTdopnAYKh

## Bandit Level 6
* find -size 1033c -> ./maybehere07/.file2
* password is in there -> DXjZPULLxYr17uwoI01bNLQbtFemEgo7

## Bandit Level 7
* find -size 33c -user bandit7 -group bandit6 2>/dev/null -> ./var/lib/dpkg/info/bandit7.password
* the 2>/dev/null part hides all error messages. "Permission denied" etc.
* HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

## Bandit Level 8
* cat data.txt | grep "millionth" -> cvX2JJa4CFALtqS87jk27qwqGhBM9plV

## Bandit Level 9
* cat data.txt | sort | uniq -cu -> UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
* you have to sort before uniq because uniq can only remove duplicates if they are directly successively

## Bandit Level 10
* strings data.txt | grep -E "==" -> truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
* strings - print the strings of printable characters in files.

## Bandit Level 11
* base64 -d data.txt -> IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

## Bandit Level 12
* cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' -> 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
* The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
