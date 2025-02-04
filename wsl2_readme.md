# Running Docker with WSL2

- On windows terminal type look for your ip address for WSL2 by using the following command
```bash
ipconfig
```
Look for something that looks like this 
```bash
Ethernet adapter vEthernet (WSL (Hyper-V firewall)):
...
   IPv4 Address. . . . . . . . . . . : IP.ADDRESS.VAL
```

Then on your WSL2 terminal in this directory run the following
```
docker exec -it sitl ./Tools/autotest/sim_vehicle.py -v ArduPlane --frame quadplane --map --console -w --mavproxy-args="--out IP.ADDRESS.VAL:14550 --state-basedir=/tmp/mavlink-sitl"`
```
Where you need to change IP.ADDRESS.VAL to your value of the ip address, this will let you connect to QGC or Mission Planner

output add:172.18.64.1:14550
output add:127.0.0.1:14551
