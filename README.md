# tweak-findings
Stuff i found out abt Tweaking Windows. May include fixes for ur problems


### Intro

So you've ran some Windows Script from the Internet or even from trusted Stuff and now stuff you like to do doesnt work anymore?\
Well heres some of my finding to WHY stuff doesnt work anymore.


## Cant change Profile Picture anymore.

Well. Thats easy to fix.\
``Task Scheduler -> Microsoft -> Windows -> Shell -> Enable CreateObjectTask``

## Cannot get Store to download some Apps?

`Task Scheduler -> Microsoft -> Windows -> Subscription -> Enable Both Entries if disabled`

## Welp. cant Install and use WSL

`Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Mup -> Turn it on`

Then LxssManager Should work again

## Auto Regedit Backup is busted.

`Task Scheduler -> Microsoft -> Windows -> Regedit -> Enable Entry if disabled`

## I cant defrag anymore

`Start Defrag Service -> Open Cmd as Admin -> chkdsk *drive*: /f /r -> N -> Y -> Restart`

## I cant see the Internet Icon anymore

`CMD as Admin -> sc config "RmSvc" start=manual`

## Create new Recovery Partition

Download Windows ISO and unpack it to a folder.\
`Open CMD as Admin -> md c:\test -> dism /mount-image /imagefile:E:\UserFolders\Desktop\meow\sources\install.wim /index:1 /mountdir:C:\test\ /readonly`\
then\
`Go to C:\test\Windows\System32\Recovery -> copy the winRe.wim -> C:\Windows\System32\Recovery -> paste`\
and at last\
`reagentc /setreimage /path C:\windows\system32\recovery -> dism /unmount-image /mountdir:C:\test\ /discard -> reagentc /enable`

## Other Store Fix

Download ``https://www.tweaking.com/content/page/windows_repair_all_in_one.html``\
Select Portable and open it.\
In the Program itself, select Repairs and continue.\
Then Select all repairs and deselect them.\
After that select \
```1. Register System Files, 2. Repair Firewall, 3. Repair Hosts File, 4. Repair Network, 5. Repair Proxy Settings, 6. Repair App Store (Complete Reset), 7. Window Component Storage```.\
After that give it some time, reboot and it should work again.

## Fix Windows 11 Action Center.

```1. Go to Services -> Enable CDPSvc```

## AMD Chipset Driver crashes after selecting?

```Create New User -> Open the Exe and install it there.```

