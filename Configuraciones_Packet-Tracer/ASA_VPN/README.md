### <h1>Contexto</h1>

Se solicita configurar la topología de una empresa ficticia, con los siguientes objetivos principales:
- Configuración de los dispositivos de la topología considerando medidas de seguridad en Capa 2 y Capa 3.
- Configurar Firewall ASA y VPN según los requerimientos solicitados.
---

### <h1>Topología configurada</h1>

<img width="689" height="686" alt="imagen" src="https://github.com/user-attachments/assets/c8fe285d-b70f-4a48-974d-a707c74582d7" />

---

### <h1>Requisitos específicos</h1>
<p>
  <ul>
  <h2>Implementación en Capa 2</h2>
    <li>Interfaces no utilizadas de Switches no deben estar asignadas a VLAN1, y deben estar apagadas.</li>
    <li>Implementar seguridad de puertos con aprendizaje dinámico y máximo de 2 direcciones MAC, con desactivación de interfaces en caso de violación.</li>
    <li>Implementar mecanismo de estabilización con STP.</li>
    <li>Implementar control de tormentas al 20% (Broadcast) en interfaces que corresponda.</li>
    <li>Configurar DHCP Snooping en el dispositivo que corresponda, y considerar configurar un mecanismo para evitar un ataque de hambruna (DCHP Starvation) permitiendo solo 2 IPs por minuto.</li>
  </ul>

  <ul>
  <h2>Implementación en Capa 3</h2>
    <li>Direccionamiento IPv4 en toda la topología.</li>
    <li>Implementar Protocolo de Enrutamiento de Estado de Enlace, utilizando área de Blackbone. Configurar interfaces pasivas según corresponda.</li>
    <li>Implementar autenticación de protocolo de enrutamiento a nivel de interfaz.</li>
  </ul>

  <ul>
    <li>Definir nombres de zonas en Firewall ASA. Niveles de seguridad: INSIDE con el máximo nivel; DMZ con el 40% de INSIDE; OUTSIDE la mitad de DMZ.</li>
    <li>En Firewall ASA, configurar pool DHCP que proporcione direcciones IP de forma dinámica a zona INSIDE. Ofrecer no más de 16 direcciones IPv4.</li>
    <li>Implementar PAT para que zona INSIDE pueda salir por OUTSIDE. Implementar MPF para permitir el paso de ICMP.</li>
    <li>Permitir que PC-DMZ pueda salir por NAT estático hacia OUTSIDE. Utilizar IPv4 a elección del segmento de red. realizar la configuración para que paquetes ICMP response ingresen a DMZ.</li>
    <li>Permitir que el servidor "SERVICIOS" pueda acceder por TELNET hacia ASA.</li>
    <li>Implementar VPN Site-To-Site para que "PC-SITE-TO-SITEVPN" pueda llegar al servidor "SERVICIOS".</li>
  </ul>
</p>

---

### <h1>Configuraciones</h1>

<p> Se puede obtener el detalle de las configuraciones realizadas en la topología en el documento adjunto "Informe_configuraciones.pdf". </p>

---
