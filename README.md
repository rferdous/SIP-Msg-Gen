# SIP-Msg-Gen


SIP Message Generator (SIP-Msg-Gen)
_____________________________________________
Performance evaluation of a SIP message filtering architecture relies on large scale of SIP traces. But reliable real world VoIP traces are not always available as VoIP providers are not willing to distribute their data due to user privacy agreements. Moreover, VoIP traces with attack information are not so frequent. Considering this situation, we have developed a Synthetic generator 'SIP-Msg-Gen' for generating SIP traces. 'SIP-Msg-Gen' is a synthetic SIP message generator which is capable of generating SIP messages for evaluating the performance of SIP-Parser and SIP malformed detection system. The generator generates SIP malformed messages following SIP torture test messages defined in RFC 4475. 'SIP-Msg-Gen' is capable of generating well-formed SIP messages following SIP grammar defined in RFC 3261.

Download & Install 'SIP-Msg-Gen'
___________________________________________

After downloading please unzip the compressed file. The compressed file contains :

    Jar file of the 'SIP_LEX' application named 'SIP Malformed Msg Generator.jar'.
    A configuration file named “input.properties” containing the list of parameters that should be configured before running 'SIP-Msg-Gen'.

Configure SIP-Msg-Gen
_________________________________
The first step of using SIP-Msg-Gen application is to configure the input parameters which are defined in the configuration file named “input.properties”. The mandatory parameters are :

    1. OUTPUT_FILE_NAME - Path of the input files containing SIP messages
    2. NUMBER_OF_MESSAGE_TYPE -User should define the message types. Value range 1 to 14. Default value is 14 indicating 14 types of messages including both well-formed and malformed INVITE, REGISTER, 	    CANCEL, BEY, ACK, OPTION request messages and response messages.
    3. NUMBER_OF_MESSAGE_SCENARIO - Number of scenarios indicates the number of implemented scenarios of generating malformed messages. Value range 1-19.
    4. MESSAGE_NUMBER - Number of messages to be generaged

Run SIP-Msg-Gen
____________________________
After downloading 'SIP-Msg-Gen', users need to untar it.

    Set PATH variable - export PATH=$PATH:"Location of the .jar file"

    java -jar SIP Malformed Msg Generator.jar

    Output file: SIP_MSG.txt
