#  Phishing expert level 
Can you manage to phish CTFkom?

Email client: http://129.241.150.108:8001/

Admin login page: http://129.241.150.108:8000/

The admin checks and interacts with all the links in the mail.

This level I have integreted an AI that looks for suspicious emails and denies them. Can you find a workaround?

## Solution:
The site is offline now so i cant access it but the premise was the exact same as before except this time there was a AI bot which checked whether the mail was real or not.

It did this by checking how legitemate it looked. For example if you used a webhook link it would tell you that it looked very suspicious.

The trick i used was to use tinyurl.com. Along with that i created a realistic email.

After this the AI bot visits the url and as before you get a request in Webhook.site with the username and password.
