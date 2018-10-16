# badown
The name is a short for bash-downloader.
This script can download files from mediafire, zippyshare & mega (file & folder).
It fully support folder download on mega.
Futhermore, you can control the bandwidth with the option, `-s 70K` or `--speed 1M`.

### dependencies
It requires:
* bash (tested with 4.4), 
* wget (tested with 1.19), 
* gzip (tested with 1.8),
* awk  (tested with 4.1),
* openssl aes-128-(cbc, ecb & ctr)
* (coreutils).

### usage
To execute the script give it execute right.  
`chmod +x badown`
  
To download a file:  
`./badown 'https://mega.nz/#F!NogxFaIK!PavsMkUPQSXJ_o5zwCs5Ew'`  
`./badown 'https://mega.nz/#!RnQFkTYS!rFIJp7MBKxcS-Po8okSSoykR17KpIGV7xcXNZvpx38I'`  
`./badown 'https://www.mediafire.com/file/jbbbncd27n5mukh/test.zip'`  
`./badown 'http://www49.zippyshare.com/v/OSZ5J7so/file.html'`  
Those links refer to the same zipped test folder.
It is unziped for the first link.  
  
To download from a file with a lot of urls just use a loop for:  
`for i in $(cat urls); do ./badown $i && sleep .5; done`  

### todo
Add more sites (if asked) and resume paused download.
