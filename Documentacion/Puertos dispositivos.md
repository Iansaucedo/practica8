### Actualización de la Lista de Puertos y Configuración

#### Torre A

1. **Switch 1 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 2" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

2. **Switch 2 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 1" y "Switch 3" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

3. **Switch 3 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 2" y "Switch 4" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

4. **Switch 4 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 3" y "Switch 5" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

5. **Switch 5 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 4" y "Switch 6" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

6. **Switch 6 (2960)**
   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 5" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

#### Torre B

1. **Switch 1 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 2" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

2. **Switch 2 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 1" y "Switch 3" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

3. **Switch 3 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 2" y "Switch 4" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

4. **Switch 4 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 3" y "Switch 5" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

5. **Switch 5 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 4" y "Switch 6" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

6. **Switch 6 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 5" y "Switch 7" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

7. **Switch 7 (2960)**

   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 6" y "Switch 8" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

8. **Switch 8 (2960)**
   - **FastEthernet0/1 - 0/4**: 4 APs
   - **FastEthernet0/5 - 0/18**: 14 dispositivos cableados (PCs)
   - **FastEthernet0/19 - 0/20**: Enlaces múltiples a "Switch 7" (LACP)
   - **FastEthernet0/21 - 0/24**: Puertos de reserva

### Routers

1. **Router "R_Resi"**

   - Ubicación: Cuarto de equipos principal en el sótano 1 de la Torre A.
   - Conexiones:
     - **GigabitEthernet0/0**: Conectado al router del proveedor de Internet.
     - **GigabitEthernet0/1**: Conectado a `GigabitEthernet0/0` de `R_Principal`.

2. **Router "R_Principal"**
   - Ubicación: Cuarto de equipos principal en el sótano 1 de la Torre A.
   - Conexiones:
     - **GigabitEthernet0/0**: Conectado a `GigabitEthernet0/1` de `R_Resi`.
     - **GigabitEthernet0/1**: Conectado a `FastEthernet0` del `Server_Intranet`.
     - **GigabitEthernet0/2**: Conectado a la red interna de la residencia.

### Servidor

1. **Servidor de Intranet**
   - Ubicación: Cuarto de equipos principal en el sótano 1 de la Torre A.
   - Conexiones:
     - **FastEthernet0**: Conectado a `GigabitEthernet0/1` de `R_Principal`.

### Configuración General

#### Configuración de VTP

##### Configuración del Switch VTP Server (SwitchA1)

```plaintext
SwitchA1> enable
SwitchA1# configure terminal
SwitchA1(config)# vtp domain mydomain
SwitchA1(config)# vtp mode server
SwitchA1(config)# vtp password mypassword
SwitchA1(config)# exit
```

##### Configuración de los Switches VTP Client

```plaintext
Switch> enable
Switch# configure terminal
Switch(config)# vtp domain mydomain
Switch(config)# vtp mode client
Switch(config)# vtp password mypassword
Switch(config)# exit
```

#### Configuración de VLANs en el Switch VTP Server (SwitchA1)

```plaintext
SwitchA1> enable
SwitchA1# configure terminal
SwitchA1(config)# vlan 10
SwitchA1(config-vlan)# name Residencia
SwitchA1(config-vlan)# exit
SwitchA1(config)# vlan 20
SwitchA1(config-vlan)# name Administracion
SwitchA1(config-vlan)# exit
SwitchA1(config)# vlan 30
SwitchA1(config-vlan)# name EstudioDescanso
SwitchA1(config-vlan)# exit
SwitchA1(config)# vlan 40
SwitchA1(config-vlan)# name Management
SwitchA1(config-vlan)# exit
```

#### Configuración de Trunk Ports en los Switches

##### Configuración de Trunk Ports en el Switch VTP Server (SwitchA1)

```plaintext
SwitchA1> enable
SwitchA1# configure terminal
SwitchA1(config)# interface range gigabitethernet 0/1 - 0/2
SwitchA1(config-if-range)# switchport mode trunk
SwitchA1(config-if-range)# switchport trunk allowed vlan all
SwitchA1(config-if-range)# exit
```

##### Configuración de Trunk Ports en los Switches VTP Client

```plaintext
Switch> enable
Switch# configure terminal
Switch(config)# interface range gigabitethernet 0/1 - 0/2
Switch(config-if-range)# switchport mode trunk
Switch(config-if-range)# switchport trunk allowed vlan all
Switch(config-if-range)# exit
```

#### Configuración de Puertos de Acceso en los Switches

