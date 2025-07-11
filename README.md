# window-server-RDP-lisence-issue




how to remove RDP lisence issue on window server
====================================================================================
# got to registry edit
wind+R
regedit
#go to the following path
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server\RCM
# right click on RCM and then permission 
give a full control for administrator 
#if you get 'access denaid' error 
under permission go to advanced and click on change button infront of  owner : SYSTEM
then applay and ok 
# under lisence core on the right side delete the key 
# restart the server to make the chagetake effect 

this method is worked for us on one of our window server 
