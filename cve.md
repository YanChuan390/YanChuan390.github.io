---
layout: page
title: CVEs
---

<!--p class="message">
<i class="fa fa-star"></i> We got some vulnerabilities on the latest Android 12! Have a look now! 
</p-->

## Table of Common Vulnerabilities and Exposures (CVEs) found in this study

| CVE ID         | Affected Devices | Involved UUIs  | Severity* | Vendor Advisory<sup>$</sup>                                  |
|----------------|------------------|----------------|------------|---------------------------------------------------------------|
| CVE-2020-12489 | Vivo (G10)       | Serial         | 5.5 MEDIUM | [[**Link**](https://www.vivo.com/en/support/security-advisory-detail?id=5){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2020-12488.png){:target="_blank"}] |
| CVE-2020-14103 | Xiaomi (H10, H11) | Serial         | 5.5 MEDIUM | [[**Link**](https://trust.mi.com/misrc/bulletins/advisory?cveId=41){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2020-14103.png){:target="_blank"}]        |
| CVE-2020-14105 | Xiaomi (H10, H11) | Misc UUI (sno) | 5.5 MEDIUM | [[**Link**](https://trust.mi.com/misrc/bulletins/advisory?cveId=48){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2020-14105.png){:target="_blank"}]        |
| CVE-2021-0428  | Pixel (AOSP 10)  | ICCID          | 5.5 MEDIUM | [[**Link**](https://source.android.com/docs/security/bulletin/2021-09-01){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/av-2021-0428.png){:target="_blank"}]  |
| CVE-2021-25344 | Samsung (E10)    | Serial         | 5.5 MEDIUM | [[**Link**](https://security.samsungmobile.com/securityUpdate.smsb){:target="_blank"}<sup>+</sup>, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2021-25344.png){:target="_blank"}]       |
| CVE-2021-25358 | Samsung (E10)    | IMSI           | 3.3 LOW    | [[**Link**](https://security.samsungmobile.com/securityUpdate.smsb){:target="_blank"}<sup>#</sup>, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2021-25358.png){:target="_blank"}]       |
| CVE-2021-26278 | Vivo (G10)       | WiFi MAC       | 6.3 MEDIUM | [[**Link**](https://www.vivo.com/en/support/security-advisory-detail?id=7){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2021-26278.png){:target="_blank"}] |
| CVE-2021-37055 | Huawei (A10)     | ICCID          | 5.3 MEDIUM | [[**Link**](https://consumer.huawei.com/en/support/bulletin/2021/9/){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2020-12488.png){:target="_blank"}]      |

<!--
| CVE-2022-30753 <sup>new</sup> | Samsung    | Device ID          | 3.3 LOW | [[**Link**](https://security.samsungmobile.com/securityUpdate.smsb?year=2022&month=7){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2022-30753.png){:target="_blank"}]      |
| CVE-2022-27822 <sup>new</sup> | Samsung    | Misc UUI (EF_RUIMID)  | 5.5 MEDIUM | [[**Link**](https://security.samsungmobile.com/securityUpdate.smsb?year=2022&month=4){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2022-27822.png){:target="_blank"}]      |
| CVE-2022-22272 <sup>new</sup> | Samsung     | IMSI              | 3.3 LOW | [[**Link**](https://security.samsungmobile.com/securityUpdate.smsb?year=2022&month=1){:target="_blank"}, [**Snapshot**]({{ site.baseurl }}/snapshots/vendor-advisory/va-2022-22272.png){:target="_blank"}]      |
-->

\* According to NIST NVD CVSS 3.x Severity and Metrics scoring standard.  
$ All the URLs listed are accessed on 20 September 2022.  
\+ In the section "SMR-MAR-2021" of the webpage.  
\# In the section "SMR-APR-2021" of the webpage.

<p>    </p>

## More details about CVE-2021-0428 
#### SubscriptionInfo.getIccid() in Android 10

We found an issue in *SubscriptionInfo.getIccid( )* and reported to Google. The vulnerability is later confirmed by Google [[**Snapshot of Google's IssueTracker Website**]({{ site.baseurl }}/docs/public/google/IssueTracker.mhtml){:target="_blank"}] and registered with a CVE.

The fixing of this vulnerability turns out to be an unexpectedly non-trivial process.
During our assessment, we notice that the vulnerability in *getIccid( )* only exists in Android 10 and is not inherited by Android 11 and later releases.  

This may be because Google has been aware of this issue and has fixed it in AOSP 11, or it may have unintentionally fixed that vulnerability during the development process.  

After we reported it, Google issued a warning in its security bulletin on 5th Apr 2021 [[**link**](https://source.android.com/security/bulletin/2021-04-01){:target="_blank"}], which confirms the issue has been fixed.  
However, later in June 2021, the "fix" was recalled as shown in an updated version of the security bulletin.
Google explained that the recall was because of *application compatibility issues*.  

Google later updated the comments in the source code of *getIccid( )* [[**Link to AOSP Repo**](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/telephony/java/android/telephony/SubscriptionInfo.java){:target="_blank"}], stating that the system-level permission for this method is imposed since Android 11 (API level 30) rather than Android 10 (API level 29).
This, however, contradicts Android's documentation and the policies on other UUIs, where the system-level permission is imposed since Android 10.

You can find more technical details of the fixing and recalling of this CVE from the [**slides**]({{ site.baseurl }}/docs/public/google/CVE20210428.pdf){:target="_blank"} prepared by us 
