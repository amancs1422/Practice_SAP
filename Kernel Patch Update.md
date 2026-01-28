## Step 1 : Pre-Checks
Check the current kernel patch version.
```
disp + work --version
```
## Step 2 : Download the kernel patch files.
## Step 3 : Uncar the files.
## Step 4 : Change ownership and permissions.
```
chown -R <sid>adm:sapsys *
chmod -R 755 *
```
## Step 5 : Stop the application and make sure no SAP processes are running.
```
stopsap r3
ps -ef | grep <sid>adm
```
## Step 6 : Take a backup of kernel from the global directory.
## Step 7 : Copy the extracted kernel files to the global directory from extracted path.
## Step 8 : Check kernel version.
## Step 9 : Run saproot.sh script.
## Step 10 : Start the applications.