---
title: "Social Engineering and Reconnaisance"
date: 2021-08-04T15:01:29+01:00
---



 
Contents
1.0.	Introduction	1
2.0.	Social Engineering	2
2.1.	Technical/Practical implementation	2
2.2.	Real world example	3
2.3.	Wider security context (What does it mean in terms of security, commonality and capability?)	3
2.4.	Mitigation of the problem	4
2.5.	Social, Legal and Ethical considerations	5
3.0.	Reconnaissance	6
3.1.	Technical/Practical implementation	6
3.2.	Real world example	7
3.3.	Wider security context (What does it mean in terms of security, commonality and capability?)	8
3.4.	Mitigation of the problem	9
3.5.	Social, Legal and Ethical considerations	9
4.0.	Summary	10
References	11

 



1.0.	Introduction
This report will cover two common topics related to cyber security, reconnaissance and social engineering, both of which are in similar phases of the Ethical Hacking process, meaning that we can analyse the links and implementations of them in regards to each other.
These topics are of interest in Cyber Security as they are arguably the most important aspects of the field. They are crucial to understanding an organisation along with how it operates securely in its day-to-day operations. Therefore, by building awareness and understanding, more organisations and individuals will have the knowledge and understanding as to how to mitigate the effects of these attacks. Graylog (2020.) gives a detailed breakdown of a typical attack process, placing emphasis on the requirement of time and patience, which is integral to building a comprehensive and complete understanding of the target. By understanding how an attacker would go about performing these attacks, together with experience of dealing with the consequences of their outcomes, is crucial to the Cyber Security industry and professionals.
2.0.	Social Engineering
Social engineering has been a deep-rooted part of human culture since long before the digital age. This discipline works by using knowledge of human nature to manipulate people into divulging information that they may otherwise keep to themselves, much like a hacker would manipulate a program to exploit and gain access to system and user information. (Nathaniel S. 2018)
The biggest difference between these two methods is that it is usually easier to hack a person than a computer system, which are usually designed to stop access from unauthorised users (Simpson M. 2013: 90). One saying that demonstrates this is “Why try to crack and password, when you can simply ask for it?”. Even if you’ve got all the latest software security, physical security, defensive technologies and up to date policies and procedures, any social engineer worth his salt will be able to find a way into your organisation/network. (Fruhlinger J. 2019).
2.1.	Technical/Practical implementation

‘The art of deception’ by Mitnick (2002); demonstrates the effects of social engineering and how they work in regards to technical/practical application. Mitnick (2002: 3-8) introduces an example of when social engineering can become interwoven with technical security, stating “There’s a popular saying that a secure computer is one that’s turned off. Clever, but false; The pretexter simply talks someone into going into the office and turning the computer on”. Demonstrating that a technical resolution may be subverted by social interaction and manipulation.

Social engineering attacks come in many forms, making it tricky to understand and utilise effectively. One method of manipulation may work in one scenario, and not in another. Due to the nature of the skills, they require a social engineer to not only understand human behaviours, but also technical behaviours of computer and security systems. A high degree of confidence, charisma, tenacity and technical know-how are required to effectively use social engineering (Zorz M. 2016). If successfully done, it can allow for many different exploitative processes to be set into action.

Some of these processes could be; inserting malware on the system (such as spyware, worms, trojans, etc), system crashes/catastrophic failures, information gathering, all of which can cause many problems for the victim. In most cases a technically savvy social engineer can take full control of a victim’s system without having to even type a command. Social engineering causes many different problems for the victim of the attacks, as written in the (Hackcontrol. N.d.) article, some of these problems are loss productivity/finances, which result from having to retrain staff and pay for reparations if breaches occur, as well as the cost of recovery and the damage to the reputation of the business.

One of the most common methods of social engineering is phishing, which involves a target being contacted by someone posing as a legitimate institution, in an attempt to lure them into providing otherwise inaccessible information (Phishing. N.d.). A social engineer will use previously gathered intelligence to carefully craft a malicious payload (e.g., An email), which will contain specific information to build rapport with the target. After navigation to the malicious link address is complete, the attacker will be able to actively gather intelligence and information about the target. There are many types of phishing that require different implementations, spear phishing for example could be used to attack an organisation, here an attacker would need to gather intelligence from the staff/associates of the organisation in order to understand how they operate. (Simpson M. 2013:p.98-99)

