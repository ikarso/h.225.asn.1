# h.225.asn.1

http://www.itu.int/itu-t/recommendations/rec.aspx?rec=H.225

$ mkdir code  
$ cd code  
$ /path/to/asn1c -fcompound-names -gen-PER -pdu=CallIdentifier ../*.asn  
$ make -f Makefile.am.sample  
$ ./progname -iaper /path/to/h.323.rtp_example/h.225/cs.setup/H323-MESSAGES/H323-UserInformation/h323-uu-pdu/h323-message-body/Setup-UUIE/callIdentifier/callIdentifier.hex  
<CallIdentifier>  
    <guid>C0 FE F9 3E CD 9E D6 11 9A B2 00 04 76 22 20 17</guid>  
</CallIdentifier>  
