# Email Enumeration

A common question gets asked every time a large Phishing attack occurs; Who did they get my email? 
Below are a few techniques that you can use to find where you emails are. Once you know what is exposed, you can start to focus on protecting them.
This could come in the form of targeting training for those hit with high number of Phishing attacks. 

Remember, you can't always rely on your security controls. A spear phishing campaign, sending nothing more than a confusing email, to get replies won't be picked up by a system that scans for malicious links and content. Sometimes it best to focus on the endpoint which in Phishing is the user.   
More: https://securethelogs.com/2019/07/11/how-the-phishers-phish/


## Email Sources
Your email is often your online identity. Enterprises heavily reply on email as a source of communication. 
Emailing outside of the organisation to bring in business or support. Signing up for events or personal interests using your company email address. 
All of this is common and day to day life, but all of it leaves a trace. Someone in the chain must store your email address in order to communicate or supply a service. If left unprotected or exposed, it can be stolen. 
Here are a few other sources of information for gathering email addresses: 

- Social media sites such as LinkedIn
- Attendance logs (Third party sites)
- Company website
- Mail listings
- CVs (inc Job reference)
- Google (cached)

## Finding Your Email Address
Below are a few techniques you can use to identify where your email addresses are recorded. This uses the OSINT framework, which is useful framework for finding information online.
If you don't go searching for it, attacks will. You may not be able to take them down, but you will be able to pre-empt and attack (mainly Phishing).

### Google Dorking
Google caches the internet meaning it keeps hold of useful information. If you loaded Google and entered: *"@gmail.com" insite: contact

you would see results of pages that contain peoples gmail address. Now if you started to play with this, you can start to enumerate pages which host your email. If you run the same query but replace gmail.com with your email domain what do you find? 

Now replace, the contact with: *"@gmail.com" filetype:doc | filetype:pdf | filetype:csv | filetype:pdf | filetype:docx  

This will return documents stored on sites that contain people Gmail address. Dorking something that anyone can do, and can help you find exactly what you are looking for. 

More: https://securethelogs.com/2019/05/02/how-to-hack-with-google-dorks/


### Email Patterns
Email patterns are common and make life easier for Phishers. Say for example, your email is John.Doe@Company1.com and John has a LinkedIn account. Johns company also has a LinkedIn account, which has it's employees as connections. If a Phisher was to go through this list, you could most likely generate a list that would be 70% accurate. If Michael Scott and Toby Flenderson both work there, you could assume their email might be: 

Michael.Scott@Company1.com   
Toby.Flenderson@Company1.com   

This is why you should take the time to skim through social media sites, and query your email domain. If it returns multiple people, you may want to ask if they hide it as it's not just Phishers that dig for this information. If they do require to present a mailbox, it should be a secondary STMP, shared mailbox or forwarder. For example, John could publish on his LinkedIn that his contact is jd@company1.com, or enquires@company1.com, basically something that doesn't give the game away. 


## in progress








