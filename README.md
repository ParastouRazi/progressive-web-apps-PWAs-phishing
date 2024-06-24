# progressive-web-apps-PWAs-phishing
Phishing and malware installing by progressive web apps (PWAs) and detection

A new technique that can be used for phishing and possibly other malicious operations has been detailed in a post by security researcher mr.d0x. The method takes advantage of progressive web applications (PWAs). In this video, we go over what these apps are, why they might be harmful, how hackers could utilize them for their own gain, and how to protect against this threat.

Progressive web apps (PWAs):
PWAs are web technologies-based apps. In essence, these are webpages that mimic the appearance and functionality of native apps that are installed on the device.


With one significant exception, the overall concept is the same as applications developed on the Electron framework. Electron apps, which have a built-in browser, are similar to a "sandwich" made of a website (the filling) and a browser (the bread) that is used to operate that website. PWAs, on the other hand, show the same website using the engine of the user's installed browser, much like a sandwich without bread.

PWAs are supported by all current browsers, however, the most complete implementation is provided by Google Chrome and Chromium-based browsers (such as the Microsoft Edge browser included with Windows).

If the relevant website allows it, installing a PWA is quite easy. To confirm the installation, simply click on a discreet button located in the address bar of the browser.

Sysmon Detection:

Sysmon Events:

File created:
Image: C:\Program Files\Google\Chrome\Application\chrome.exe
TargetFilename: C:\Users\Administrator\Desktop\Microsoft Login.lnk

File created:
Image: C:\Program Files\Google\Chrome\Application\chrome.exe
TargetFilename: C:\Users\Administrator\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Chrome Apps


File created:
RuleName: technique_id=T1187,technique_name=Forced Authentication
Image: C:\Program Files\Google\Chrome\Application\chrome.exe
TargetFilename: C:\Users\Administrator\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Chrome Apps\Microsoft Login.lnk

File created:
RuleName: technique_id=T1187,technique_name=Forced Authentication
Image: C:\Program Files\Google\Chrome\Application\chrome.exe
TargetFilename: C:\Users\Administrator\AppData\Local\Google\Chrome\User Data\Default\Web Applications\_crx_cncogclafdofkhcjlicnmbdcccahmacn\Microsoft Login.lnk

File created:
RuleName: technique_id=T1187,technique_name=Forced Authentication
Image: C:\Program Files\Google\Chrome\Application\chrome.exe
TargetFilename: C:\Users\Administrator\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar\Microsoft Login.lnk

Process Create:
RuleName: technique_id=T1204,technique_name=User Execution
Image: C:\Program Files\Google\Chrome\Application\chrome_proxy.exe
Description: Google Chrome
Product: Google Chrome
Company: Google LLC
OriginalFileName: chrome_proxy.exe
CommandLine: "C:\Program Files\Google\Chrome\Application\chrome_proxy.exe"  --profile-directory=Default --app-id=cncogclafdofkhcjlicnmbdcccahmacn
CurrentDirectory: C:\Program Files\Google\Chrome\Application\
Hashes: SHA1=FAD6B8FC1BCC0DB04A2DF235DE5614239150CD28,MD5=F287362CE8B6FD317BE6CB3788E37505,SHA256=019DFF0268F12C3884D514CE2672F502F308E231C34BDE6679FD5777A20F68C6,IMPHASH=140FF2EF9713229377B0108CA6
ParentImage: C:\Windows\explorer.exe
ParentCommandLine: C:\Windows\Explorer.EXE /NOUACCHECK


Sysmon Event:
Registry value set:
RuleName: technique_id=T1543,technique_name=Service Creation
EventType: SetValue
Image: C:\Program Files\Google\Chrome\Application\chrome_proxy.exe
TargetObject: HKLM\System\CurrentControlSet\Services\bam\State\UserSettings\S-1-5-21-737678691-3956078732-2995625844-500\\Device\HarddiskVolume2\Program Files\Google\Chrome\Application\chrome.exe

Video :
https://www.youtube.com/watch?v=u1_EE5GLmqg
