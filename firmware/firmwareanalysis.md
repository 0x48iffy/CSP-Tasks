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
