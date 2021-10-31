# tweak-findings
Stuff i found out abt Tweaking Windows. May include fixes for ur problems


## Intro

So you've ran some Windows Script from the Internet or even from trusted Stuff and now stuff you like to do doesnt work anympre?
Well heres some of my finding to WHY stuff doesnt work anymore.


### Cant change Profile Picture anymore.

Well. Thats easy to fix.
``Task Scheduler -> Microsoft -> Windows -> Shell -> Enable CreateObjectTask``

### Cannot get Store to download some Apps?

`Task Scheduler -> Microsoft -> Windows -> Subscription -> Enable Both Entries if disabled`

### Welp. cant Install and use WSL

`Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Mup -> Turn it on`

Then LxssManager Should work again

### Auto Regedit Backup is busted.

`Task Scheduler -> Microsoft -> Windows -> Regedit -> Enable Entry if disabled`