2.2.	Real world example

Mitnick (2002)’s book, ‘The art of deception’ discusses some attacks on entry-level employees. ‘The helpful security guard’ demonstrates how an attacker can use insider knowledge and a good-natured employee to achieve a desired outcome. The attack begins by demonstrating how pretexting can be used to coerce an individual into assisting in an attack. The attacker asks a Ph.D. candidate who has an internship at the target company if she would assist him, under the pretext of writing a script for a movie about robbing a bank. She agrees, and in order to dissuade her from telling anyone, he reasons that their ideas may be stolen if she does. The attacker contacted the business indicating that he was having car troubles and could not get into the facility, this is used to make the individual receiving the call feel empathy towards; and want to help the attacker. He then promptly informs the target that he has tried to contact the supervisor, giving his details to imply they are well acquainted. By using these tactics, he will build trust and rapport with the target, ensuring compliance later on. 
The attack resulted in successful root access to the target machines. The attacker used information from the Ph.D. candidate, in addition to passive recon, to successfully manipulate the employee’s and breach the target (Mitnick. 2002. P.195-200). Using seemingly harmless information and some basic pretexting he had manipulated the employees into wanting to comply with his requests. 
A more recent and interesting example comes from an article from the wall street journal. In the article Stupp. 2019 explains how attacker(s) used AI in order to successfully mimic the voice of a chief executive, they used this to demand a fraudulent transfer of $243,000, in what cybercrime experts describe as an unusual case of artificial intelligence being used in hacking. This technology is usually referred to as deep faking. 
This example highlights how social engineering is evolving beyond basic human-to-human interactions. By using AI to create identical voice signatures/patterns of high-ranking executives and officials, attackers will be able to manipulate any number of staff/employees (Stone. 2019) and these methods have already been wreaking havoc on the business world. Attacks such as this have been done in the past, usually by editing hundreds of hours of audio samples together which achieve the required goal. Creating visual deep-fakes is a lot more difficult to do, however by utilising AI, the potential damage, popularity and ease of these attacks could see exponential growth. WebWise (n.d.) asserts the potential for deep fakes when they say “While the technology used to create deep fakes in relatively new, it is advancing quickly and it is becoming more and more difficult to check if a video is real or not.”



2.3.	Wider security context (What does it mean in terms of security, commonality and capability?)

Due to the fact that social engineering has been around since before computers, its impact within a security context is fairly well understood, although this does not mean that it is easy to mitigate. The article by Identity Experts (2017) explores the different techniques behind social engineering, covering some of the most common and easy to execute attacks, explaining what kind of thing an attacker might say and do, and how the response of the target is used to further the attacker’s goals.
The commonality of techniques like; baiting, tailgating and phishing, demonstrate that these problems are ones that cannot be easily controlled, however regular training and well-defined policies and procedures can ensure that employees will know what to look for and will have better sense for red-flags when they are presented. The capability of social engineering attacks depends heavily on human error, and how well an attacker is able to manipulate and control the individuals they are interacting with (KasperSky. n.d.). This is what makes it particularly dangerous if used effectively. 
The article by Imperva (n.d.) states ‘What makes social engineering especially dangerous is that it relies on human error, rather than vulnerabilities in software and operating systems. Mistakes made by legitimate users are much less predictable, making them harder to identify and thwart than a malware-based intrusion’. This represents one of the main issues surrounding social engineering prevention, most systems security is based on access control, meaning that any user who has the correct permissions may access the appropriate resources. This raises the question; what if someone other than the legitimate user gains control of the account? Whether it be the attacker themselves or just their influence on the legitimate user, the system will be compromised. Microsoft Security (2018: p.16) back this up in their 2018 intelligence report by writing ‘As software vendors incorporate stronger security measures into their products, it is becoming more expensive for hackers to successfully penetrate software. By contrast, it is easier and less costly to trick a user into clicking a malicious link or opening a phishing email.’.
Social engineering is one of the only areas of cyber security where the attacker can breach most network defences just by interacting with the individuals who use the system on a regular basis. If the attacker controls the actions of legitimate users then they would not be easily discovered by intrusion detection systems, and may even have access to commands they would otherwise be denied from using. 
In order to successfully access these accounts, the attacker will gather information like:
-	User Passwords
-	Security badges/keys/ID’s
-	Design specifications, source code, development documentation
-	Private and confidential employee information
-	Customer lists, sales prospects.
Using the information above and much more, any attacker could easily access a system with certified user credentials and wreak havoc on the target system, there are almost endless possibilities as to what an attacker can do with this information (Beaver, n.d.). The nature of social engineering attacks has changed the way we view security mechanisms in the cyber industry, it has also meant that we have needed to change how we apply these mechanisms, for example user access control is clearly ineffective against social engineering, as the attacker would be able to use the targets account to conduct their attacks. Winder (2018) makes this point clear in his response to the question ‘Is there a technical solution we can deploy (against social engineering)?’, he says that it is not as easy as installing product x, however he does say that good practises such as 2-factor authenticated login requirements and disabling remote access when not needed are as close to technical solutions as we can come.
2.4.	Mitigation of the problem

