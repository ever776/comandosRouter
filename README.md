# Redes

`> MODO USUARIO donde se puede consultar informacion del ROUTER SIN MODIFICARLA`

`# MODO PRIVILEGIADO donde se puede visualizar el ESTADO del router`

`(config)# MODO de configuracion GLOBAL permite una configuracion general`

`(config-line) MODO de configuracion de LINEA consola, telnet, SSH`
 `(config-if) MODO de configuracion de INTERFACE de un PUERTO`

### modo privilegiado
- enable 
### reiniciar (#)
- reload
### modo de configuracion GLOBAL
- configure terminal 
### cambiar en nombre al ROUTER (config)
- hostname nombre_del_router
### password para proteger el modo privilegiado (config)
- enable password nombre_de_la_contraseña
### mensaje de bienvenida (config)
- banner motd "Mensaje de bienvenida"
### guardar la configuracion del router #
- copy running-config startup-config
### modo de configuracion de LINEA consola
- line console 0

### password para ingresar al router (config-line)
- enable-password n_password /om
- password nombre_del_password
- login
---
### modo de configuracion de interfaz de un puerto usado como gateway
- interface nombre_puerto
### asignar la ip del gateway (config-if)
- ip address nro_de_ip nro_mascara
- no shutdown
---
### informacion de las interface del router #
- show ip interface
### informacion de las interfaces del router en una tabla #
- show ip interface brief
---
### Configuracion Telnet (config)
- line vty 0 2
- password nombre_password
---
### ingresar al router remotamente
- telnet ip_router
---
### wireshark
### para capturar datos de ip
- icmp
---
## ver la informacion 

- show version
- show flash
### configuracion inical del router
- show startup config
### muestra la configuracion actual del router que esta corriendo en la memoria
- show running-config
### comando para comentario (config-if)
- description
### Borrar la configuracion(#)
- erase startup-config
- write erase
- reload
---
- ejecutar comando ping
- ejecutar arp -a
- tracert dir_ip
- pc1 10.0.0.1 masc 255.0.0.0
- pc2 10.0.0.2 masc 255.0.0.0
- pc4 10.0.0.3 masc 255.0.0.0


192.168.43.220 diego
192.168.43.151 ever
192.168.43.143 ale

---

- dispositivos iguales - cable cruzado
- dispositivos diferentes - cable directo

- vty hasta 4 dispositivos simultaneamente

## Mostrar las Configuraciones de inicio (startup-config)(#)
- show running-config - (configuracion en memoria ram running) (podemos ver la contraseña para ingreso a la consola)
- show startup-config (configuracion de inicio del switch)
---
# Enrutamiento estatico

## configuracion de router
- enable
- configure terminal
- interface fastehernet0/0
- ip address 195.190.1.1 255.255.255.0
- no shutdown
---
- interface fastethernet0/1 
- ip address 195.190.3.1 255.255.255.0
- no shutdown
---
## enrutamiento statico (config)
- ip route (red de destino) (mascara) (red a travez del salto)
