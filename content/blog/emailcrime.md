Title: Email Cyber Crime
Date: 2017-11-14
Modified: 2017-11-14 19:54
Category: Email
Tags: email, cyber, cybercrime, computer crime
Slug: email_cyber_crime_explained
Authors: Mika Ayenson
Summary: Let's do a deep dive into e-mail and cyber crimes.

![Alt Text]({filename}/images/red_email.png)

#### Introduction 

E-mail in day-to-day business is an essential capability that empowers employees to communicate internally and externally.  Users receive updates, share documents, receive alerts, organize meetings, share information, and many other things without having to physically meet or call people they want to communicate with. When e-mails are received, there is a level of trust that the sender is who the mail server says they are. This trust factor and other technical aspects of mail servers are unfortunately exploited and give adversaries different attack vectors. In this blog, the client and server fundamentals, examples of e-mail crime committed, vulnerabilities associated with emails, spoofing, tools used to investigate e-mail cybercrime, and laws to fight email cybercrime are discussed. 

### Server and Client Involved in Email Communication

The mail server and endpoint client are the two main nodes used in email communication. The mail server sends e-mails between endpoints and other mail servers, receives e-mails from endpoints, and stores e-mails for user endpoints. Mail servers and user endpoints are configured to use the same protocol whether it is POP3, IMAP, SMTP, or HTTP ("Setting Up Mail Servers in Outlook Express", 2017). The client machines typically send, receive, and store e-mails on endpoints like mobile devices and computers. From endpoint to endpoint, e-mail must connect to at least one mail server. Users can use software like Microsoft outlook to send the e-mail, the e-mail is sent to a Microsoft Exchange server, and then ends ultimately at another users e-mail. 

### Four Examples of Crime Committed by Sending E-mails

By sending malicious e-mails perpetrators can commit crimes in multiple ways. Four examples of e-mail crimes are e-mail bombing, e-mails involving threating extortion, e-mail fraud, and maliciously spreading malware. According to US-CERT, e-mail bombing is when an individual repeatedly sends e-mails targeted at a victim with typically a large and meaningless amount of data ("Email Bombing Spamming", 2017). The goal of the adversary is to consume a large amount of the victim’s data and network resources.

Another example is when computer criminals send threatening e-mails to victims in attempt to extort them. According to the FBI in 2007, life-threatening e-mails started to trend online that attempted to scare victims into paying thousands on dollars (Online Extortion, 2007). Although the Internet Crime Complaint Center didn’t report and financial loss for the victims, the act of sending malicious e-mails itself was still a crime.

Spreading malware through e-mails is also a computer crime ("Report Phishing Sites", 2017). Typically this is sent as a phishing attempt where the adversary tries to trick the victim into opening a file or downloaded and executing a windows binary. The adversary typically claims that the file is an urgent update and must be executed.

Lastly, in 2016 the IRS reported e-mail being used fraudulently to send e-mails claiming they were apart of the IRS team so that users would send their personal information (IRS News Releases, 2016). This was not exactly a spoofing attempt but a few characteristics were similar. For example, the perpetrator included images that resembled the IRS logos, and posed as the IRS by saying “Your eServices Team” in the from header.

As a safe precaution, if any e-mails appear suspicious, users can analyze the e-mails headers to verify the e-mails authenticity.

### Common E-mail Headers and Description


|Header name |        Protocol|
|---  |       --- |
| Date |                  Message date and time|
| From |                  Mailbox of message author|
| Sender |                Mailbox of message sender|
| Reply-To |              Mailbox for replies to message|
| To |                    Primary recipient mailbox|
| Cc |                    Carbon-copy recipient mailbox|
| Bcc |                   Blind-carbon-copy recipient mailbox|
| Message-ID |            Message identifier|
| In-Reply-To |           Identify replied-to message(s)|
| References |            Related message identifier(s)|
| Subject |               Topic of message|
| Comments |              Additional comments about the message|
| Keywords |              Message key words and/or phrases|
| Resent-Date |           Date and time message is resent|
| Resent-From |           Mailbox of person for whom message is resent|
| Resent-Sender |         Mailbox of person who actually resends the message|
| Resent-To |             Mailbox to which message is resent|
| Resent-Cc |             Mailbox(es) to which message is cc'ed on resend|
| Resent-Bcc |            Mailbox(es) to which message is bcc'ed on resend|
| Resent-Reply-To |       Resent reply-to|
| Resent-Message-ID |     Message identifier for resent message|
| Return-Path |           Message return path|
| Received |              Mail transfer trace information|
| Encrypted |             Message encryption information|
| Disposition-Notification-To |     Mailbox for sending disposition notification|
| Disposition-Notification-Options |     Disposition notification options|
| Accept-Language |       Language(s) for auto-responses|
| Original-Message-ID |   Original message identifier|
| PICS-Label |            PICS rating label|
| Encoding |              Message encoding and other information|
| List-Archive |          URL of mailing list archive|
| List-Help |             URL for mailing list information|
| List-ID |               Mailing list identifier|
| List-Owner |            URL for mailing list owner's mailbox|
| List-Post |             URL for mailing list posting|
| List-Subscribe |        URL for mailing list subscription|
| List-Unsubscribe |      URL for mailing list unsubscription|
| Message-Context |       Type or context of message|
| DL-Expansion-History |  Trace of distribution lists passed|
| Alternate-Recipient |   Controls forwarding to alternate recipients|
| Original-Encoded-Information-Types |  Body part types in message|
| Content-Return |        Return content on non-delivery?|
| Generate-Delivery-Report |  Request delivery report generation|
| Prevent-NonDelivery-Report |  Non-delivery report required?|
| Obsoletes |             Reference message to be replaced|
| Supersedes |            Reference message to be replaced|
| Content-Identifier |    Message content identifier|
| Delivery-Date |         Message delivery time|
| Expiry-Date |           Message expiry time|
| Expires |               Message expiry time|
| Reply-By |              Time by which a reply is requested|
| Importance |            Message importance|
| Incomplete-Copy |       Body parts are missing|
| Priority |              Message priority|
| Sensitivity |           Message content sensitivity|
| Language |              X.400 message content language|
| Conversion |            Conversion allowed?|
| Conversion-With-Loss |  Lossy conversion allowed?|
| Message-Type |          Message type: delivery report?|
| Autosubmitted |         Automatically submitted indicator|
| Autoforwarded |         Automatically forwarded indicator|
| Discarded-X400-IPMS-Extensions |  X.400 IPM extensions discarded|
| Discarded-X400-MTS-Extensions |   X.400 MTS extensions discarded|
| Disclose-Recipients |   Disclose names of other recipients?|
| Deferred-Delivery |     Deferred delivery information|
| Latest-Delivery-Time |  Latest delivery time requested|
| Originator-Return-Address |  Originator return address|
| X400-Content-Identifier |  Message content identifier|
| X400-Content-Return |   Return content on non-delivery?|
| X400-Content-Type |     X400 content type|
| X400-MTS-Identifier |   X400 MTS-Identifier|
| X400-Originator |       X400 Originator|
| X400-Received |         X400 Received|
| X400-Recipients |       X400 Recipients|
| X400-Trace |            X400 Trace|


