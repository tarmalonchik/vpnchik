```
{
	"observatory": {
		"subjectSelector": [
			"proxy"
		],
		"probeURL": "http://www.google.com/gen_204",
		"probeInterval": "8s",
		"enableConcurrency": true
	},
	"inbounds": [
		{
			"listen": "127.0.0.1",
			"port": 10808,
			"protocol": "socks",
			"settings": {
				"auth": "noauth",
				"udp": true,
				"userLevel": 8
			},
			"sniffing": {
				"destOverride": [
					"http",
					"tls"
				],
				"enabled": true,
				"routeOnly": false
			},
			"tag": "socks"
		},
		{
			"listen": "127.0.0.1",
			"port": 10809,
			"protocol": "http",
			"settings": {
				"userLevel": 8
			},
			"tag": "http"
		}
	],
	"log": {
		"loglevel": "warning"
	},
	"outbounds": [
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
			"tag": "proxy11"
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
			"tag": "proxy44"
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
			"tag": "proxy20"
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
			"tag": "proxy34"
		},
				{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "213.171.4.131",
						"port": 443,
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
					"publicKey": "dkVl6tmLLWG3580AI81ecGt1hA0PmelCEbB1ViWbZFw",
					"serverName": "yandex.ru",
					"shortId": "15b4f9f309316461"
				},
				"security": "reality"
			},
			"tag": "proxy666"
		},
				{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "213.171.4.131",
						"port": 443,
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
					"publicKey": "dkVl6tmLLWG3580AI81ecGt1hA0PmelCEbB1ViWbZFw",
					"serverName": "yandex.ru",
					"shortId": "15b4f9f309316461"
				},
				"security": "reality"
			},
			"tag": "proxy666"
		},
		{
			"protocol": "vless",
			"settings": {
				"vnext": [
					{
						"address": "94.131.113.201",
						"port": 443,
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
					"publicKey": "dkVl6tmLLWG3580AI81ecGt1hA0PmelCEbB1ViWbZFw",
					"serverName": "yandex.ru",
					"shortId": "15b4f9f309316461"
				},
				"security": "reality"
			},
			"tag": "proxy667"
		},
		{
			"protocol": "freedom",
			"settings": {
				"domainStrategy": "UseIP"
			},
			"tag": "direct"
		}
	],
	"routing": {
		"domainStrategy": "AsIs",
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
		],
		"rules": [
			{
				"inboundTag": [
					"wg",
					"vless",
					"socks"
				],
				"balancerTag": "bal"
			}
		]
	}
}
```