The level of complexity that is involved in social engineering attacks is something that most people will struggle to understand, this does not mean that there is no way of preventing them, however it does mean that businesses will be required to develop a multi-layered approach that includes staff training in addition to technical defence measures. (Ford. 2018)
Some of the methods suggested by Ford are:
-	Build a positive security culture: Staff must be aware of their security responsibilities, and report any suspicious activity immediately, free and open communication must be maintained, if an employee is afraid or reprisals, they may not divulge any information about a potential attack.
-	Learn the psychological triggers: Staff need to be informed about the common techniques used in social engineering attacks. If they sense they are being manipulated into a certain way of thinking, they will be able to stop and report it effectively.
-	Train your staff: Training is very important in mitigating these types of attacks. When an employee understands the consequences of certain actions and use the safe cyber security practises outlined by company policy, they will be less likely to fall victim to it.
-	Test the effectiveness of the training: Constant attack drills should be implemented into security policy, ensuring that staff are able to use the training they are provided, and teaching valuable experience to any new employees.
-	Implement appropriate technical measures: Training and drills are not enough to prevent an attacker from successfully gathering their intelligence. Technical security and constant monitoring of network logs needs to be a priority for any organisation looking to protect their information and staff.

In the Webinar by BetterCloud (2016.) Chris Hadnagy discusses how his team would perform external black-box tests, not knowing anything about the target company. His team would figure out the names of applications or system by asking questions to the staff inside the organisation. If a staff member let slip even the name of a department system, the attacker would be able to use this to build pretext on the next call, using this information builds trust and rapport, as the attacker would be socially engaging with the same mannerisms as the victim.
Figure 1 shows a poll made by TechRepublic (2002), shows how most people do not feel confident about their company employee’s not being manipulated by this type of attack.
2.5.	Social, Legal and Ethical considerations

Social engineering has been a social, legal and ethical talking point since before it became associated with cyber security. Due to its nature of manipulating human beings into doing things that they otherwise would not do, it has many considerations that are discussed frequently. In the CyberCrime Magazine (2020) video interview, Kevin Mitnick describes how he used pretexting to get free rides on the public transit system. As he was only young, he was unaware that this was fraud and was very open about his exploit of the transit system. This clearly demonstrates how easy it is for anyone to begin using these types of attacks, which raises concerns for how little awareness there is surrounding them. Whether a government or private organisation, it is important for social awareness to be a key security policy.
An article by Elsevier (2015) regarding the necessity for ethics in social engineering research deliberated on some of the key ethical questions regarding this field of computer security. In the section ‘Ethics (2.2)’ the article outlines ‘The IEEE code of ethics’, which shows some of the considerations that are commonly discussed, such considerations are: ‘1. To accept responsibility in making decisions consistent with the safety, health and welfare of the public… 5. To improve the understanding of technology, its appropriate application, and potential consequences… 8. To treat fairly all persons and to not engage in acts of discrimination’. These points cover only a few of the most important social, legal and ethical aspects of conducing social engineering research/exercises. The employees are to comply with accepting the responsibilities that comes from their decisions, ensuring improved awareness and understanding the dangers and to make sure they do not use their powers in any discriminatory manner.
The social, ethical and legal points that come from social engineering are weighted heavily in the ideas that the individual must understand their role and the consequences of their actions, whether it be a professional organisation, or a child messing around with transit tickets. By increasing awareness and understanding for the problems and acting in a ethically virtuous way, social engineering can become a tool for good. (Aldawood H. Alashoor T. Skinner Geoffrey. 2020.)
3.0.	Reconnaissance

