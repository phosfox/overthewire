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

## Bandit Level 13
* move data.txt to your tmp folder
* xxd -r data.txt out.gz
* gzip -d out.gz
* bzip2 -d out
* mv out.out out.gz
* gzip -d out.gz
* mv out out.tar
* tar-xvf out.tar
* tar-xvf data5.bin 
* bzip2 -d data6.bin
* tar -xvf data6.bin.out
* mv data8.bin data8.gz
* gzip -d data8.gz
* cat data8 -> 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

## Bandit Level 14
* ssh bandit14@localhost -i sshkey.private
* cat /etc/bandit_pass/bandit14 -> 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

## Bandit Level 15
* on bandit14
* telnet localhost 30000
* passw from lvl14 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
* -> BfMYroe26WYalil77FoDi9qh59eK5xNr

## Bandit Level 16
* ssh bandit@bandit.labs.overthewire.org
* openssl s_client -connect localhost:30001 paste in the password from 15
* -> cluFn7wTiGryunymYOu4RcffSxQluehd

## Bandit Level 17
* nmnap -p31000-32000 
* openssl s_client -connect localhost:31790
* paste the password from 16
* save the RSA key 
* ssh -i bandit17.key bandit17@localhost

## Bandit Level 18
* start with 17 for this, you need the bandit17 shell
* diff password.new password.old
* first entry is the pw for the next level
* kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
* 
