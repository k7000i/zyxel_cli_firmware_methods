#Zyxel firmware cli upload
---------------------

1. Step serial port to firewall/router
2. Step minicom -D /dev/tty.usbserial-2140 -b 115200
3. Step restart device and after reboot press any key to enter developer mode
In serial console type:
	atkz –f –l 192.168.1.1
	atgof
Device will be waiting firmware in ftp

4. Connect to device p1 port with enthernet:
5. Open terminal and type:
	ftp 192.168.1.1
	press enter to log in
	bin
	if console returned 200 TYPE is now 8-bit binary then proceed
	put path/to/firmware.bin (no spaces after firmware bin)

5. If everything is ok then device will be restarting...

Upload config via cli
---------------------
1. Open device via ftp client with admin level user
2. Copy config file in device conf dir
3. After login in router in cli type:
	configure terminal
	apply /config/config_filename.conf
