# h.225.asn.1

http://www.itu.int/itu-t/recommendations/rec.aspx?rec=H.225

$ mkdir code  
$ cd code  
$ /path/to/asn1c -fcompound-names -gen-PER -pdu=H323-UserInformation ../*.asn  
$ make -f Makefile.am.sample  
$ ./progname -iaper /path/to/h.323.rtp_example/h.225/cs.setup/H323-MESSAGES/H323-MESSAGES.hex
<H323-UserInformation>
    <h323-uu-pdu>
        <h323-message-body>
            <setup>
                <protocolIdentifier>0.0.8.2250.0.4</protocolIdentifier>
                <sourceAddress>
                        <h323-ID>m.jemec</h323-ID>
                    
                </sourceAddress>
                <sourceInfo>
                    <vendor>
                        <vendor>
                            <t35CountryCode>9</t35CountryCode>
                            <t35Extension>0</t35Extension>
                            <manufacturerCode>61</manufacturerCode>
                        </vendor>
                        <productId>
                            43 61 6C 6C 67 65 6E 33 32 33 20 70 6F 67 61 63 
                            73 61 6D 00 00
                        </productId>
                        <versionId>30 2E 39 61 6C 70 68 61 34 00 00</versionId>
                    </vendor>
                    <terminal>
                    </terminal>
                    <mc><false/></mc>
                    <undefinedNode><false/></undefinedNode>
                </sourceInfo>
                <destCallSignalAddress>
                    <ipAddress>
                        <ip>0A 01 06 12</ip>
                        <port>1720</port>
                    </ipAddress>
                </destCallSignalAddress>
                <activeMC><false/></activeMC>
                <conferenceID>F8 FD F9 3E CD 9E D6 11 9A B2 00 04 76 22 20 17</conferenceID>
                <conferenceGoal>
                    <create></create>
                </conferenceGoal>
                <callType>
                    <pointToPoint></pointToPoint>
                </callType>
                <sourceCallSignalAddress>
                    <ipAddress>
                        <ip>0A 01 03 8F</ip>
                        <port>32803</port>
                    </ipAddress>
                </sourceCallSignalAddress>
                <callIdentifier>
                    <guid>C0 FE F9 3E CD 9E D6 11 9A B2 00 04 76 22 20 17</guid>
                </callIdentifier>
                <mediaWaitForConnect><false/></mediaWaitForConnect>
                <canOverlapSend><false/></canOverlapSend>
                <multipleCalls><false/></multipleCalls>
                <maintainConnection><false/></maintainConnection>
            </setup>
        </h323-message-body>
        <h245Tunnelling><false/></h245Tunnelling>
    </h323-uu-pdu>
</H323-UserInformation>


$ ./progname -iaper /path/to/h.323.rtp_example/h.225/cs.connect/H323-MESSAGES/H323-MESSAGES.hex 
<H323-UserInformation>
    <h323-uu-pdu>
        <h323-message-body>
            <connect>
                <protocolIdentifier>0.0.8.2250.0.3</protocolIdentifier>
                <h245Address>
                    <ipAddress>
                        <ip>0A 01 06 12</ip>
                        <port>1232</port>
                    </ipAddress>
                </h245Address>
                <destinationInfo>
                    <vendor>
                        <vendor>
                            <t35CountryCode>0</t35CountryCode>
                            <t35Extension>0</t35Extension>
                            <manufacturerCode>0</manufacturerCode>
                        </vendor>
                        <productId>33 31 30 69</productId>
                        <versionId>52</versionId>
                    </vendor>
                    <terminal>
                    </terminal>
                    <mc><false/></mc>
                    <undefinedNode><false/></undefinedNode>
                </destinationInfo>
                <conferenceID>F8 FD F9 3E CD 9E D6 11 9A B2 00 04 76 22 20 17</conferenceID>
                <callIdentifier>
                    <guid>C0 FE F9 3E CD 9E D6 11 9A B2 00 04 76 22 20 17</guid>
                </callIdentifier>
                <multipleCalls><false/></multipleCalls>
                <maintainConnection><false/></maintainConnection>
            </connect>
        </h323-message-body>
        <h245Tunnelling><false/></h245Tunnelling>
    </h323-uu-pdu>
</H323-UserInformation>