### Four Examples of Crimes Supported by E-mails

There are several different e-mail crimes that are supported through e-mails like harassment, blackmailing, identity fraud, and even sharing classified information.  When people send threatening e-mails they are cyber bullying. Similar to bullying in general, when people bully victims through e-mail, they are breaking cyber harassment laws. Similarly, blackmail through e-mail is another supported crime. Blackmail just like harassment is when individuals direct threating or abusive messages to another individual. Blackmail extends the crime by extorting the victim. Identity fraud is a supported by e-mails by being apart of the attack strategy. Criminals send e-mails either to individuals or businesses posing as another person to steal personal data or defraud another individual. An example of this is when a person sends an e-mail to a bank posing as another individual to gain access to their bank account. Finally, something as egregious espionage is supported through e-mail. For example, if an individual’s sends classified documents from the secret internet protocol router network to the non-classified internet protocol router network, they are committing a cyber crime. 

### E-mail Spoofing

Another example of crime supported by e-mails that are committed by sending an e-mail is called e-mail spoofing. Adversaries sometimes use simple tactics to spoof e-mails and sometimes simply just say that they are someone in the e-mail that they really are not. E-mail spoofing is not the same thing as forging, where an individual sends an e-mail with header information that appears to originate from a source that is not the actually source.  E-mail addresses can be spoofed, the content of the e-mail can be faked, and the headers can be forged ("Spoofed/Forged Email", 2017). Each tactic is used to trick the user into revealing sensitive information to the attacker.

### Common Invesigative E-mail Cybercrime Tools

Other than looking at header information directly, there are several tools that help investigators in e-mail cybercrime like eMailTrackerPro, EmailTracer, Adcomplain, Aid4Mail Forensic, AbusePipe, AccessData’s FTK, EnCase Forensic, FINALeMAIL, Forensics Investigation Toolkit (FIT), and Paraben (Network) E-mail Examiner (Tariq Banday, 2011). 

|Tool	| Description|
| --- | --- |
|eMailTrackerPro	| Analyses e-mail headers to identify the senders IP address.|
|EmailTracer	| Indian law enforcement tool to trace IP address and e-mail headers of originator.|
|Adcomplain	| Tool to report inappropriate commercial e-mails in postings.|
|Aid4Mail | Forensic	E-mail forensic tool to e-discovery and litigation support.|
|AbusePipe	| Tool to analyze complaint e-mails to determine e-mail originator.|
|AccessData’s FTK |	Court-validated digital forensic investigator with e-mail capabilities.|
|EnCase Forensic	|Digital forensics tool with imaging capabilities.|
|FINALeMAIL	| E-mail recovery tool.|
|Forensics | Investigation Toolkit (FIT)	Packet capturing tool to ingest raw data and use in fraud and forensic law enforcement.|
|Paraben (Network)| E-mail Examiner	Tool to search through e-mail applications, recover e-mails and analyze e-mails.|

### Two US laws Fighting Against E-mail Cybercrime

Two laws that help the United States fight against e-mail cyber are the Computer Fraud and Abuse Act of 1986 (CFAA), and the Identity Theft Enforcement and Restitution Act of 2008 (ITERA). ITERA was created to increase federal prosecution for identity theft related crimes and help the victims by providing restitution for the victims ("H.R.4718 - 99th Congress (1985-1986): Computer Fraud and Abuse Act of 1986", 2017). CFAA was created to persecute criminals that intentionally committed computer fraud ("Identity Theft Enforcement and Restitution Act of 2007 (2007 - S. 2168)", 2017). Although ITERA applies to identity theft in general, both of these laws also apply to cybercrimes including e-mail related crimes.

### Conclusion

When e-mail capabilities are used in an organization, there are several different components to consider when trying protecting a business from adversaries. There is the server and client that must be created and properly configured, different threat vectors that adversaries can use to attack individuals, tools and techniques used to investigate e-mail related crimes, and finally laws that are designed to protect against e-mail related computer crimes. Each of these areas has to be properly assessed to mitigate cyber crimes within the business.


<script>
var tables, i;
tables = document.getElementsByTagName('table');
for (i=0;i<tables.length;i++) {
  tables[i].className = 'table table-striped';
}
</script>

 
