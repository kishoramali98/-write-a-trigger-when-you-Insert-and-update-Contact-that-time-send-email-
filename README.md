# -write-a-trigger-when-you-Insert-and-update-Contact-that-time-send-email-
 write a trigger when you Insert and update Contact that time send email 
Trigger SendemailContact(before insert ,before uodate )
{
    Messaging.SingleEmailMessage  KM= new Messaging.SingleEmailMessage();

    list<string> ToAddresses=New list<string> {'kishoramali1818@gmail.com'};
     list<string> ccAddresses=New list<string> {'kishoramali1818@gmail.com','kishormali1898@gmail.com'};


       KM.setToAddresses(ToAddresses);
       KM.setCCAddresses(ccAddresses);
       KM.setSubject('hey your contact Created');
       KM.setPlainTextBody(' Many many happy returns of the day');
}
