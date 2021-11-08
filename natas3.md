
# Web Crawlers and robots.txt








### If the title was not a sufficient clue - read on !!

* Open the inpector window to observe the HTML code and there is a clue
```
<!-- No more information leaks!! Not even Google will find it this time... -->
```

### Background Information
* Google's search engine uses [crawlers](https://www.cloudflare.com/learning/bots/what-is-a-web-crawler/#:~:text=A%20web%20crawler%2C%20or%20spider,appear%20in%20search%20engine%20results.) to find out about any new webpages on a particular website related to a particular topic. 
*  [Googlebot](https://blog.seoprofiler.com/googles-web-crawler-googlebot/#:~:text=Googlebot%20is%20the%20name%20of,Internet%20for%20new%20web%20pages.&text=Google%20and%20other%20search%20engines,has%20its%20own%20web%20crawler.) is google's web crawler. 
* If you as the website owner decide that you want a some resouces not be shown on Google searches, then you would use [robots.txt](https://developers.google.com/search/docs/advanced/robots/intro) file and mention the resources you do not want the crawler to find.  

### Finding password 4
* On the robots.txt file you should see 
```
   User-agent: *
   Disallow: /s3cr3t/
```
which means that the crawler should not query for this path on the server. 

* But nothing prevents us from going through that directory by directly entering that in the URL 

```http://natas3.natas.labs.overthewire.org/s3cr3t/```

* Password is in users.txt

### Why it worked!!

* Not allowing crawlers to find the page/directory does not prevent others from knowing about the existence of such a file/folder.

* Bad way to protect secrets from rogue bots (crawlers).

    [Rogue bots](https://www.willmaster.com/library/security/one-way-robots.txt-can-be-a-security-risk.php)

