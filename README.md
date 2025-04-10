## netcopy :  Untility to upload/download files/folders over ssh without password

    This utility is used to upload files/folders to a remote server over ssh, without password.

    Note: netcopy is based on openssh. To use this utility, openssh service should be enabled in the remote server.

### How to install this package?

    1. chmod +x install.sh
    2. sudo ./install.sh

### How to use this utility?

#### Step 1: Enable ( configure ) uploader

    $netcopy  -e <username>@<domain/ip_address>
    
#### Example
    
    $netcopy -e  testuser@192.168.1.10
    
    -> Feed the remote server password 

#### Step 2: Upload files/folders to remote server without password 

    $netcopy <local file/folder>  <username>@<domain/ip_address>/<remote_server_path>
    
##### Example
    
    $netcopy test.txt testuser@192.168.1.10/home/ubuntu/
    
    -> with this command, a file named "test.txt" will be copied to "/home/ubuntu/" on server 192.168.1.10

#### Step 3: Download files/folders from remote server without password 

    $netcopy  <username>@<domain/ip_address>/<remote_server_path> <local file/folder> 
    
##### Example
    
    $netcopy testuser@192.168.1.10/home/ubuntu/test.txt /home/
    
    -> with this command, a file on remote server named "/home/ubuntu/test.txt" will be copied to "/home/" on the local machine


#### Step 4: Disable uploader ( After this command you can upload files to remote server )

    $netcopy  -d <username>@<domain/ip_address>
    
##### Example
    
    $netcopy  -d testuser@192.168.1.10
 

### Tested Systems

    - Ubuntu
    - Mac OSX