When it comes to ethical hacking/penetration testing, one phase that is arguably the key to a successful attack is reconnaissance, it is the act of gaining information about our target, usually for use later on in the attack process (Harvey. 2019). Recon can usually be broken down into two types, active and passive, both of which have benefits and downsides (HackingLoops. n.d.).  Active recon is when the attacker interacts with the target. It is much faster and more accurate but has the most risk potential associated with it, an attacker could be detected by a firewall or Intrusion detection system. Passive recon does not require interaction with the target, which means that it is less likely that the attacker will be detected, however the information is not as accurate and may take longer to piece together.

3.1.	Technical/Practical implementation

In active recon, things an attacker would look for are open ports, OS specifications, services, and if there are any vulnerable applications available. They could achieve this through any number of methods, the most common are discovery, port scanning and OS fingerprinting. (HackingLoops. n.d.). 
-	Discovery: The act of discovering possible victims, this is vital to the recon process as the attacker will need to know which targets are available.

-	Port scanning: Port scanning is used on a target to discover which ports are available to attack. These can host many different types of services, which has meant there are multiple types of port scans available.

-	OS Fingerprinting: Fingerprinting will give the attacker information about the victims operating system. This is a crucial bit of information as we cannot make an attack if we do not know what system it is.
The methods used to obtain the information listed above vary depending on the attacker’s skillsets. Most attackers will tend to use tools such as Nmap (network mapper), Metasploit (pre-packaged exploits), Nikto (Web-vulnerability scanner), SQLMap (SQL database mapper), and many more. Advanced/expert attackers will be able to build their own tools to achieve these means. (Poston H. 2019)
With passive reconnaissance, the attacker will not be actively engaging with the systems, whereas active recon involves the above examples of port scanning, etc., which are actively engaging with the systems. Common methods of passive reconnaissance can be looking for information on discarded computers and devices, using social engineering and deception to masquerade as an authorised company personnel. (TechTarget Contributor. N.d.)
Common passive recon tools used by cyber security experts include Wireshark (Packet sniffing), Google (Open-source Intelligence), Shodan (Search engine for internet-connected devices) and more. As with the active recon tools, more advanced attackers would be able to create their own modified tools to do these jobs, ones that are not picked up by security systems. (Poston H. 2019)
Through a combination of both active and passive recon, an attacker is able to build a fairly comprehensive image of the organisational structures that are in place. Once they have this image, they can begin to craft their exploit, utilising any information that they have previously gathered. (Cooper Z. 2020)
3.2.	Real world example
In the news article by TechRadar (Nice S. 2010) the writer talks through an example of how both passive and active reconnaissance are used to an attacker’s advantage from the viewpoint of the hacker, however in this case, he was acting ethically. Passive recon as stated earlier is the preparatory phase of an attack, it is used to gather information without directly interacting with the victim systems.
-	URL/networking info: Using the WHOIS tool the Ethical Hacker gathered information about the URL. Then they performed a reverse WHOIS on the IP of the Name server, giving them an IP block with their address, name, UK address, number and the network block.

-	URL Gathering: With serversniff.net the Ethical Hacker discovered subdomains and detail about products, partners, intranet and more. They thought of the possibility of looking for old redundant software to exploit.


-	IP Address scanning: Using the URL/Networking information, the Ethical Hacker was able to scan each server for additional domains, this could have led to more vulnerabilities and information leaks.

-	Google Hacking: By creating complex search engine queries the Ethical Hacker was able to see what the search engines had cached, which led to the discovery of sensitive documents.
Active recon examples from the article by TechRadar also comply with the earlier description given, which dictated that an active scan would interact with the victim system directly.
-	Scanning: Using tools like Nmap and the information gathered in the passive reconnaissance stage, the Ethical Hacker was able to discover open ports, indicating there was possibly a MySQL server running, and a Windows remote desktop port, 80.

