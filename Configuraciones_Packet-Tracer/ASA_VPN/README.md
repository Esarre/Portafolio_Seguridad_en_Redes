### Contexto

Se solicita configurar la topología de una empresa ficticia, con los siguientes objetivos principales:
- Configuración de los dispositivos de la topología considerando medidas de seguridad en Capa 2 y Capa 3.
- Configurar Firewall ASA y VPN según los requerimientos solicitados.
---

### Topología configurada

<img width="689" height="686" alt="imagen" src="https://github.com/user-attachments/assets/c8fe285d-b70f-4a48-974d-a707c74582d7" />

---

### Requisitos específicos
<p>
<ul>
Implementación en Capa 2
  <li>Interfaces no utilizadas de Switches no deben estar asignadas a VLAN1, y deben estar apagadas.</li>
  <li>Implementar seguridad de puertos con aprendizaje dinámico y máximo de 2 direcciones MAC, con desactivación de interfaces en caso de violación.</li>
  <li>Implementar mecanismo de estabilización con STP.</li>
  <li>Implementar control de tormentas al 20% (Broadcast) en interfaces que corresponda.</li>
  <li>Configurar DHCP Snooping en el dispositivo que corresponda, y considerar configurar un mecanismo para evitar un ataque de hambruna (DCHP Starvation) permitiendo solo 2 IPs por minuto.</li>
</ul>

- Implementación en Capa 3

</p>
---

### Configuraciones

<p> Se puede obtener el detalle de las configuraciones realizadas en la topología en el documento adjunto "Informe_configuraciones.pdf" </p>
---
