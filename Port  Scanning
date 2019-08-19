#This is a simple port scanner based on the famous "Nmap" - Using Socket Library, By David Dvir.

import socket,time
list_of_services = ["ssh","http","ftp"]
ip = input("Target IP/Destination:\n")
port = 1
while port <= 1000:
    print(port)
    try:
        s = socket.socket()
        s.connect((ip,port))
        print("port {} is open".format(port))
        s.settimeout(5)
        banner = s.recv(2048).decode()
        for service in list_of_services:
            if service in banner.lower():
                print("the port {} is {}".format(port,service))
        s.close()

        port += 1
    except:
        #print("port {} is closed".format(port))
        port += 1
