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
* nodejs (tested with 12.22)
* (coreutils).

### usage
To execute the script give it execute right.  
`chmod +x badown`
  
To download a file:  
`./badown 'https://mega.nz/#F!NogxFaIK!PavsMkUPQSXJ_o5zwCs5Ew'`  
`./badown 'https://mega.nz/folder/NogxFaIK#PavsMkUPQSXJ_o5zwCs5Ew'`  
`./badown 'https://mega.nz/#!RnQFkTYS!rFIJp7MBKxcS-Po8okSSoykR17KpIGV7xcXNZvpx38I'`  
`./badown 'https://mega.nz/file/RnQFkTYS#rFIJp7MBKxcS-Po8okSSoykR17KpIGV7xcXNZvpx38I'`  
`./badown 'https://www.mediafire.com/file/jbbbncd27n5mukh/test.zip'`  
`./badown 'https://www74.zippyshare.com/v/WjE4KUUF/file.html'`  
Those links might be dead for inactivity, however they will stay here for the syntax.  
  
To download from a file with a lot of urls just use a loop for:  
`for i in $(cat urls); do ./badown $i && sleep .5; done`  

### todo
- Add more sites and resume paused download.  
- Extend mega function with specific file in folder download.  
- Add proxy support, else as an option or as a function with automatic grabber.  
