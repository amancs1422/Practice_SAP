## Step 1 : Pre-Checks
Check the current kernel version.
```
disp + work --version
```
## Step 2 : Download the kernel patch files.
## Step 3 : Uncar the files.
```
SAPCAR -xvf SAPEXE<patch_level>.SAR
SAPCAR -xvf SAPEXEDB<patch_level>.SAR
```
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
```
cd /sapmnt/<sid>
cp -R exe exe_old
```
## Step 7 : Copy the extracted kernel files to the global directory from extracted path.
cp -pr * /sapmnt/<sid>/exe/uc/linuxx86_64
## Step 8 : Check kernel version.
```
disp + work --version
```
## Step 9 : Run saproot.sh script.
```
sudo su -
./saproot.sh
```
## Step 10 : Start the applications.
```
startsap r3
```

-AK