-	Identifying server OS: The Ethical Hacker knew that he needed to confirm the servers Operating System. Using Xprobe2 (Remote active OS fingerprinting tool) he found there was a Linux server, including another windows server running in an unknown version.

-	Banner grabbing: The attacker went to identify the applications and versions. Using telnet, they came to the understand that several common services like DNS, Apache, HTTPS Apache and SSH were open.

-	Web server application scan: Finally, the Ethical Hacker ran a web file scanner to enumerate information related to the web applications running on the server. PHP information was found so they took notes on the information and versions that were outputted.

The cyber threat is continually increasing in scale and sophistication. Now more than ever there are a multitude of tools available for anyone to become threat actors (Deloitte. n.d). The examples above of how passive and active recon are used to discover information are only a few of the many different ways that reconnaissance can be conducted.
3.3.	Wider security context (What does it mean in terms of security, commonality and capability?)

The wider security context of reconnaissance seems to be a fairly obvious one, being that the name itself is the act of discovering information about a target, it would not be unthinkable to assume that this is all there is to it. However, this assumption would be ill-advised, reconnaissance is not just about understanding the networks and information structures surrounding the target, rather it is about understanding how these network entities interact and operate with each other on a regular basis. (Kishore S. n.d).
From this we can understand that in terms of security, it is essential that organisations take the appropriate measures to mitigate the about amount of information that is released upon probing the server. The security implications depend on how motivated and skilled the attacker is, however if they are sufficiently motivated then the outcomes could be excessive. An attack could lead to halt in operations or lead to ransoms being demanded, among other things (Olson J. 2019).
The commonality of such attacks would be fairly low, considering the amount of time and effort it takes to effectively gather all appropriate information is not something an average person would be willing to go through. However, as more tools and methods are developed, it does become easier and more accessible, leading to an increase in overall attacks. The post by ThreatPost (2021.) states that with the increase in people working from home due to the Coronavirus pandemic, it is becoming more common for employees to take shortcuts that often expose information or provide attackers with a foothold in which to launch an exploitative attack.
3.4.	Mitigation of the problem

Unfortunately, most early computer technologies and programs were not designed with security in mind, more often than not the idea was to create an efficient system/application that was able to work alongside other systems/applications in a given environment. It is usually more difficult to fix a problem that is built into the foundation of something, than one that comes from the manipulation of it in its more abstract/present form. Holt T. (2017).
In order to counter the active recon method of port scanning, a firewall could be put in place, or in order to stop an attacker from banner grabbing, ensure that you turn off any ‘Server Signatures” or try concealing any file extensions. By removing old files, ensuring that third party software is up to date and proper restrictions are in place, an organisation will be in a better place to ward off these types of attacks. (Nice S. 2010.)
For passive recon mitigation, in relation to URL gathering, an attacker would attempt to find any subdomains by querying the Name Servers found from <WHOIS> command, an organisation could create any subdomains on an internal DNS rather than internet-facing one. It is difficult to mitigate the effects of scanning. When multiple name servers/websites are on a server hosted by an organisation, an attacker may perform a host query on the IP, revealing new information. Recommended mitigation steps would be ensuring effective network firewalls, in addition to constant monitoring of network activity and logs. (Nice S. 2010.)

3.5.	Social, Legal and Ethical considerations

When discussing the considerations of reconnaissance, it is important to consider the context of the attack. For example, if an Ethical Hacker was conducting a pen-test, or some research into the organisation’s security measures, whilst also ensuring that they stick to the scope set out by the overseeing body, they have not crossed any lines outside of what is commonly accepted. However, if a malicious hacker was to perform reconnaissance on an organisation with the intention of committing future offense, then it would not be ensuring that the social, legal and ethical considerations are being upheld. By hacking for political purposes, as part of an organised crime, or for notoriety an individual would be taking part in unethical, socially immoral and illegal process. (Bridewell Consulting. 2019.)
There are common stereotypes for Hackers that they are evil, socially weird, and commonly take part in illegal online activities. This stereotype may have been closer to the truth in the early days of the internet; now however, it is quite the opposite. Most cyber security experts will use their knowledge to a meet high standard of contribution within their respective fields, whilst maintain good ethical, legal and social standing. Pen-testers are required to think like a bad actor, a ‘black hat’ in order to fully protect and mitigate the effects of a real attack. This would not be possible without well-defined methodologies for pen-testing, reconnaissance and all other Ethical Hacking steps required to gain this knowledge and understanding. (Field T. 2011)
Therefore, it should be stated that when discussing whether a hacker is acting with the above considerations in mind, we should also look at the purpose of their actions, whether they are performing them as a good or bad actor, what their intentions are, and moreover whether their actions will outcome in positive or negative consequences.
4.0.	Summary