##### Configuración de Puertos de Acceso en los Switches

```plaintext
Switch> enable
Switch# configure terminal
Switch(config)# interface range fastethernet 0/1 - 0/10
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 10
Switch(config-if-range)# exit

Switch(config)# interface range fastethernet 0/11 - 0/20
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 20
Switch(config-if-range)# exit

Switch(config)# interface range fastethernet 0/21 - 0/24
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 30
Switch(config-if-range)# exit

Switch(config)# interface range gigabitethernet 0/1 - 0/2
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 40
Switch(config-if-range)# exit
```

#### Configuración de LACP para Enlaces Múltiples

##### Configuración de LACP en el Switch VTP Server (SwitchA1)

```plaintext
SwitchA1> enable
SwitchA1# configure terminal
SwitchA1(config)# interface range fastethernet 0/19 - 0/20
SwitchA1(config-if-range)# channel-group 1 mode active
SwitchA1(config-if-range)# exit
SwitchA1(config)# interface port-channel 1
SwitchA1(config-if)# switchport mode trunk
SwitchA1(config-if)# switchport trunk allowed vlan all
SwitchA1(config-if)# exit
```

##### Configuración de LACP en los Switches VTP Client

```plaintext
Switch> enable
Switch# configure terminal
Switch(config)# interface range fastethernet 0/19 - 0/20
Switch(config-if-range)# channel-group 1 mode active
Switch(config-if-range)# exit
Switch(config)# interface port-channel 1
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk allowed vlan all
Switch(config-if)# exit
```

### Configuración de Routers y Conexiones

#### Configuración del Router "R_Resi"

```plaintext
R_Resi> enable
R_Resi# configure terminal
R_Resi(config)# interface gigabitethernet 0/0
R_Resi(config-if)# ip address 20.7.77.14 255.255.192.0
R_Resi(config-if)# no shutdown
R_Resi(config-if)# exit
R_Resi(config)# ip route 0.0.0.0 0.0.0.0 20.7.127.254
R_Resi(config)# exit
```

#### Configuración del Router "R_Principal"

```plaintext
R_Principal> enable
R_Principal# configure terminal
R_Principal(config)# interface gigabitethernet 0/0
R_Principal(config-if)# ip address 192.168.1.1 255.255.255.0
R_Principal(config-if)# no shutdown
R_Principal(config-if)# exit

R_Principal(config)# interface gigabitethernet 0/1
R_Principal(config-if)# ip address 192.168.2.1 255.255.255.0
R_Principal(config-if)# no shutdown
R_Principal(config-if)# exit

R_Principal(config)# interface gigabitethernet 0/2
R_Principal(config-if)# ip address 192.168.3.1 255.255.255.0
R_Principal(config-if)# no shutdown
R_Principal(config-if)# exit

R_Principal(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.2
R_Principal(config)# exit
```

#### Configuración del Servidor de Intranet

```plaintext
Server_Intranet> enable
Server_Intranet# configure terminal
Server_Intranet(config)# interface fastethernet 0
Server_Intranet(config-if)# ip address 192.168.2.2 255.255.255.0
Server_Intranet(config-if)# no shutdown
Server_Intranet(config-if)# exit
Server_Intranet(config)# ip default-gateway 192.168.2.1
Server_Intranet(config)# exit
```

### Conexiones Físicas

1. **Conexión entre "R_Resi" y el Router del Proveedor de Internet**:

   - Utiliza un cable Ethernet cruzado.
   - Conecta `GigabitEthernet0/0` de `R_Resi` al puerto correspondiente del router del proveedor de Internet.

2. **Conexión entre "R_Resi" y "R_Principal"**:

   - Utiliza un cable Ethernet.
   - Conecta `GigabitEthernet0/1` de `R_Resi` a `GigabitEthernet0/0` de `R_Principal`.

3. **Conexión entre "R_Principal" y el Servidor de Intranet**:
   - Utiliza un cable Ethernet.
   - Conecta `GigabitEthernet0/1` de `R_Principal` a `FastEthernet0` del `Server_Intranet`.

### Resumen de la Configuración

1. Configura `SwitchA1` como servidor VTP.
2. Configura los demás switches como clientes VTP.
3. Configura las VLANs en `SwitchA1`.
4. Configura los puertos de enlace troncal (trunk) en los switches.
5. Configura los puertos de acceso en los switches para asignar dispositivos a las VLANs correspondientes.
6. Configura LACP para enlaces múltiples en los switches.
7. Configura `R_Resi` con la IP 20.7.77.14/18 y la ruta por defecto hacia 20.7.127.254.
8. Configura `R_Principal` con las IPs 192.168.1.1, 192.168.2.1 y 192.168.3.1.
9. Configura el `Server_Intranet` con la IP 192.168.2.2 y la puerta de enlace 192.168.2.1.
10. Conecta `R_Resi` al router del proveedor de Internet, `R_Principal` y el `Server_Intranet` utilizando cables Ethernet.

