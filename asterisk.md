# 1. sip.conf

**[sgroot]**  

type=friend

secret=0000  

context=Marketing

username=sgroot

callerid=Stéphane Groot <88012>  

host=dynamic  

mailbox=88012@ff  

vmsecret = 1234  

disallow=all  

allow=ulaw    


# 2. users.conf

**[sgroot]**   

fullname = Stéphane Groot  

username = sgroot  

secret = 0000  

cid_number = 88012  

hasvoicemail = yes  

description = Finances  

hassip = yes  


# 3. extensions.conf

**[Marketing]**  

exten => 88012,1,Dial(SIP/${EXTEN},20)  

exten => 88012, 2, Voicemail(88012@ff)  

exten => 88012,3,Hangup()  

