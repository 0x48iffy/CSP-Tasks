## Firmware-Analysis :
---

### Step 1 :

We need to first Download the firmware which we want to analyze further. Then we need the extract the file system using ```binwalk```.

Command : 
```bash
$ binwalk -e <name of the firmware>
```
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/1.png)


### Step 2:

After extracting we need to go to the newly created extracted folder where the file system of the firmware situated. We will get  `squafs`file system.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/2.png)


### Step 3:

Then after explore the squafs file system
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/3.png)

### Step 4:

Find out "telnet" service as this will lead us to the credentials using ``grep`` command:

```bash
$ grep -iRn "telnet"
```

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/4.png)

### Step 5:

After running the above command we have got an script named `telnetd.sh` , let's check out the script.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/5.png)

### Step 6:
Now check the script file content using `cat` command:

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/6.png)

### Step 7:

From the telnetd.sh script we have got a username and also a password filed but by understaing the script we have got that password is fetched from another filed from a location in the file system now get that:
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/firmware/photo/7.png)


Yayyyy! Got the username and password of the firmware.