### Configuración de DHCP en el Router "R_Principal"

#### Paso 1: Configuración del Servicio DHCP en el Router "R_Principal"

```plaintext
R_Principal> enable
R_Principal# configure terminal

# Configuración del pool DHCP para la VLAN 10 (Residencia)
R_Principal(config)# ip dhcp pool VLAN10
R_Principal(dhcp-config)# network 192.168.10.0 255.255.255.0
R_Principal(dhcp-config)# default-router 192.168.10.1
R_Principal(dhcp-config)# dns-server 8.8.8.8
R_Principal(dhcp-config)# exit

# Configuración del pool DHCP para la VLAN 20 (Administración)
R_Principal(config)# ip dhcp pool VLAN20
R_Principal(dhcp-config)# network 192.168.20.0 255.255.255.128
R_Principal(dhcp-config)# default-router 192.168.20.1
R_Principal(dhcp-config)# dns-server 8.8.8.8
R_Principal(dhcp-config)# exit

# Configuración del pool DHCP para la VLAN 30 (Estudio y descanso)
R_Principal(config)# ip dhcp pool VLAN30
R_Principal(dhcp-config)# network 192.168.30.0 255.255.255.192
R_Principal(dhcp-config)# default-router 192.168.30.1
R_Principal(dhcp-config)# dns-server 8.8.8.8
R_Principal(dhcp-config)# exit

# Configuración del pool DHCP para la VLAN 40 (Management)
R_Principal(config)# ip dhcp pool VLAN40
R_Principal(dhcp-config)# network 192.168.40.0 255.255.255.224
R_Principal(dhcp-config)# default-router 192.168.40.1
R_Principal(dhcp-config)# dns-server 8.8.8.8
R_Principal(dhcp-config)# exit

# Excluir direcciones IP del rango DHCP
R_Principal(config)# ip dhcp excluded-address 192.168.10.1 192.168.10.10
R_Principal(config)# ip dhcp excluded-address 192.168.20.1 192.168.20.10
R_Principal(config)# ip dhcp excluded-address 192.168.30.1 192.168.30.10
R_Principal(config)# ip dhcp excluded-address 192.168.40.1 192.168.40.10
R_Principal(config)# exit
```

#### Paso 2: Configuración de DHCP Relay en los Switches

Para redirigir las peticiones DHCP de los clientes a través de diferentes VLANs, configura el DHCP Relay en los switches.

##### Configuración de DHCP Relay en los Switches

```plaintext
Switch> enable
Switch# configure terminal
Switch(config)# interface vlan 10
Switch(config-if)# ip helper-address 192.168.1.1
Switch(config-if)# exit

Switch(config)# interface vlan 20
Switch(config-if)# ip helper-address 192.168.1.1
Switch(config-if)# exit

Switch(config)# interface vlan 30
Switch(config-if)# ip helper-address 192.168.1.1
Switch(config-if)# exit

Switch(config)# interface vlan 40
Switch(config-if)# ip helper-address 192.168.1.1
Switch(config-if)# exit
```

### Resumen de la Configuración

1. Configura el servicio DHCP en el router "R_Principal" para las VLANs 10, 20, 30 y 40.
2. Excluye las direcciones IP del rango DHCP que no deben ser asignadas dinámicamente.
3. Configura el DHCP Relay en los switches para redirigir las peticiones DHCP a través de diferentes VLANs.

### Configuración de "R_Principal" y el Servidor de Intranet

#### Paso 1: Configuración de "R_Principal"

```plaintext
R_Principal> enable
R_Principal# configure terminal

# Configuración de interfaces
R_Principal(config)# interface gigabitethernet 0/0
R_Principal(config-if)# ip address 192.168.1.1 255.255.255.0
R_Principal(config-if)# no shutdown
R_Principal(config-if)# exit

R_Principal(config)# interface gigabitethernet 0/1
R_Principal(config-if)# ip address 192.168.2.1 255.255.255.0
R_Principal(config-if)# no shutdown
R_Principal(config-if)# exit

R_Principal(config)# interface gigabitethernet 0/2
R_Principal(config-if)# ip address 192.168.3.1 255.255.255.0
R_Principal(config-if)# no shutdown
R_Principal(config-if)# exit

# Configuración de la ruta por defecto para entregar todo el tráfico a "R_Resi"
R_Principal(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.2
R_Principal(config)# exit
```

