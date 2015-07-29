# phonebook

print "Erie's and Sarah's Phone Numbers"

print "___________________________________________"

def displayuserinfo (userinfo):
    print ("\t-----------------------------------------------------------")
    print ("\t!Match found for", userinfo[0], "", userinfo [1], "!!")
    print ("\tFirst Name:" , userinfo [0])
    print ("\tphoneNumber",  userinfo [1])
    print ("\t------------------------------------------------------------")
    return


firstname = ""
phoneNumber = ""
entryfound =""


while firstname != "exit" :
       firstname= raw_input("Enter first name(exit to end):")
       firstname= firstname.lower()

       if firstname == "exit":
            break
       else:
              phoneNumber = raw_input ("Enter a number:")
              phoneNumber = phoneNumber.lower()
            
              addressbook = open ("ThisPC\Documents\python\phoneNumber4",'r')

              for line in addressbook:
                   userinfo=line.split('|')
                   if  ((userinfo[0].lower () == (firstname or firstname.lower)) and (userinfo[1].lower() == (phoneNumber or phoneNumber.lower))):
                        entryfound = True
                        break
                   else:
                        entryfound = False
                        continue
                        
            if  entryfound == False :
                print ("Sorry that Name or Number does not exist")

            else:
                 displayuserinfo (userinfo)
            addressbook.close ()
            entryfound = " "



            
