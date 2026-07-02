---
modulo: 14
tema: repaso
tipo: repaso
tags: [ITN, modulo14, repaso, flashcards, TCP, UDP, examen]
---

# ⚡ Repaso Rapido — Modulo 14

> [!tip] 📖 Como usar este repaso
> Intenta responder antes de expandir. ✅

---

> [!question] ¿Cuales son las 4 tareas de la Capa de Transporte?
>> [!done]- ✅ Respuesta
>> 1. Seguimiento de conversaciones individuales
>> 2. Segmentacion de datos y rearmado
>> 3. Agregar informacion de encabezado
>> 4. Multiplexar multiples conversaciones simultaneas

---

> [!question] ¿Cuales son las 4 caracteristicas de TCP?
>> [!done]- ✅ Respuesta
>> 1. **Establece sesion** (orientado a conexion)
>> 2. **Entrega confiable** (retransmite lo perdido)
>> 3. **Entrega en orden** (numeros de secuencia)
>> 4. **Control de flujo** (ajusta velocidad segun el receptor)

---

> [!question] ¿Cuales son las 4 caracteristicas de UDP?
>> [!done]- ✅ Respuesta
>> 1. Reconstruye en orden de **recepcion** (no reordena)
>> 2. Segmentos perdidos **NO se reenvian**
>> 3. **Sin** establecimiento de sesion
>> 4. El emisor **no sabe** la disponibilidad del receptor

---

> [!question] ¿Cuantos bytes tiene el encabezado UDP vs TCP?
>> [!done]- ✅ Respuesta
>> - **UDP**: 8 bytes, solo 4 campos
>> - **TCP**: 20+ bytes, muchos mas campos (secuencia, ACK, ventana, flags...)

---

> [!question] ¿Cuales son los 3 rangos de puertos?
>> [!done]- ✅ Respuesta
>> - **Bien conocidos**: 0–1,023 (apps comunes: HTTP, FTP, SSH)
>> - **Registrados**: 1,024–49,151 (apps especificas registradas)
>> - **Privados/Dinamicos (efimeros)**: 49,152–65,535 (asignados por el SO al cliente)

---

> [!question] ¿Que es un socket?
>> [!done]- ✅ Respuesta
>> La combinacion de **direccion IP + numero de puerto**. Ejemplo: `192.168.1.10:443`. Permite distinguir procesos y conexiones diferentes.

---

> [!question] Describe los 3 pasos del 3-Way Handshake
>> [!done]- ✅ Respuesta
>> 1. Cliente → **SYN** → Servidor
>> 2. Servidor → **SYN-ACK** → Cliente
>> 3. Cliente → **ACK** → Servidor
>> Conexion establecida.

---

> [!question] ¿Por que la terminacion de sesion TCP necesita 4 pasos?
>> [!done]- ✅ Respuesta
>> Cada direccion se cierra independientemente:
>> 1. Cliente → FIN
>> 2. Servidor → ACK
>> 3. Servidor → FIN
>> 4. Cliente → ACK
>> El servidor puede seguir enviando datos hasta enviar su propio FIN.

---

> [!question] ¿Cuales son los 6 flags de control TCP?
>> [!done]- ✅ Respuesta
>> **URG** (urgente) · **ACK** (confirmacion) · **PSH** (empuje) · **RST** (reinicio) · **SYN** (sincroniza) · **FIN** (fin de datos)

---

> [!question] ¿Que es SACK?
>> [!done]- ✅ Respuesta
>> **Selective Acknowledgement** — permite al receptor confirmar exactamente que segmentos recibio, incluso con huecos (segmentos discontinuos), en vez de solo "todo hasta X".

---

> [!question] ¿Como se calcula el MSS tipico con IPv4?
>> [!done]- ✅ Respuesta
>> MTU Ethernet (1500) − Header IPv4 (20) − Header TCP (20) = **1460 bytes**

---

> [!question] ¿Cuales son los 3 escenarios donde se prefiere UDP?
>> [!done]- ✅ Respuesta
>> 1. **Video/audio en vivo** (VoIP, streaming) — tolera perdida, no tolera retraso
>> 2. **Solicitud-respuesta simple** (DNS, DHCP)
>> 3. **Apps que manejan confiabilidad ellas mismas** (SNMP, TFTP)

---

## 🗺 Mapa completo del modulo

```
  CAPA DE TRANSPORTE
  ├── FUNCION: enlace app-red · segmenta · multiplexa
  ├── TCP
  │   ├── Orientado a conexion · confiable · ordenado · control flujo
  │   ├── Header 20+ bytes · con estado (stateful)
  │   ├── 3-Way Handshake: SYN → SYN-ACK → ACK
  │   ├── Terminacion (4 pasos): FIN→ACK→FIN→ACK
  │   ├── Secuencia + ACK + SACK + Ventana deslizante
  │   └── MSS = MTU - IP header - TCP header = 1460
  ├── UDP
  │   ├── Sin conexion · mejor esfuerzo · sin reordenar
  │   ├── Header 8 bytes · sin estado
  │   └── Usos: video en vivo, DNS/DHCP, SNMP/TFTP
  └── PUERTOS
      ├── Bien conocidos (0-1023) · Registrados (1024-49151) · Dinamicos (49152-65535)
      ├── Socket = IP + Puerto
      └── netstat → ver conexiones activas
```

---

🔗 [[MOC - Modulo 14 Capa de Transporte]]

*#ITN #modulo14 #repaso #flashcards #TCP #UDP #examen*
