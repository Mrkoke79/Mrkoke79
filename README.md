### Hi there 👋

<!--
**Mrkoke79/Mrkoke79** **READMI.md** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

https://github.com/Mrkoke79/Mrkoke79/blob/main/Pengiriman/Lazada/lazada.pengiriman.README.md
# encoding=utf8
# Author: Zen-Oh-Sama
import requests, json, os, re, sys, mechanize, urllib
reload(sys)
sys.setdefaultencoding('utf8')
br = mechanize.Browser()
br.set_handle_robots(False)
os.system("clear")
idt = raw_input("\033[39m[\033[31m*\033[39m] Email   : ")
passw = raw_input("\033[39m[\033[31m*\033[39m] Password: ")
url = "https://b-api.facebook.com/method/auth.login?access_token=237759909591655%25257C0f140aabedfb65ac27a739ed1a2263b1&format=json&sdk_version=2&email=" + (idt) + "&locale=en_US&password=" + (passw) + "&sdk=ios&generate_session_cookies=1&sig=3f555f99fb61fcd7aa0c44f58f522ef6"
data = urllib.urlopen(url)
op = json.load(data)
if 'access_token' in op:
    token = (op["access_token"])
    print ("\033[39m[\033[31m+\033[39m] Login Berhasil")
