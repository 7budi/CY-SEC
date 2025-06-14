# Subdomain 
1)To find subdomains there is  a tool called sublist3r which is very easy to use.
Ex: sublist3r -d youtube.com.
2)There is also crt.com in website.
3)Another one is amass which is very good subdomain finder it's a bit complicated to use.
# Nmap
Its used to gain some information about the target like the ports its using, services and versions and so on.
EX: nmap -p- -T4 -A -vv -oA 192.aa.aa.aa.
We can use the -sU to scan the UDP but since its very slow we just scan the first 1000 ports  only.
