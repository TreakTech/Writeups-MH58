#  Phishing baby level 
Can you manage to phish CTFkom?

Email client: http://129.241.150.52:8001/

Admin login page: http://129.241.150.52:8000/

The admin checks and interacts with all the links in the mail.

#### Hint: 
The way it works is that the bot checks links and inputs its username and password into the form and tries to login. It does not check that the URL is legit.

## Solution:
At first one might think that challenge requires you to hijack the admin bots cookie. But you need to pay attention to the title "Phising". 

The hint basically explains the entire premise "the bot checks links and inputs its username and password into the form and tries to login".\

What you need to do is give the bot a link to a site with a username and password field. It will then enter its information and try to log in.

For this we will be using https://webhook.site/. By using the edit function in the top right we can inject our payload into the Content field:

<img width="1916" height="449" alt="{D06275DE-1E1D-474C-BFBC-2B24DA4E5ABC}" src="https://github.com/user-attachments/assets/67d9adfe-50b1-4886-ba16-9c588215e56e" />
<img width="580" height="548" alt="{C9D2859B-DE9A-4C94-BB81-FD43BD98CCF7}" src="https://github.com/user-attachments/assets/8070543e-5fe1-4d3c-8dd7-2cb0e2ecfa16" />

As you can see, all i have done is made a simple login page with input fields for both username and password.\
You can also just look through the login pages source code and copy and paste it in.

Now we can compose the mail as such and send it in:

<img width="1854" height="1057" alt="{17BE620E-8271-4845-8446-7F2FA998C65D}" src="https://github.com/user-attachments/assets/2c2b507f-d887-435c-9394-63a945410fd7" />

If we now return to webhooks we can see that there has been a POST request made with the username aand password:

<img width="2245" height="963" alt="{6B7B7F15-EF60-4418-A022-18F72673FAE2}" src="https://github.com/user-attachments/assets/4a7017b9-caad-4f50-958f-1d3e38173fdd" />

Username: admin\
Password: b771611d0b5e17787bfbc226d1469e3f

Moving on to the Admin login page we can log in and get the flag:

<img width="572" height="491" alt="{B14ABB52-A2E7-4C77-ADA1-A124509B457E}" src="https://github.com/user-attachments/assets/a1795600-731e-49ad-ad62-5b7612a1efe7" />

#### Flag: CTFkom{345y_ph15h1n9_n07_h42d}

