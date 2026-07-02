---
modulo: 13
tema: repaso
tipo: repaso
tags: [ITN, modulo13, repaso, flashcards, examen]
---

# ⚡ Repaso Rapido — Modulo 13

> [!tip] 📖 Como usar este repaso
> Intenta responder antes de expandir. ✅

---

> [!question] ¿Que es ICMP y para que sirve?
>> [!done]- ✅ Respuesta
>> **Internet Control Message Protocol** — da informacion sobre problemas en el procesamiento de paquetes IP. No transporta datos de usuario, solo avisa de errores.

---

> [!question] ¿Cuales son los 3 mensajes ICMP comunes a IPv4 e IPv6?
>> [!done]- ✅ Respuesta
>> 1. **Accesibilidad al host** (Echo Request/Reply) → base del `ping`
>> 2. **Destino/servicio inalcanzable** → con codigo explicando por que
>> 3. **Tiempo excedido** → TTL/Hop Limit en 0 → base de `traceroute`

---

> [!question] ¿Cuales son los 4 mensajes de Neighbor Discovery en ICMPv6?
>> [!done]- ✅ Respuesta
>> - **RS/RA** → entre router y dispositivo (asignacion dinamica)
>> - **NS/NA** → entre dispositivos (DAD y resolucion de MAC)

---

> [!question] ¿Que es DAD y como funciona?
>> [!done]- ✅ Respuesta
>> **Deteccion de Direcciones Duplicadas**. El dispositivo envia un **NS** con su propia IP como objetivo. Si otro responde con **NA**, hay un duplicado.

---

> [!question] ¿Cuales son las 3 pruebas progresivas de ping?
>> [!done]- ✅ Respuesta
>> 1. **Loopback** (127.0.0.1 / ::1) → prueba el stack TCP/IP local
>> 2. **Default Gateway** → prueba la LAN
>> 3. **Host remoto** → prueba toda la ruta

---

> [!question] ¿Por que el primer ping frecuentemente falla?
>> [!done]- ✅ Respuesta
>> Porque necesita resolver la direccion primero (**ARP** en IPv4 o **ND** en IPv6) antes de enviar el Echo Request. Es normal, no indica un problema real.

---

> [!question] ¿Como funciona traceroute usando el TTL?
>> [!done]- ✅ Respuesta
>> Incrementa el TTL progresivamente (1, 2, 3...). Cada router donde el TTL llega a 0 responde con "Tiempo excedido", revelando cada salto de la ruta hasta el destino.

---

> [!question] ¿Que significa un asterisco (*) en traceroute?
>> [!done]- ✅ Respuesta
>> Un paquete **perdido o sin respuesta** en ese salto especifico. Ayuda a localizar el router problematico.

---

> [!question] ¿Por que un ping fallido no siempre significa que el host esta caido?
>> [!done]- ✅ Respuesta
>> Muchos administradores **bloquean ICMP** por razones de seguridad. La falta de respuesta puede ser una restriccion de firewall, no una falla real del host.

---

## 🗺 Mapa completo del modulo

```
  ICMP
  ├── PROPOSITO: avisar de problemas en el procesamiento IP
  ├── 3 MENSAJES COMUNES
  │   ├── Accesibilidad (Echo) → ping
  │   ├── Inalcanzable (con codigo de razon)
  │   └── Tiempo excedido (TTL/Hop Limit=0) → traceroute
  ├── ICMPv6 EXCLUSIVO (Neighbor Discovery)
  │   ├── RS/RA → asignacion dinamica de direccion
  │   └── NS/NA → DAD + resolucion de MAC
  ├── PING
  │   ├── Loopback → gateway → host remoto (escalera)
  │   └── Primer intento puede fallar (ARP/ND)
  └── TRACEROUTE
      ├── Incrementa TTL: 1,2,3... hasta destino
      └── * = paquete perdido en ese salto
```

---

🔗 [[MOC - Modulo 13 ICMP]]

*#ITN #modulo13 #repaso #flashcards #ICMP #ping #traceroute #examen*