#### Paso 2: Configuración del Servidor de Intranet

```plaintext
Server_Intranet> enable
Server_Intranet# configure terminal

# Configuración de la interfaz de red
Server_Intranet(config)# interface fastethernet 0
Server_Intranet(config-if)# ip address 192.168.2.2 255.255.255.0
Server_Intranet(config-if)# no shutdown
Server_Intranet(config-if)# exit

# Configuración de la puerta de enlace predeterminada
Server_Intranet(config)# ip default-gateway 192.168.2.1
Server_Intranet(config)# exit

# Configuración del servicio HTTP
Server_Intranet(config)# ip http server
Server_Intranet(config)# exit
```

#### Paso 3: Configuración de la Conectividad IP entre "R_Resi" y "R_Principal"

```plaintext
R_Resi> enable
R_Resi# configure terminal

# Configuración de la interfaz de red
R_Resi(config)# interface gigabitethernet 0/0
R_Resi(config-if)# ip address 20.7.77.14 255.255.192.0
R_Resi(config-if)# no shutdown
R_Resi(config-if)# exit

R_Resi(config)# interface gigabitethernet 0/1
R_Resi(config-if)# ip address 192.168.1.2 255.255.255.0
R_Resi(config-if)# no shutdown
R_Resi(config-if)# exit

# Configuración de la ruta para alcanzar la red 192.168.2.0/24
R_Resi(config)# ip route 192.168.2.0 255.255.255.0 192.168.1.1
R_Resi(config)# exit
```

### Resumen de la Configuración

1. Configura las interfaces de red en "R_Principal" con las IPs 192.168.1.1, 192.168.2.1 y 192.168.3.1.
2. Configura la ruta por defecto en "R_Principal" para entregar todo el tráfico a "R_Resi".
3. Configura la interfaz de red y la puerta de enlace predeterminada en el Servidor de Intranet.
4. Habilita el servicio HTTP en el Servidor de Intranet.
5. Configura las interfaces de red en "R_Resi" con las IPs 20.7.77.14 y 192.168.1.2.
6. Configura la ruta en "R_Resi" para alcanzar la red 192.168.2.0/24 a través de "R_Principal".

### Configuración de "R_ISP" y Conexión a Internet

#### Paso 1: Configuración del Router "R_ISP"

```plaintext
R_ISP> enable
R_ISP# configure terminal

# Configuración de la interfaz de red conectada a "R_Resi"
R_ISP(config)# interface gigabitethernet 0/0
R_ISP(config-if)# ip address 20.7.127.254 255.255.192.0
R_ISP(config-if)# no shutdown
R_ISP(config-if)# exit

# Configuración de la interfaz de red conectada al PC
R_ISP(config)# interface gigabitethernet 0/1
R_ISP(config-if)# ip address 8.8.8.1 255.255.255.0
R_ISP(config-if)# no shutdown
R_ISP(config-if)# exit

# Configuración de la ruta por defecto
R_ISP(config)# ip route 0.0.0.0 0.0.0.0 20.7.77.14
R_ISP(config)# exit
```

#### Paso 2: Configuración de "R_Resi"

```plaintext
R_Resi> enable
R_Resi# configure terminal

# Configuración de la interfaz de red conectada a "R_ISP"
R_Resi(config)# interface gigabitethernet 0/0
R_Resi(config-if)# ip address 20.7.77.14 255.255.192.0
R_Resi(config-if)# no shutdown
R_Resi(config-if)# exit

# Configuración de la interfaz de red conectada a "R_Principal"
R_Resi(config)# interface gigabitethernet 0/1
R_Resi(config-if)# ip address 192.168.1.2 255.255.255.0
R_Resi(config-if)# no shutdown
R_Resi(config-if)# exit

# Configuración de la ruta por defecto para alcanzar Internet a través de "R_ISP"
R_Resi(config)# ip route 0.0.0.0 0.0.0.0 20.7.127.254
R_Resi(config)# exit
```

#### Paso 3: Configuración del PC conectado a "R_ISP"

```plaintext
PC> ip address 8.8.8.8 255.255.255.0
PC> ip default-gateway 8.8.8.1
```

### Resumen de la Configuración