This report has outlined two important Ethical Hacking topics, detailing what they are, how they are applied and some examples of their implementation, whilst also discussing the ethical, social and legal aspects of their use. 
The social engineering topic introduced the idea that computer security is not solely based on the application of technical skills and knowledge, it can be a dynamic range of human interaction and intelligence gathering. 
As for reconnaissance, the report defined the types and examples which are used regularly by hackers. This topic is more closely associated with the systems themselves and therefore is better understood by cyber security experts.
These two topics link together through the larger process of an attack, meaning that they complement each other and provide large coverage for the reconnaissance phases of the pen-test process. By using social engineering and other passive/active reconnaissance, an attacker would be able to build a comprehensive picture of the target, allowing them more ease to breach and exploit later on. The more thorough the initial recon phases are, the more likely an attack will be successful.
The overall impact on Cyber Security for these topics is dependent on the intentions of the hacker. If the intentions are to a malicious end then the impact would be defined by the damage caused to the victim. In the case of ethical intentions, the impact is one of increasing awareness and understanding of how bad actors manipulate the systems and individuals that use them on a daily basis, whilst also developing new and improved techniques for mitigation.
There are many more topics of discussion in this subject area, all of which link together and complement one another in some form. To begin understanding the entire process, one must break down each part and analyse how they are used, what is the impact of that use and how building a positive security culture that emphasises openness and communication can be an effect method of mitigating potential damage done by these attacks.













References

