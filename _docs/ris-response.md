---
title: RIS Response
tags: [RIS, Response, Example]
---

After a merchant has posted RIS information to Kount, a key-value pair string will be returned to the merchant (RIS Response). The RIS response format will be the same that was specified in the RIS post, with the default being named pairs. Each data field must be invoked by `getter` methods on the response object found in the SDK. The merchant can then use the RIS response to automate the order management process by keying off the AUTO field and can utilize any of the additional data returned for internal processing.

An important use of the RIS response is the ability to verify if the Data Collector process was successful and view any warnings or errors that were made during the RIS post from the merchant. The KAPT field is used to determine if the Data Collector process was successful. KAPT=Y means successful, KAPT=N means the process was unsuccessful. All warnings will be displayed in the response and if errors do occur the RIS response will be returned with a MODE=E.


## RIS Response JSON (with no rules triggered)

```json
{
    "VERS": "0700",
    "MODE": "Q",
    "TRAN": "76JG032JT7CD",
    "MERC": "888889",
    "SESS": "f2d209d0d4cf4c37b0481ff3adcbde00",
    "ORDR": "ORDR-1567540565",
    "AUTO": "A",
    "SCOR": "28",
    "GEOX": "US",
    "BRND": "VISA",
    "REGN": "US_ID",
    "NETW": "N",
    "KAPT": "Y",
    "CARDS": "1",
    "DEVICES": "1",
    "EMAILS": "1",
    "VELO": "0",
    "VMAX": "0",
    "SITE": "DEFAULT",
    "DEVICE_LAYERS": "DF651ACF30..99CF09F417.E3D16F2CB7.061826EF2B",
    "FINGERPRINT": "290D1C0172364AADAC25D9FD0B13D946",
    "TIMEZONE": "360",
    "LOCALTIME": "2019-09-03 13:56",
    "REGION": "US_ID",
    "COUNTRY": "US",
    "PROXY": "N",
    "JAVASCRIPT": "Y",
    "FLASH": "N",
    "COOKIES": "Y",
    "HTTP_COUNTRY": "US",
    "LANGUAGE": "EN",
    "MOBILE_DEVICE": "N",
    "MOBILE_TYPE": null,
    "MOBILE_FORWARDER": "N",
    "VOICE_DEVICE": "N",
    "PC_REMOTE": "N",
    "RULES_TRIGGERED": 0,
    "COUNTERS_TRIGGERED": 0,
    "REASON_CODE": null,
    "DDFS": "2019-08-22",
    "DSR": "1050x1680",
    "UAS": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/76.0.3809.100 Safari/537.36",
    "BROWSER": "Chrome 76.0.3809.100",
    "OS": "Mac OS X 10.14.6",
    "PIP_IPAD": null,
    "PIP_LAT": null,
    "PIP_LON": null,
    "PIP_COUNTRY": null,
    "PIP_REGION": null,
    "PIP_CITY": null,
    "PIP_ORG": null,
    "IP_IPAD": "208.75.113.3",
    "IP_LAT": "43.6337",
    "IP_LON": "-116.2004",
    "IP_COUNTRY": "US",
    "IP_REGION": "Idaho",
    "IP_CITY": "Boise",
    "IP_ORG": "UNKNOWN",
    "OMNISCORE": 54,
    "3D_SECURE_MERCHANT_RESPONSE": "Challenge"
    "WARNING_COUNT": 0
} 
```
## RIS Response JSON (with rules triggered)