1. **Configuración de "R_ISP"**:

   - Configura la interfaz `GigabitEthernet0/0` con la IP 20.7.127.254/18.
   - Configura la interfaz `GigabitEthernet0/1` con la IP 8.8.8.1/24.
   - Configura la ruta por defecto en "R_ISP" para entregar todo el tráfico a "R_Resi".

2. **Configuración de "R_Resi"**:

   - Configura la interfaz `GigabitEthernet0/0` con la IP 20.7.77.14/18.
   - Configura la interfaz `GigabitEthernet0/1` con la IP 192.168.1.2/24.
   - Configura la ruta por defecto en "R_Resi" para entregar todo el tráfico a "R_ISP".

3. **Configuración del PC conectado a "R_ISP"**:
   - Configura la IP del PC como 8.8.8.8/24.
   - Configura la puerta de enlace predeterminada del PC como 8.8.8.1.

### Configuración de NAT/PAT en "R_Resi"

Para permitir que todos los equipos internos de la red puedan navegar por Internet, configuraremos NAT/PAT en el router "R_Resi".

#### Paso 1: Configuración de NAT/PAT en "R_Resi"

```plaintext
R_Resi> enable
R_Resi# configure terminal

# Configuración de la interfaz interna (LAN)
R_Resi(config)# interface gigabitethernet 0/1
R_Resi(config-if)# ip nat inside
R_Resi(config-if)# exit

# Configuración de la interfaz externa (WAN)
R_Resi(config)# interface gigabitethernet 0/0
R_Resi(config-if)# ip nat outside
R_Resi(config-if)# exit

# Configuración de la lista de acceso para permitir el tráfico interno
R_Resi(config)# access-list 1 permit 192.168.0.0 0.0.255.255

# Configuración de NAT/PAT para traducir las direcciones IP internas a la IP externa
R_Resi(config)# ip nat inside source list 1 interface gigabitethernet 0/0 overload
R_Resi(config)# exit
```

#### Paso 2: Probar la Conectividad a Internet

Para probar que la configuración de NAT/PAT funciona correctamente, realiza un ping a la dirección IP 8.8.8.8 desde un dispositivo interno.

##### Probar desde un PC Interno

```plaintext
PC> ping 8.8.8.8
```

### Resumen de la Configuración

1. **Configuración de NAT/PAT en "R_Resi"**:

   - Configura la interfaz `GigabitEthernet0/1` como `ip nat inside`.
   - Configura la interfaz `GigabitEthernet0/0` como `ip nat outside`.
   - Configura una lista de acceso para permitir el tráfico interno.
   - Configura NAT/PAT para traducir las direcciones IP internas a la IP externa.

2. **Probar la Conectividad a Internet**:
   - Realiza un ping a la dirección IP 8.8.8.8 desde un dispositivo interno para verificar que la configuración de NAT/PAT funciona correctamente.

### Modelado de la Red con Dispositivos Finales

Para modelar la red utilizando dispositivos finales como PC, Laptop, y Server, así como PCs para representar centros de control domótico y televisiones, sigue los pasos a continuación.

#### Paso 1: Configuración de Dispositivos Finales

1. **PCs y Laptops**:

   - Conecta los PCs y Laptops a los switches correspondientes.
   - Configura las direcciones IP y puertas de enlace predeterminadas.

2. **Centros de Control Domótico y Televisiones**:
   - Representa los centros de control domótico y televisiones con PCs.
   - Conecta estos PCs a los switches correspondientes.
   - Configura las direcciones IP y puertas de enlace predeterminadas.

#### Ejemplo de Configuración de un PC

##### Configuración de un PC en la VLAN 10 (Residencia)

```plaintext
PC> ip address 192.168.10.11 255.255.255.0
PC> ip default-gateway 192.168.10.1
```

##### Configuración de un PC en la VLAN 20 (Administración)

```plaintext
PC> ip address 192.168.20.11 255.255.255.128
PC> ip default-gateway 192.168.20.1
```

##### Configuración de un PC en la VLAN 30 (Estudio y Descanso)

```plaintext
PC> ip address 192.168.30.11 255.255.255.192
PC> ip default-gateway 192.168.30.1
```

#### Paso 3: Probar la Conectividad a Internet

##### Probar desde un PC Interno

```plaintext
PC> ping 8.8.8.8
```

### Resumen de la Configuración

1. **Configuración de Dispositivos Finales**:
   - Conecta PCs, Laptops, y servidores a los switches correspondientes.
   - Configura las direcciones IP y puertas de enlace predeterminadas en los dispositivos.
