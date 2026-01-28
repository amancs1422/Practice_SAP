## Step 1 : Pre-Checks
Check the current kernel version and also perform PAM verification.
```
disp + work --version
```
## Step 2 : Download the kernel files.
## Step 3 : Prepare new kernel directory.
```
mkdir <dir_path>
cd <dir_path>
```
## Step 4 : Uncar the kernel files.
```
SAPCAR -xvf SAPEXE<new_release><patch_level>.SAR
SAPCAR -xvf SAPEXEDB<new_release><patch_level>.SAR
```
## Step 5 : Change ownership and permissions.
```
chown -R <sid>adm:sapsys *
chmod -R 755 *
```
## Step 6 : Stop the application and make sure no SAP processes are running.
```
stopsap r3
ps -ef | grep <sid>adm
```
## Step 7 : Take a backup of existing kernel.
```
cd /sapmnt/<sid>
cp -Rp exe exe_old
```
## Step 7 : Replace kernel executables.
```
cp -Rp * /sapmnt/<sid>/exe/uc/linuxx86_64
```
## Step 8 : Run saproot.sh script.
```
sudo su -
./saproot.sh
```
## Step 9 : Start the applications.
```
startsap r3
```
## Step 10 : Check kernel version.
```
disp + work
```


-AK