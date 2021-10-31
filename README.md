# tweak-findings
Stuff i found out abt Tweaking Windows. May include fixes for ur problems


### Cant change Profile Picture anymore.

Well. Thats easy to fix. \n
`Task Scheduler -> Microsoft -> Windows -> Shell -> Enable CreateObjectTask`

### Cannot get Store to download some Apps?

`Task Scheduler -> Microsoft -> Windows -> Subscription -> Enable Both Entries if disabled`

### Welp. cant Install and use WSL

`Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Mup -> Turn it on`

Then LxssManager Should work again
