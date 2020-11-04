# asusmerlin-scripts

These files are ones that I regularly use on my Asus Merlin AC68U

**bfs_portforward** is for Brute Force protection Port Forwarding. 
Just add this to your scripts folder and in nat-start add a line such as 
bfs_portforward HTTP up eth0 http 80 tcp 60 15

**healtcheck** is great for checking vpn tunnels.
Just add this to your scripts folder and in your openvpn up event script add this
healthcheck up $dev
In the openvpn downscript add
healthcheck down $dev

**Port_Knocking** is just for a little bit of security when opening up certain ports.
Just add this to your scripts folder. in your firewall-start add a line such as
port_knock SSH up 22 tcp 8881 7777 9991 30
