# edcash Masternode Install Guide

# important to pay attention the script works only 1 masternode in each vps

1. Launch an Ubuntu 16.04 server from either Vultr or DigitalOcean
2. Login to your newly launched server
3. Copy and paste the following line into the server:

```curl -sL https://raw.githubusercontent.com/edcash-project/masternode/master/edcash-masternode.sh | sudo -E bash -```

4. Open your wallet debug console:

```Tools -> Debug Console```

5. Type the following to generate a new address:

```getaccountaddress mn1``` or what masternode number it is that you're launching

6. Send exactly 25,000 EDC to this newly generated address
7. Go to the debug console and enter:

```masternode genkey``` - this is your private key for masternode installation

8. Go back to your VPS and press 'y' to install the dependencies and 'y' when prompted to "compile" the daemon
9. When requested, enter your private key generated above into the VPS and hit enter
10. Go back to your wallet debug console and type:

```masternode outputs```

11. Next, click on:

```Tools -> Open Masternode Configuration File```

12. You will receive your IP address of the VPS after installation is complete along with the private key again, enter the MN config like this below:

```mn# IP_ADDRESS:5003 PRIVATE_KEY TXID INDEX```

13. The TXID and INDEX came from the masternode outputs command
14. Save the file, restart the wallet, and start the masternode after 16 confirmations!
