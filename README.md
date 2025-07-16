```
{
	"observatory": {
		"subjectSelector": [
			"proxy"
		],
		"probeURL": "http://www.google.com/gen_204",
		"probeInterval": "3s",
		"enableConcurrency": true
	},
	"routing": {
		"domainStrategy": "AsIs",
		"rules": [
			{
				"inboundTag": [
					"wg",
					"vless",
					"socks"
				],
				"balancerTag": "bal"
			}
		],
		"balancers": [
			{
				"selector": [
					"proxy"
				],
				"strategy": {
					"type": "leastPing"
				},
				"tag": "bal"
			}
		]
	},
	"inbounds": [
		{
			"listen": "127.0.0.1",
			"port": 1080,
			"protocol": "socks",
			"settings": {
				"auth": "noauth",
				"udp": true
			},
			"sniffing": {
				"destOverride": [
					"http",
					"tls",
					"quic"
				],
				"enabled": false,
				"routeOnly": true
			},
			"tag": "socks"
		}
	],
	"outbounds": [
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fin3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "ilkr8h9TZ5--WfVVb3kRv-Ga-L4dcFTcQXD72BxGYEU",
					"serverName": "fin3.nxtcloud.cc",
					"shortId": "73c7f5f07329ceb5"
				},
				"security": "reality"
			},
			"tag": "proxy0",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fin4.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "fgxBnWYtvfbMJ74xJbIQtYIMRWP22xsBbo-sG0UVv3c",
					"serverName": "fin4.nxtcloud.cc",
					"shortId": "86f376118ec28398"
				},
				"security": "reality"
			},
			"tag": "proxy1",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fin5.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "t08Fy7av9T20QAOWzdWhXHdf8yzKG8nNDtfxbjmgyTI",
					"serverName": "fin5.nxtcloud.cc",
					"shortId": "24c2ff209c48a065"
				},
				"security": "reality"
			},
			"tag": "proxy2",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fin6.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "SDdiEqwH6NVLy7FriM7dfm7s1vUt4VCWxocDycGjeiY",
					"serverName": "fin6.nxtcloud.cc",
					"shortId": "3092e799359c6b68"
				},
				"security": "reality"
			},
			"tag": "proxy3",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "g0wexMXOvYha8WcfhoLqRKq5opFz64Z1_JJv7azetQM",
					"serverName": "deu3.nxtcloud.cc",
					"shortId": "d71f2a52d3b3e61a"
				},
				"security": "reality"
			},
			"tag": "proxy4",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu4.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "v3L7_odZd18pHRViNUcwG6L7z1_ijgkATafQItzeniQ",
					"serverName": "deu4.nxtcloud.cc",
					"shortId": "99e905bedcaf4b8a"
				},
				"security": "reality"
			},
			"tag": "proxy5",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu5.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "HELP8dC-vhMUWWrsT-_KcwTHOah9SdFWhGpSnveiLDg",
					"serverName": "deu5.nxtcloud.cc",
					"shortId": "37acd433f5051d3e"
				},
				"security": "reality"
			},
			"tag": "proxy6",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu6.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "Nr3-sbL8kb8qFXWWHbQzsW4GebmrfLlsZWECf4hB6HI",
					"serverName": "deu6.nxtcloud.cc",
					"shortId": "826da5f6153f7d31"
				},
				"security": "reality"
			},
			"tag": "proxy7",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu7.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "WoqlgP96Ylfeebv_R_j3y4TBDfyTCY6aFklXm5ioT3k",
					"serverName": "deu7.nxtcloud.cc",
					"shortId": "1e78eaf0dbed1f27"
				},
				"security": "reality"
			},
			"tag": "proxy8",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu8.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "oZOmSmSk7mRow9IqgcsuVKXl6o_TVsBdph-bT5TEa1E",
					"serverName": "deu8.nxtcloud.cc",
					"shortId": "30aeb9e3a87b8aee"
				},
				"security": "reality"
			},
			"tag": "proxy9",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu9.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "XJbJutMIwR2GyAeZx48INxjaa84cBoZx0EzqPDWNGR4",
					"serverName": "deu9.nxtcloud.cc",
					"shortId": "96119d6a1c409e8a"
				},
				"security": "reality"
			},
			"tag": "proxy10",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "deu10.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vBeiK_0s_U_aJeHbnLglTFCw3TN4L1Kn0F0t4N7g7gY",
					"serverName": "deu10.nxtcloud.cc",
					"shortId": "f10234328dea05f1"
				},
				"security": "reality"
			},
			"tag": "proxy11",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "usa1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "i7ElBsBYnfoN_ezSYkt1f8L9NJop9xZNKiSrjhlt2Bs",
					"serverName": "usa1.nxtcloud.cc",
					"shortId": "6e7953c8f69ecf13"
				},
				"security": "reality"
			},
			"tag": "proxy12",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "pol1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "lbOxUfCOas7NH9UyUON0-JBrC2bf-LqX3qtDKaDHqUg",
					"serverName": "pol1.nxtcloud.cc",
					"shortId": "93c9117e5c700dcf"
				},
				"security": "reality"
			},
			"tag": "proxy13",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "esp1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "ySLtJxyCx9aVl3HShabC4mgiglD4yEebjzaZe2pxAlM",
					"serverName": "esp1.nxtcloud.cc",
					"shortId": "615fdf45a54a0876"
				},
				"security": "reality"
			},
			"tag": "proxy14",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "gbr1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "C6E8wxLdaeZgDSKlMF1A-X9rYKf5_BtMVbppSE0TIFw",
					"serverName": "gbr1.nxtcloud.cc",
					"shortId": "182065cc5832e9a3"
				},
				"security": "reality"
			},
			"tag": "proxy15",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "cze1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "PB53XIFhBS-ScKAMwJvGv1r18uU312unk9gQ92J62ik",
					"serverName": "cze1.nxtcloud.cc",
					"shortId": "0b91636e3fdf3493"
				},
				"security": "reality"
			},
			"tag": "proxy16",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fra1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "Sw-GpHb1WupkX3vaTZCqfjN9s7CmOLk03Dks4d0E2F0",
					"serverName": "fra1.nxtcloud.cc",
					"shortId": "e8f18636300ec4ea"
				},
				"security": "reality"
			},
			"tag": "proxy17",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "nld1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "MYV7YSWy9GstGdezygXKOTr_eXwyaewvQJfz87ojZj4",
					"serverName": "nld1.nxtcloud.cc",
					"shortId": "d6753c2333b56b3e"
				},
				"security": "reality"
			},
			"tag": "proxy18",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "nld2.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "yQwI9A0KksA7qgCAkfGbLqRmpmDtHfYCh0YqCPvo5zA",
					"serverName": "nld2.nxtcloud.cc",
					"shortId": "96e6ab92a73531f0"
				},
				"security": "reality"
			},
			"tag": "proxy19",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "nld3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "nld3.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy20",
			"SendTorrent": "true"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "ita1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "ita1.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy21",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "bgr1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "bgr1.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy22",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fra2.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "fra2.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy23",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "ita2.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "ita2.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy27",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "gbr2.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "i7ElBsBYnfoN_ezSYkt1f8L9NJop9xZNKiSrjhlt2Bs",
					"serverName": "gbr2.nxtcloud.cc",
					"shortId": "6e7953c8f69ecf13"
				},
				"security": "reality"
			},
			"tag": "proxy28",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "cze2.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "PB53XIFhBS-ScKAMwJvGv1r18uU312unk9gQ92J62ik",
					"serverName": "cze2.nxtcloud.cc",
					"shortId": "0b91636e3fdf3493"
				},
				"security": "reality"
			},
			"tag": "proxy29",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "pol3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "PB53XIFhBS-ScKAMwJvGv1r18uU312unk9gQ92J62ik",
					"serverName": "pol3.nxtcloud.cc",
					"shortId": "0b91636e3fdf3493"
				},
				"security": "reality"
			},
			"tag": "proxy30",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "cze3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "PB53XIFhBS-ScKAMwJvGv1r18uU312unk9gQ92J62ik",
					"serverName": "cze3.nxtcloud.cc",
					"shortId": "0b91636e3fdf3493"
				},
				"security": "reality"
			},
			"tag": "proxy31",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "pol2.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "lbOxUfCOas7NH9UyUON0-JBrC2bf-LqX3qtDKaDHqUg",
					"serverName": "pol2.nxtcloud.cc",
					"shortId": "93c9117e5c700dcf"
				},
				"security": "reality"
			},
			"tag": "proxy32",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fra3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "fra3.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy33",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "gbr3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "i7ElBsBYnfoN_ezSYkt1f8L9NJop9xZNKiSrjhlt2Bs",
					"serverName": "gbr3.nxtcloud.cc",
					"shortId": "6e7953c8f69ecf13"
				},
				"security": "reality"
			},
			"tag": "proxy34",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "ita3.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "ita3.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy35",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "ita4.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "ita4.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy36",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "ita5.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "ita5.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy37",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "pol4.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "PB53XIFhBS-ScKAMwJvGv1r18uU312unk9gQ92J62ik",
					"serverName": "pol4.nxtcloud.cc",
					"shortId": "0b91636e3fdf3493"
				},
				"security": "reality"
			},
			"tag": "proxy38",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fra4.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "fra4.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy39",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "rou1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "rou1.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy40",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "srb1.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "srb1.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy41",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "fra5.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "vOOkcMRPmw50Fn1wBprDpfYxGAX3oAjtGtb6zirevXk",
					"serverName": "fra5.nxtcloud.cc",
					"shortId": "8eadf0574a167804"
				},
				"security": "reality"
			},
			"tag": "proxy42",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "usa4.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "i7ElBsBYnfoN_ezSYkt1f8L9NJop9xZNKiSrjhlt2Bs",
					"serverName": "usa4.nxtcloud.cc",
					"shortId": "6e7953c8f69ecf13"
				},
				"security": "reality"
			},
			"tag": "proxy43",
			"SendTorrent": "false"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "usa5.nxtcloud.cc",
						"port": 8443,
						"users": [
							{
								"encryption": "none",
								"flow": "xtls-rprx-vision",
								"id": "e4d61f2c-462f-44cb-9323-63250613e178"
							}
						]
					}
				]
			},
			"streamSettings": {
				"network": "tcp",
				"realitySettings": {
					"fingerprint": "random",
					"publicKey": "i7ElBsBYnfoN_ezSYkt1f8L9NJop9xZNKiSrjhlt2Bs",
					"serverName": "usa5.nxtcloud.cc",
					"shortId": "6e7953c8f69ecf13"
				},
				"security": "reality"
			},
			"tag": "proxy44",
			"SendTorrent": "false"
		},
		{
			"protocol": "freedom",
			"tag": "direct"
		},
		{
			"protocol": "blackhole",
			"tag": "block"
		}
	]
}
```