Aldawood H. Alashoor T. Skinner Geoffrey. (2020). International journal of computer applications. Does the awareness of Social engineering make employee’s more secure? https://www.ijcaonline.org/archives/volume177/number38/aldawood-2020-ijca-919891.pdf
Beaver K. (n.d.). Dummies. The Dangers of social engineering. https://www.dummies.com/computers/pcs/computer-security/the-dangers-of-social-engineering/
Bridewell Consulting. (2019). When is hacking Illegal and legal?. https://www.bridewellconsulting.com/when-is-hacking-illegal-and-legal
Cooper Z. (2020). ITPro. Whats the difference between active and passive reconnaissance?. https://www.itpro.co.uk/penetration-testing/34465/whats-the-difference-between-active-and-passive-reconnaissance
Deloitte. (n.d). Advanced cyber reconnaissance and analytics. https://www2.deloitte.com/us/en/pages/public-sector/articles/understand-organization-adversarial-lens-advanced-cyber-reconnaissance-analytics-federal-government-public-sector.html
Elsevier. (2015). Research gate. Necessity for ethics in social engineering research. https://www.researchgate.net/publication/281968010_Necessity_for_ethics_in_social_engineering_research
Field T. (2011). Bank info Security. Why we need ethical hacking. https://www.bankinfosecurity.com/interviews/we-need-ethical-hacking-i-1145
Ford N. (2018). GRC E-Learning. 5 ways to mitigate social engineering attacks. https://www.grcelearning.com/blog/5-ways-to-mitigate-social-engineering-attacks
Fruhlinger J. (2019). CSO Online. Social engineering explained: How criminals exploit human behavour. CSOonline. https://www.csoonline.com/article/2124681/what-is-social-engineering.html
Geeksforgeeks. (2021). Reconnaissance | Penetration testing. https://www.geeksforgeeks.org/reconnaissance-penetration-testing/
Graylog. (2020). Understanding the 5 phases of intrusion. https://www.graylog.org/post/cyber-security-understanding-the-5-phases-of-intrusion
Hackcontrol. (n.d.). Hack Control. What is the impact of social engineering attacks? https://hackcontrol.org/cases/what-is-the-impact-of-social-engineering-attacks/ 
HackingLoops. (n.d.). Introduction to reconnaissance part 1 terms and methods. https://www.hackingloops.com/introduction-to-reconnaissance-part-1-terms-and-methods/
Harvery J. (2019). Medium. Passive vs. Active reconnaissance. https://medium.com/@jharve08/passive-vs-active-reconnaissance-c2974913237f
Holt T. (2017). Scientific American. What are software vulnerabilities and why are there so many of them? . https://www.scientificamerican.com/article/what-are-software-vulnerabilities-and-why-are-there-so-many-of-them/
Identity Experts. (2017). How social engineering impacts security. https://identityexperts.co.uk/news/how-social-engineering-techniques-impact-security 
Imperva. (n.d.). Social Engineering. https://www.imperva.com/learn/application-security/social-engineering-attack/ 
KasperSky. (n.d.). What is social engineering?.
https://www.kaspersky.co.uk/resource-center/definitions/what-is-social-engineering
Kishore S. (n.d). SISAInfoSec. Reconnaissance the eagle eye of cyber security. https://www.sisainfosec.com/blogs/reconnaissance-the-eagles-eye-of-cyber-security/
Krigsman M. [BetterCloud].  (2016 March 10). How to recognise and prevent social engineering attacks [Webinar]. https://www.bettercloud.com/. https://youtu.be/yezCxMLtvmA?t=1379
Microsoft Security. (2018). Microsoft Security Intellegence Report Volume 23. https://info.microsoft.com/rs/157-GQE-382/images/EN-US_CNTNT-eBook-SIR-volume-23_March2018.pdf 
Mitnick K. [Cybercrime Magazine]. (2020 April 26). My first social engineering hack. [Interview]. https://www.youtube.com/watch?v=YmGwdoS706M&ab_channel=CybercrimeMagazine
Mitnik K. (2002). The art of deception. Wiley Publishing Inc. https://www.wiley.com/en-gb.
Nathaniel S. (2018). Commissum. The history and evolution of social engineering attacks. https://commissum.com/blog-articles/the-history-and-evolution-of-social-engineering-attacks 
Olson J. (2019). Eidebailly. How to deal with Hackers: Detection and Action. https://www.eidebailly.com/insights/articles/2020/11/how-to-deal-with-hackers-detection-and-action 
Phishing. (n.d.). What is phishing?. https://www.phishing.org/what-is-phishing
Poston H. (2019). Top 10 network recon tools. InfoSec Institute. https://resources.infosecinstitute.com/topic/top-10-network-recon-tools/ 
Simpson M. (2013). Hands on Ethical Hacking. CENGAGE Learning. https://www.cengage.com/ 
Stone M. (2019). Security Intelligence. Why deepfake audio technology is a real threat to enterprise security. https://securityintelligence.com/articles/why-deepfake-audio-technology-is-a-real-threat-to-enterprise-security/
Stupp C. (2019). Wall street journal. Fraudsters Used AI to Mimic CEO’s Voice in Unusual Cybercrime Case. https://www.wsj.com/articles/fraudsters-use-ai-to-mimic-ceos-voice-in-unusual-cybercrime-case-11567157402
TechTarget Contributor. (n.d). passive reconnaissance. https://whatis.techtarget.com/definition/passive-reconnaissance 
Tech Republic. (2002). Admins lack confidence in social engineering preparations. https://www.techrepublic.com/article/admins-lack-confidence-in-social-engineering-preparations/
ThreadPost. (2021). 2021 Cyber security trends. https://threatpost.com/2021-cybersecurity-trends/162629/
Webroot. (n.d). What is social engineering? Examples and prevention tips.
https://www.webroot.com/gb/en/resources/tips-articles/what-is-social-engineering
Winder D. (2018). ITPro. Social engineering: The biggest security risk to your business. https://www.itpro.co.uk/social-engineering/30017/social-engineering-the-biggest-security-risk-to-your-business
Zorz M. (2016). The life of a social engineer: Hacking the human. https://www.helpnetsecurity.com/2016/05/19/social-engineer/

