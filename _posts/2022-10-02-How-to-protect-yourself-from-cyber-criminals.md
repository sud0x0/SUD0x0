---
layout: post
date: 2022-10-02
title: How to protect yourself from cyber criminals
image: /images/article-2.jpeg]
excerpt: "I thought it would be a good idea to write an article about the methods that an individual should take to avoid cyber attacks. This is an extensive list of tasks, and this list is based on my view as a penetration tester. For example, what I look at when I have to conduct a social engineering attack, what I would focus on to attack a particular target, etc."
Keywords: cyber criminals, cyber security, cybercrime, cyber safe
---

<img class="blog-main-image" src="https://sud0x0.com/images/article-2.jpeg">
<p style="font-size:12px"><a href="https://www.pexels.com/photo/man-wearing-karategi-standing-on-grass-5968798/" target="_blankl">Photo by Parcerografo.</a></p>

<br>

***

<font color="red">If you are reading this article to figure out the immediate responses that you need to take to minimise the potential damage of the Optus data breach, I recommend you stop reading this article and follow the articles below.</font> [OAIC](https://www.oaic.gov.au/updates/news-and-media/advice-on-optus-data-breach)[ACSC](https://www.cyber.gov.au/acsc/view-all-content/alerts/optus-notifies-customers-cyberattack-compromising-customer-information)

***

<br>

This is an extensive list of tasks that I believe are necessary to perform to secure ourselves from cyber criminals. This is based on my view as a penetration tester. For example, what I look at when I have to conduct a social engineering attack, what I would focus on to attack a particular target, etc. This article has three main parts.
-  How to prepare your tools and environments?
-  Day-to-day activities
-  What to do if you are a victim of a cyber-attack?

For most of the steps I recommend, you do not need to have a high level of computer science, programming, computer networking, or cyber security knowledge.

Even though I mentioned a couple of brands, services, and vendors in this article, I do not recommend you use them based on my advice. In this article, I use them as examples. It is your responsibility to find the best brands, services, and vendors that suit you. Understand the concept and research more.  Also, you do not have to follow all the steps. Choose what suits you on your own account.

Although I tried to cover all the important areas, please be aware that I may have missed some.

<br>

## How to prepare your tools and environments?

**Devices**

- Do not use jail-broken or rooted devices. 
There are two main issues associated with this. The OS will not receive updates unless you do it by yourself. The software you use may contain malware. Don’t do this unless you are 100% sure about every single bit of code that you must use (to jailbreak and the software that you install) and you are capable of updating it regularly when important updates are released. It is always better to have separate devices for testing purposes.

- Avoid the use of used devices. 
Someone can install a rootkit (malware type) and sell the device. Even if you reinstall the OS, the rootkit may stay as it is. In my opinion, it is always better to buy new devices when it comes to personal use, unless you are knowledgeable enough to refurbish the device properly.

- Do not use devices and apps/software without proper research. 
Some vendors have malicious intentions, such as espionage. Some seek to gain more money by gathering data unlawfully. Research the security and privacy of devices and software that you use before using them.

- Enable automatic updates. 
It is always important to keep the device up to date to avoid malicious attacks. If we do manual updating, we may miss important updates for various reasons. That’s why I believe that it is important to keep this option enabled.

- Make sure to download software from the original vendor's website. 
A person can add a malicious code to reputed software and market it on a different website. To avoid this, it is better to download software from the original vendor’s website.

- Do not use pirated software. 
How do you know that the person who made the pirated copy did not install malware on the software?

- Configure the devices and software according to a security and privacy guide. 
There are security guides for most of the devices and software that we use. Follow them. Most devices, apps, and software do not come preconfigured with 100% focus on your security and privacy. It is your responsibility to configure them based on your needs by using the available options.

- Do not use a Windows or Linux admin account. This is important to block malware attackers from getting admin access to your device. This may not always work, as if someone has low-level access to your device, they may escalate the privileges to admin by exploiting other vulnerabilities. However, this can sometimes be useful in avoiding such attacks. 

- Configure your devices to request you to enter a password before logging in. 

- Setup the BIOS/UEFI access password. 
This will prevent unauthorised access to your computer and some other physical attacks.

- Configure your devices to lock themselves if you are inactive for longer than 5 minutes. 
If your device stays unlocked once you unlock it, any person who has access to the device can view your information (5 minutes is my preference).

- Configure important apps/software to request a password before logging you in. 
Do you want someone to access apps that have your sensitive information, such as bank apps or messaging apps, if by accident they get access to your device?

- Focus on the web browser's security. 
The web browser is one of the main ways to attack your device. Choose a secure web browser and update it regularly. Use relevant software (extensions) to avoid malicious websites. Be careful when you choose extensions.

- Use malware scanning software. 
Yes, MacOS and Linux also have malware. So, it is better to use malware scanners on all platforms when necessary.

- Use a firewall on the computer. 
A properly configured firewall can protect your device from many types of attacks. Windows and MacOS come with a pre-configured firewall. Do not disable it or change it without knowing what you are doing.

- Encrypt your files and devices. (Including portable SDD and USB). 
If the device is not encrypted, malicious attackers will be able to access your data through physical attacks. Some examples are stolen items and lost USB drives.

- Use a VPN. 
I strongly believe that choosing a VPN provider that respects privacy is extremely important to enhance the security and privacy of your daily work. For example, when you connect to a network, how do you know that the network owner does not keep proxy logs and does not do security-related tasks such as deep packet inspection (DPI)? *However, VPN does not provide complete security and privacy over DPI.*

- Use a virtual machine. 
A virtual machine is a useful tool when it comes to checking suspicious websites. Make sure to use a different OS on the virtual machine. For example, if your main OS is Windows or MacOS, make the virtual machine Ubuntu. Also, install a secure browser on the virtual machine. But never log into your online accounts from the virtual machine's web browser. Never keep the virtual machine turned on and destroy it once in a while and build a new one (this can be easily done by using a clone). When you are using the virtual machine, connect the virtual machine to a VPN and use a different IP address.

- Use a Multi-Factor Authentication (MFA) app. 
SMS is mostly not encrypted. Therefore, use of an MFA app is much more secure than using SMS to receive the MFA code.

- Use a password manager. 
A password manager is a good way to organise passwords.

- Follow a minimalistic method. 
Should you instal 100 software packages if you can do your work with 25? The more complex the device is, the higher the chance of getting into a cyber-attack. Design your use cases while focusing on simplistic and minimalistic methods.

**Network**

- Use a firewall and other tools that can protect your computer network. 
Secure your network by blocking unwanted protocols and ports. Use network intrusion detection software, DNS sinkholes like Pi-Hole, and security monitoring software.

- Use a secure Wi-Fi protocol: In 2022, the most secure protocol is WPA3. But not all hardware supports WPA3. Where possible, choose WPA3 over WPA2.

- Use a strong Wi-Fi password. 
A weak password may allow your neighbour access to your network. Make sure to have a strong password with at least 15 characters that contains letters in both cases, numbers, and special characters.

- Whitelist the devices that can join the network. 
Whitelisting MAC addresses is a great way to avoid unauthorised access to the network via physical ports or Wi-Fi.

- Use a separate virtual network for IoT devices. 
Does your Roomba need to be on the same network that your computer is on? Having a virtual LAN for IoT devices can provide more security to the main network. You can also use a separate device, such as a tablet, as the master controller. Thus, you do not have to install IoT devices' apps on your personal devices.


**Online Presence**

- Use multiple email accounts. 
Use one account for personal activities (activities that include sensitive data). Do not use it when you are registering for third-party services like LinkedIn. Do not use your official email for your personal tasks. Also, divide 3rd party services into multiple levels. For example, if you want to provide your email to receive discounts when you purchase an item from a shop, it should not be the same email that you gave to LinkedIn. Do not use your birth date in your email address.

- Use multiple phone numbers. 
The same principle as with emails. The use of two phone numbers can protect you from many types of attacks.

- Use multiple bank accounts. 
This method will prevent you from suffering a major loss if you get into a cyber-attack. For example, use one account for all the payments. That account must not contain more money than the required amount. Another example is that the account that you use to receive money should not be your "savings" account.

- Setup expense locks on credit cards and bank accounts.
Expense locks can prevent criminals from taking a huge amount of money at once. This will give you time to act.

- Use services that monitor your online presence and financial activities. 
Use services that do credit score checks and email monitoring (such as Have I Been Pawned). Also, setup important accounts (such as bank accounts) to alert you when an activity happens (such as a transaction).

- Record every service that you register. 
This is a technique I use to identify sensitive information that a service has about me. In this way, if a data breach happens, I can act quickly. A spreadsheet is more than enough to have a service registry.

**Physical Access**

- Focus on the physical protection of data and devices. 
Where do you store your devices? Do you store paper-based documents such as passports in a safe location? Do you use monitoring methods such as cameras?

- Use RFID protection. 
This is still a questionable approach. However, RFID skimming is a practical attack that can be done.

- Choose proper locks. 
Some rugged looking locks are terrible at protecting you. Check this [YouTube channel](https://www.youtube.com/c/lockpickinglawyer/about) to see how insecure some locks are.

<br>

## Day-to-Day activities

**Devices**
- Do some research about the software that you want to download. 
Some vendors have malicious intentions, such as espionage. Some seek to gain more money by gathering data unlawfully. Research the security and privacy of devices and software that you want to use before using them.

- Unwanted apps or software should be removed. 
If you do not use software, do not keep it.

- Do not plug unknown devices into your computer or phone. 
The unknown devices you see can be weaponised tools belonging to a malicious attacker. If so, once you plug it in, your device will be affected.

- Avoid the use of publicly available USB cables. 
The same problem as with the unknown devices.

- Before destroying or selling hardware, wipe it clean. 
Deleting or reformatting or mostly factory resetting will not delete 100% of the data from the device. In the computer world, deleting is different than wiping. Make sure to wipe the device. If not possible, responsibly destroy it.

- Restart devices at least once a week. 
If any malware activities are happening on your device, this may break it. This is not 100% effective. But it will help you to stay secure. 

- Upgrade and update your devices and apps/software.

- Turn off unwanted services such as Bluetooth when the job is done. 
If a service such as Bluetooth or Airdrop is not needed, turn it off once the task is done.

- Store your devices in safe places. 
When you are travelling with your devices, be vigilant. 

- Immediately act if a device is lost.

**Network**

- Do not use public Wi-Fi. 
Public Wi-Fi could lead to many types of attacks, including Man-in-the-Middle attacks.

- If you must use a public Wi-Fi, make sure to verify who manages it. 
Use it only if a trusted party is providing the service.

- If you must use public Wi-Fi, use a VPN. 
A VPN can partially protect you from some of the attacks that could happen, such as Man-in-the-Middle.

- If you must use public Wi-Fi, configure the device not to auto-join. 
Auto-join can lead to unnoticed joining, which could lead to malicious attacks.

- If you must use public Wi-Fi, always restart the device as soon as you finish your task. 
This is important as, if you can interrupt a malware attack before it becomes persistent, the damage could be low.

- Do not connect to random computer networks. 
The same as Wi-Fi, but for other connection types like Bluetooth connections. 

- Do not use shared computers. 
The same as Wi-Fi.

- If you must use a shared computer, make sure to verify who manages it. 
The same as Wi-Fi.

- If you must use a shared computer, log out once done and make sure you logged out. 
This is because sometimes the log-out button may not work (or will redirect you to a different page without destroying your session). Thus, reopen the web browser and paste the link to check whether you are still logged in or not. It is good to delete the browser history if possible. Also, make sure to use incognito mode. 

<font color="purple">Please note that even if you logout and change the password of a service after using public Wi-Fi or a shared computer, malicious attackers could still get your data as some web applications do not manage user sessions properly.</font>

- If you cannot keep an eye on what they are doing, delete or wipe personal data before handing the device to someone else.
For example, if you are about to give your device for a repair, check the device for sensitive information and know what could happen if it gets into the wrong hand. Use mechanisms to safeguard sensitive information.

- Do not give your device to unauthorised or unknown people. 
Be aware of who has access to your devices. Sometimes it takes less than a minute to install malware on a device.

- Do not share your Wi-Fi password. 
This could lead to unauthorised access to the network to conduct malicious attacks.

- If you share your Wi-Fi password, make sure to change the password immediately once the task is done.

- Update passwords once a year. 
Sometimes, other people may know your passwords without your knowledge. For example, sometimes your phone pin may be exposed to other people when you are typing.


**Online Presence**

- Use strong passwords. 
Use more than 15 characters that contain letters (in both cases), numbers, and special characters. Try to use passphrases when possible. An example is ‘Optus, APIs are_Important21st!c”

- Update passwords once a year. 
Sometimes, other people may know your passwords without your knowledge. For example, a shared password.

- Do not use the same password in multiple accounts.
Repeating the same password in multiple places could lead to a major compromise if your password goes to the wrong hand.

- Use MFA if it is available. 
In my opinion, passwords are mostly useless without MFA. MFA verifies the person who uses the password. 

- Do not provide guessable answers to security questions. 
One of the best examples is, what's the name of the city where you were born? To avoid the risks associated with such questions, make sure to write something that is not correct and note it down on your password manager.

- Do not share passwords. 
Sharing passwords could lead to cyber-attacks for many reasons. How do you know that the person who received it will protect it? Do you trust that person? What sensitive information can be found on the service?

- If you share access to an account, make sure to change the credentials once done.

- Monitor your online accounts and financial accounts for unusual activities. 
Constant monitoring is important to identify malicious activities. You may be able to limit the damage if you identify attacks early.

- Use temporary emails. 
Temporary emails are the best way to avoid unwanted emails and companies learning about you. But make sure never to use temp emails to register for a service that you will use more than once or services that will hold sensitive information, including your name. An example of a temporary email is https://temp-mail.org/.

- Use an incognito browser. 
Incognito mode can protect you from some attacks, such as CSRF. Use it to check slightly suspicious links, but I would recommend the use of a virtual machine to check suspicious links.

- Logout when you finish your tasks. 
If your computer is compromised, this will prevent unauthorised access to your accounts.

- Search for your name on search engines often. 
It is always good to know what is linked to your identity online, especially if your name is unique. For example, someone may have started an account to impersonate you.

- Learn how to configure your privacy settings on online accounts that you use. 
This is important as no tool comes focused specifically on your privacy and security.

- Change your online identity as much as you can. 
Should you provide your real name on forums or social media such as Facebook? Should you provide details that can lead to the identification of your real identity? Think about the consequences before you provide your real identity.

- Do not link your online fake identity to your actual identity.

- Know the person that you are dealing with. 
This is significant because how do you know whether the person that is receiving information is trustworthy or not? Do you know the real intention of that person? Do not provide data without verifying who they are. For example, if someone calls you asking for some information by posing as if he is from your bank, do not provide the information straight away. Call them back using the real bank number, which you can find online, and provide the information if necessary.

- Limit giving sensitive information; only give what is required by law. 
This is extremely important to avoid unlawful information gathering.

- Focus on what data you provide on social media and know the consequences. 
Can someone damage your identity or harm yourself or a loved one physically or mentally based on the information you provide online?

- Check the URL. 
Optus.com is not the same as optus_the_platipus.com. When surfing the web, always be aware of where you are and where you are going.

- Check for HTTPS. 
HTTPS is extremely important to avoid another party sniffing your content and activities. If HTTPS is not in use, do not use that website.

- Search about the website before you use it. 
If you come across a link that you may think is incorrect, paste it on Google and check it. Also, you can use services such as https://www.virustotal.com (make sure not to upload sensitive files).

- Do not click links that are suspicious.

- Do not download files that are suspicious.

- Do not execute files that are suspicious.

- Do not use websites that seem suspicious.

- Use a virtual machine to check suspicious links. 

- Restart the device if you think that you accidently clicked a suspicious link. 
This is important to break the malware activity. This may not be 100% effective, but it will work sometimes.

- Use encrypted SMS (short message services). 
Normal SMS that you use is not always encrypted. Make sure not to send sensitive data through it. Use secure messaging applications instead.

- Do not use pirated content. 
As I mentioned earlier, how do you know that the person who made the pirated copy did not install malware on the content? If you really want to check the content, use a separate virtual machine that does not have an internet connection or a network connection to the host computer. This includes eBooks, PDFs, video files, and music files.

- Delete accounts if you do not use them anymore. Request to delete the data. 
If you do not use a service anymore, delete the account and the content (not deactivate). Some services provide a document that describes what data they have about you.

- Store your important data in encrypted containers. 
You can use software such as 7Zip or VeraCrypt to secure your data inside encrypted containers. In this way, the confidentiality and integrity of the data will be safe if you face a cyber-attack.

- When you are using online storage solutions, be careful and do not store sensitive information without encrypting it. 
Use encrypted containers as the cloud is someone else’s computer.

- When you are using grammar checkers, be careful and do not provide sensitive information. 
Grammar checkers store the information that you provide for further analysis, such as identifying how to improve their algorithm. It is good practise to remove sensitive information from the content before you use it. Do not use grammar checking extensions that you can install on web browsers, operating systems, and text editing programmes like MS Word.

- When you are using email, make sure that the email you receive and send is encrypted. 
Some services do not use encrypted emails. This could breach the confidentiality of the sensitive data you receive or provide if a third party is sniffing the networks that they or you use.

- Do not display your credit cards in your wallet. 
In this way, people can identify your card number quickly. Some services only ask for the card number and expiration date. They do not ask for a CVV number or try to verify the actions by sending a message.

- Temporarily lock the debit or credit cards if they are not getting used often. This could prevent access to your money if the card details are compromised. 

- Hide your PIN number from cameras and people when using them.

- Configure the devices to request a password when you are using RFID-based payment solutions such as watches and rings. 

**Analogue data**

- Store your analogue data in safe places. 
Do not leave documents such as passports and other confidential documents in insecure locations without your presence. Even if it is a partially secure location, be careful and know what could happen if these documents go to a wrong hand. For example, a workplace desk.

- When no longer needed, destroy physical copies that have your sensitive information in a secure way. 
Use techniques such as shredding.


<br>

## What to do if you are a victim of a cyber-attack?

No matter how careful you are, you might get into cyber attacks due to your own fault or others' faults, such as weak protection offered by companies.

- Know who to contact. 
It is better to know who to contact and what the procedure is in advance. This may help you to do what is right in the right way if you become a victim of a cyber-attack.

- Act proactively. 
Swift actions may protect you from greater damage. 

- Contact the relevant authorities regardless of feelings. 
Some scenarios could be embarrassing events for the victim. But make sure to get advice from the relevant authorities, such as police, regardless of how you feel, as the damage could be much greater in the future if you do not act at the beginning.

- Trust the authority that is responsible for taking actions, not your friendly advisers. 
There will be people (cyber security related or not) to help you if you become a victim of a cyber-attack. But how do you verify that they are recommending the right actions? Always align your actions according to the guidelines provided by the relevant authorities, such as police, banks, cyber.gov.au, etc.

<br>

Finally, it is always important to stay up to date. One of the best ways to stay up to date is by investing your time in learning the subject.

<font color="purple">Please note that, I may update this article in the future. You can find the versioning details (including changes) of this blog post on the GitHub page.</font>