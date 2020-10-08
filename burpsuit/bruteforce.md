## Burpsuite Modules :
---

[![SVG Banners](https://svg-banners.vercel.app/api?type=origin&text1=Bruteforce%20Attack%20🤠&text2=Using%20Burpsuite%20💖&width=800&height=400)](https://github.com/Akshay090/svg-banners)

## Bruteforce :


### Step 1

Intercept the the request while entering wrong username and password into the login filed.To check the request which will be made and the errror message.


![Entering username and password](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/1.png)

![Intercepting using burp](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/2.png)
![cpoy the error message](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/3.png)

### Step 2

Now sent that request to the intruder.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/4.png)

### Step 3

In intruder tab there will be 4 tabs first one will be target tab in which target will be already set.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/5.png)


### Step 4

In position tab we need to select the attack position where we'll supply the wordlist

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/6.png)

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/7.png)


we need to now select the attack type to `clusterbomb`

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/7.2.png)
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/10.png)


### Step 5

Now in the Payloads tab we'll add the simple wordlist by adding one by one ,else we can provide a list file containing all the payloads.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/9.png)
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/11.png)
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/12.png)


### Step 6

Now we'll clear the Grep -Match section then will provide the cpoied error message from the step-1.
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/13.png)

### Step 7

Then we'll start the attack

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/attack.png)

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/15.png)


### Step 8

By analyzing the length of the request we'll indentify the success of the bruteforce attack.
![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/burpsuit/images/16.png)
