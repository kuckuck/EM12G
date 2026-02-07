Band    Uplink Center (Mhz)   Downlink Center(Mhz)   	AT command (Hex mask)
1	    1950		          2140          			AT+QCFG="band",0,1
2	    1880		          1960			            AT+QCFG="band",0,2
3	    1747.5		          1842.5			        AT+QCFG="band",0,4
4	    1732.5		          2132.5			        AT+QCFG="band",0,8
5	    836.5		          881.5			            AT+QCFG="band",0,10
7	    2535		          2655			            AT+QCFG="band",0,40
8	    897.5		          942.5			            AT+QCFG="band",0,80
9	    1767.5		          1862.5			        AT+QCFG="band",0,100
12	    707.5		          737.5			            AT+QCFG="band",0,800
13	    782		              751			            AT+QCFG="band",0,1000
14	    793		              763			            AT+QCFG="band",0,2000
17	    710		              740			            AT+QCFG="band",0,10000
18	    822.5		          867.5			            AT+QCFG="band",0,20000
19	    837.5		          882.5			            AT+QCFG="band",0,40000
20	    847		              806			            AT+QCFG="band",0,80000
21	    1455.5		          1503.5			        AT+QCFG="band",0,100000
25	    1882.5		          1962.5			        AT+QCFG="band",0,1000000
26	    831.5		          876.5			            AT+QCFG="band",0,2000000
28	    725.5		          780.5			            AT+QCFG="band",0,8000000
29	    Downlink only         722.5		            	AT+QCFG="band",0,10000000
30	    2310		          2355          			AT+QCFG="band",0,20000000
32	    Downlink only	      1474		            	AT+QCFG="band",0,80000000
38	    LTE-TDD		          2595		            	AT+QCFG="band",0,2000000000
39	    LTE-TDD		          1900		            	AT+QCFG="band",0,4000000000
40	    LTE-TDD		          2350			            AT+QCFG="band",0,8000000000
41	    LTE-TDD		          2593		            	AT+QCFG="band",0,10000000000
66	    1745		          2155			            AT+QCFG="band",0,20000000000000000



AT+CLAC		list all AT commands

AT+QNWINFO      Current band in use
AT+QCFG="Band"  Current bands config
AT+CSQ 		Check signal strength
AT+QCAINFO      CA Info
AT+QNWINFO	Current band
AT+QENG="servingcell"
AT+QENG="neighbourcell"


#Change scan mode
AT+QCFG="nwscanmode",0,1 < Scan all modes
AT+QCFG="nwscanmode",1,1 < GSM only
AT+QCFG="nwscanmode",2,1 < WCDMA only
AT+QCFG="nwscanmode",3,1 < 4G-LTE only


AT+QSCAN

#Set Connection Modes
AT+QCFG="usbnet",0 - QMI/PPP/Default
AT+QCFG="usbnet",1 - ECM
AT+QCFG="usbnet",2 - MBIM

#Factory reset
AT&F
AT&F1
AT+CFUN=1

#Hard reset
AT+CFUN=1,1

AT+CFUN=0 - Turn off modem


AT+GSN		IMEI
AT+CCID		Sim card ICCID
AT+CIMI		International Mobile Subscriber Identity (IMSI)
AT+CNUM		Phone number	

#eSIM
AT+QESIM="lpamode"
AT+QSIMCFG="eid"

#cell locking
AT+QNWLOCK="common/4g",0


#APN
AT+CGDCONT?
AT+CGACT?


AT+QMBNCFG="List"
AT+QMBNCFG="AutoSel",0 


at+cversion	modem version you are currently using


#rf power
AT+QNWCFG="lte\_rx\_power"

AT+QCFG="rf/maxpower", "LTE",band, pwr

example:
AT+QCFG="rf/maxpower", "LTE",13, 200


Recommend High Gain Omnidirectional Antennas
gold-plated interface


![screenshot](screenshot.png)

![speedtest](speedtest.png)


https://github.com/4IceG/EM12-G
