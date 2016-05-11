# Arduino-WOL
Use arduino to wake in lan any PC in your network. 

Wanted to use wake on lan magic packets to wake my PC remotely was the problem. 

My ISP, my router and even the Internet wouldn't let me sent magic packets.

So I thought I have an arduino just sitting there. Let's make arduino do it for me. 

After a couple of hours this little program came up. In order to get it up and running properly follow the instructions:

1) Edit the MAC address of the shield's Ethernet card( byte mac[] )
2) Assign the proper gateway address, Arduino's IP address and subnet mask( byte ip[], byte gateway[], byte subnet[] )
3) Assign the MAC address of the computer we want to wake ( byte remote_MAC_ADD[] )
4) Assign Arduino a static IP on the router
5) Forward a specific port(e.g 56789) to our Arduino's IP port 23
6) Done!



Now you either have to have a static ip at your home or use a dynamic dns service. 

Simply use telnet like this:

e.g. telnet testing.no-ip.org:56789

Once is connected follow the instructions and arduino will wake your pc for you. 
