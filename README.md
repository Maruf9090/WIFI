# WIFI


Using the Aircrack-ng suite, we can start attacking a wifi network. This will walk you through attacking a network yourself, assuming you have a monitor mode enabled NIC.

The aircrack-ng suite consists of:

    aircrack-ng
    airdecap-ng
    airmon-ng
    aireplay-ng
    airodump-ng
    airtun-ng
    packetforge-ng
    airbase-ng
    airdecloak-ng
    airolib-ng
    airserv-ng
    buddy-ng
    ivstools
    easside-ng
    tkiptun-ng
    wesside-ng

We'll want to use aircrack-ng, airodump-ng and airmon-ng to attack WPA networks.

The aircrack tools come by default with Kali, or can be installed with a package manager or from https://www.aircrack-ng.org/

I suggest creating a hotspot on a phone/tablet, picking a weak password (From rockyou.txt) and following along with every stage. To generate 5 random passwords from rockyou, you can use this command on Kali: head /usr/share/wordlists/rockyou.txt -n 10000 | shuf -n 5 -

You will need a monitor mode NIC in order to capture the 4 way handshake. Many wireless cards support this, but it's important to note that not all of them do.

Injection mode helps, as you can use it to deauth a client in order to force a reconnect which forces the handshake to occur again. Otherwise, you have to wait for a client to connect normally.
