# Spam Email Analysis

![Screenshot 2024-02-08 061608](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/9ba1d0b6-0c3d-463f-9e26-ac7589a2ba7f)

## Introduction

In this project, we use Mozilla Thunderbird to analyze spam email sent to a dummy email account. In this objective, we will show:

- How to inspect email header
- Find how many hops the email address went through
- Find IP address of email sender
- Check status of email sender on Cisco Talos

## Downloading email and Uploading to Mozilla Thunderbird

![Screenshot 2024-02-08 061516](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/339cb150-9cb9-44e1-bea9-4c92876b1800)

![Screenshot 2024-02-08 061608](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/fcfb7e9b-d895-4dff-9b1b-c53acb499469)

First we download the email in a safe environment such as a virtual machine. Then we open the email via Mozilla Thunderbird. This is what the email looked like when I brought uploaded the email via Thunderbird.

## Changing the Header View

![Screenshot 2024-02-08 062406](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/bf50ab37-2b3b-4090-a70d-75e39a432b26)

I then changed the header view of the email. This gave me more detailed information on the sender, such as IP address and how many hops the email went through before coming to this address.

![Screenshot 2024-02-08 062513](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/5e6a946c-2e8a-4e76-b94c-a1df400920c7)

This show the IP address of the email. When doing a report, you want to defang the IP. This makes it so that anyone who gets the report doesn't accidentally click on a malicious link or IP address. You defang the IP address by putting brackets around each other periouds like this: 204[.]93[.]183[.]11

## Find the number of Hops

![Screenshot 2024-02-08 062756](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/054f61b8-f68c-4df1-b14e-cfd1f552ddbc)

![Screenshot 2024-02-08 062742](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/181d4433-af5d-4a45-95aa-a4ea15752407)

![Screenshot 2024-02-08 062715](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/98d66e72-e159-4c6e-a8d3-e69691bd23bc)

![Screenshot 2024-02-08 062819](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/857f3399-1cf8-4be4-930c-f345dced70f2)

In the view, you can see how many different hops an email went through to mask the original sender. In this instance, the email went through four hops. The to and from between each email gives indication and stops when it gets the email address that sent you the email.

## Additional Spam Email Examples

![Screenshot 2024-02-08 063142](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/35614b0a-7e8a-4397-875f-9cab650d27d5)

![Screenshot 2024-02-08 063358](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/322ed869-9f30-4f9a-ba0d-f1d3a0d7a0b3)

In the example above, the email went through 2 hops while in the exmaple below, the email went through 3 hops.

![Screenshot 2024-02-08 063442](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/a818e490-8282-4ec0-87b6-ab49669d6262)

![Screenshot 2024-02-08 063515](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/960b2f2a-62f5-406d-9c45-5413616614f9)

## Cisco Talos

![Screenshot 2024-02-08 063713](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/897eb907-1ccd-437d-a762-977437a79d30)

![Screenshot 2024-02-08 064535](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/e77a809d-4ffe-4c72-be4f-df4cc704ae06)

This is a program that you can use to check the integrity of the email sender. Since this is a lab setup, when checking the information on the the sender, it comes up as green. This just indicates that this sender hasn't sent very many spam email over the course of the email creation. In the example below we'll show a bad spam emailer.

![Screenshot 2024-02-08 064518](https://github.com/dagullett/Spam-Email-Analysis/assets/75142644/26b75d3a-5832-4d11-8507-64e2bb578aa3)

We can see the location of the IP address. We can also see the domain and the network owner. The other thing we can see is the reputation of the sender. We can see that the sender has a poor reputation. It also shows how many emails are sent and their spam level. This is a very useful tool.

##Conclusion

From just a lab standpoint, you can gain knowledge manually checking if the email is malicious. There are a variety of tools out there that can do this in a safe environment without having to create a virtual machine. With PhishTool, you can drag and drop emails and they will do detailed analysis. It has made doing this work much easier.