```json
{
    "VERS": "0700",
    "MODE": "Q",
    "TRAN": "76JG032JT7CD",
    "MERC": "888889",
    "SESS": "f2d209d0d4cf4c37b0481ff3adcbde00",
    "ORDR": "ORDR-1567540565",
    "AUTO": "A",
    "SCOR": "28",
    "GEOX": "US",
    "BRND": "VISA",
    "REGN": "US_ID",
    "NETW": "N",
    "KAPT": "Y",
    "CARDS": "1",
    "DEVICES": "1",
    "EMAILS": "1",
    "VELO": "0",
    "VMAX": "0",
    "SITE": "DEFAULT",
    "DEVICE_LAYERS": "DF651ACF30..99CF09F417.E3D16F2CB7.061826EF2B",
    "FINGERPRINT": "290D1C0172364AADAC25D9FD0B13D946",
    "TIMEZONE": "360",
    "LOCALTIME": "2019-09-03 13:56",
    "REGION": "US_ID",
    "COUNTRY": "US",
    "PROXY": "N",
    "JAVASCRIPT": "Y",
    "FLASH": "N",
    "COOKIES": "Y",
    "HTTP_COUNTRY": "US",
    "LANGUAGE": "EN",
    "MOBILE_DEVICE": "N",
    "MOBILE_TYPE": null,
    "MOBILE_FORWARDER": "N",
    "VOICE_DEVICE": "N",
    "PC_REMOTE": "N",
    "RULES_TRIGGERED": 3,
	"RULE_ID_0": "183762",
	"RULE_DESCRIPTION_0": "DECLINE: More than 4 Unique Email Addresses",
	"RULE_ID_1": "183764",
	"RULE_DESCRIPTION_1": "DECLINE: More than 4 Unique Credit Cards",
	"RULE_ID_2": "183774",
	"RULE_DESCRIPTION_2": "REVIEW: Distance from Device to Billing > 1000 km and Persona Score > 50",
    "COUNTERS_TRIGGERED": 0,
    "REASON_CODE": null,
    "DDFS": "2019-08-22",
    "DSR": "1050x1680",
    "UAS": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/76.0.3809.100 Safari/537.36",
    "BROWSER": "Chrome 76.0.3809.100",
    "OS": "Mac OS X 10.14.6",
    "PIP_IPAD": null,
    "PIP_LAT": null,
    "PIP_LON": null,
    "PIP_COUNTRY": null,
    "PIP_REGION": null,
    "PIP_CITY": null,
    "PIP_ORG": null,
    "IP_IPAD": "208.75.113.3",
    "IP_LAT": "43.6337",
    "IP_LON": "-116.2004",
    "IP_COUNTRY": "US",
    "IP_REGION": "Idaho",
    "IP_CITY": "Boise",
    "IP_ORG": "UNKNOWN",
    "OMNISCORE": 54,
    "3D_SECURE_MERCHANT_RESPONSE": "Challenge"
    "WARNING_COUNT": 0
} 
```

### Kount recommends at the minimum the following methods/functions used in the RIS response: 

RIS response Java method examples: 

<table class="tg">
  <tr>
    <td class="tg-0pky">﻿MERC</td>
    <td class="tg-0pky">getMerchantId()</td>
  </tr>
  <tr>
    <td class="tg-gaf0">MODE</td>
    <td class="tg-gaf0">getMode()</td>
  </tr>
  <tr>
    <td class="tg-0pky">TRAN</td>
    <td class="tg-0pky">getTransactionId()</td>
  </tr>
  <tr>
    <td class="tg-btxf">ORDR</td>
    <td class="tg-btxf">getOrderNumber()</td>
  </tr>
  <tr>
    <td class="tg-0pky">AUTO</td>
    <td class="tg-0pky">getAuto()</td>
  </tr>
  <tr>
    <td class="tg-pcvp">SCOR</td>
    <td class="tg-pcvp">getScore()</td>
  </tr>
  <tr>
    <td class="tg-0pky">KAPT</td>
    <td class="tg-0pky">getKaptcha()</td>
  </tr>
  <tr>
    <td class="tg-pcvp">SITE</td>
    <td class="tg-pcvp">getSite()</td>
  </tr>
  <tr>
    <td class="tg-0pky">WARNING</td>
    <td class="tg-0pky">hasWarnings()</td>
  </tr>
  <tr>
    <td class="tg-pcvp"></td>
    <td class="tg-pcvp">getWarningCount()</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">getWarnings()</td>
  </tr>
  <tr>
    <td class="tg-pcvp">ERROR</td>
    <td class="tg-pcvp">hasErrors()</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">getErrorCount()</td>
  </tr>
  <tr>
    <td class="tg-pcvp"></td>
    <td class="tg-pcvp">getErrors()</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">getErrorCodes()</td>
  </tr>
</table>
