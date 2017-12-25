# badown
The name is a short for bash-downloader.
This little script can download files from mediafire, zippyshare & mega (file and folder).
It now support bandwidth control with the option, `-s 70K` or `--speed 1M`.

### dependencies
It requires:
* bash (tested with 4.4), 
* wget (tested with 1.19), 
* gzip (tested with 1.8),
* awk  (tested with 4.1),
* openssl aes-128-(cbc, ecb & ctr)
* (coreutils).

### usage
To execute the script give it execute access.  
`chmod +x badown`
  
To download a file:  
`./badown 'https://mega.nz/#F!NogxFaIK!PavsMkUPQSXJ_o5zwCs5Ew'`  
`./badown 'https://mega.nz/#!RnQFkTYS!rFIJp7MBKxcS-Po8okSSoykR17KpIGV7xcXNZvpx38I'`  
`./badown 'https://www.mediafire.com/file/jbbbncd27n5mukh/test.zip'`  
`./badown 'http://www65.zippyshare.com/v/xU8By34s/file.html'`  
Those links refer to the same zipped test folder.
It is unziped for the first link.  
  
To download from a file with a lot of urls just use a loop for:  
`for i in $(cat urls); do ./badown $i && sleep .5; done`  


### warning
For some reason (encryption stuff), I am not able to recover the name of the folder for mega folder links.
Which means that the tree structure of the folder is not respected.
But, all the files are downloaded in a folder named megafolder with the UNIX timestamp.

### todo
Add curl support, more site and resume paused download.
Maybe build a shell version.
