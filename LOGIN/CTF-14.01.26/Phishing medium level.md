#  Phishing medium level 
Can you manage to phish CTFkom?

Email client: http://129.241.150.96:8001/

Admin login page: http://129.241.150.96:8000/

The admin checks and interacts with all the links in the mail.

This time the admin checks that the sign in actually looks legit!

## Solution:

This challenge builds upon the previous with the following: "This time the admin checks that the sign in actually looks legit!"

What this tells me is that the admin bot checks the site to make sure it is real. Knowing that, i decide to go to Admin login page and copy the source code.

<img width="587" height="64" alt="{39CC7843-7AA1-45CC-B728-BC7B5670DA11}" src="https://github.com/user-attachments/assets/628eb5a7-5062-4b03-9b58-3f9b25eab513" />

I then go into Webhook.site and write the into the Content field. \
And make sure to replace the login function here with my own:

<img width="514" height="419" alt="{88E05953-9911-4536-A2ED-B225E8F643A3}" src="https://github.com/user-attachments/assets/582c58c3-b526-4f06-8a24-2cab98aa0908" />

I then go on to compsoe the mail with the link and send it.

<img width="534" height="393" alt="{53B9B5CC-9117-48B3-96DE-BCF9957467DD}" src="https://github.com/user-attachments/assets/09b1f920-694f-4e47-93bf-d81930a26de0" />

As you can see i receive a POST request in Webhook.site with the username and password:
<img width="1528" height="667" alt="{E761FDF7-1BF9-4744-81D8-DAE67704E680}" src="https://github.com/user-attachments/assets/bb1cd252-860a-4561-bc75-62332f11eef4" />

#### username: admin
#### password: 5eccd80da44d5be7b61f75141f7545fe

Now all you need to do is go to the admin page and log in.
<img width="722" height="659" alt="{E38D93F4-4E1A-4283-BA86-8257F64A02CB}" src="https://github.com/user-attachments/assets/7f30f0e1-737f-4317-b049-fc5aad504ee5" />

#### Flag: CTFkom{4_817_h42d32_wh3n_17_ch3ck5_7h3_h7m1}


