## INSTRUCTIONS


### CLI OF ROUTER 

Would you like to enter the initial configuration dialog? [yes/no]: n \
Press RETURN to get started!\
Router>en\
Router#conf t\
Enter configuration commands, one per line.  End with CNTL/Z.\
Router(config)#hostname R1\
R1(config)#enable secret cisco\
R1(config)#int f0/0\
R1(config-if)#ip add 192.168.1.1 255.255.0.0\
R1(config-if)#no shut\
R1(config-if)#\
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up\
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0, changed state to up\
R1(config-if)#end\
R1#\
%SYS-5-CONFIG_I: Configured from console by console\
R1#wr\
Building configuration...\
[OK]\
R1#\
R1#conf t\
Enter configuration commands, one per line.  End with CNTL/Z.\
R1(config)#line vty 0 5\
R1(config-line)#login\
% Login disabled on line 132, until 'password' is set\
% Login disabled on line 133, until 'password' is set\
% Login disabled on line 134, until 'password' is set\
% Login disabled on line 135, until 'password' is set\
% Login disabled on line 136, until 'password' is set\
% Login disabled on line 137, until 'password' is set\
R1(config-line)#password pass\
R1(config-line)#end\
R1#\
%SYS-5-CONFIG_I: Configured from console by console\
R1#exit\

### Command prompt of PC 0 (to check if telnet configuration in successful or not)

Packet Tracer PC 0 Command Line 1.0\
C:\>ping 192.168.1.1\
Pinging 192.168.1.1 with 32 bytes of data:\
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255\
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255\
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255\
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255\
Ping statistics for 192.168.1.1:\
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),\
Approximate round trip times in milli-seconds:\
    Minimum = 0ms, Maximum = 0ms, Average = 0ms\
C:\>telnet 192.168.1.1\
Trying 192.168.1.1 ...Open\
User Access Verification\
Password: \
R1>en\
Password: \
R1#\

