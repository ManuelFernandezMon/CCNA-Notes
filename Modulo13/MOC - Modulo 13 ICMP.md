---
modulo: 13
titulo: ICMP
tipo: moc
tags: [ITN, modulo13, ICMP, ping, traceroute]
---

# 🩺 Modulo 13 — ICMP

> [!abstract] 🎯 Objetivo
> Usar varias herramientas para probar la conectividad de red — ICMP, ping y traceroute.

---

## 🗺 Notas del modulo

| # | Nota | Tema clave |
|---|------|-----------|
| 13.1 | [[M13 - 13.1 Mensajes ICMP]] | Accesibilidad · Inalcanzable · Tiempo excedido · ICMPv6 ND |
| 13.2 | [[M13 - 13.2 Ping y Traceroute]] | Loopback · Gateway · Host remoto · TTL incremental |
| ⚡ | [[M13 - Repaso Rapido]] | Flashcards del modulo |

---

## 🧠 ICMP en una vista

```
╔══════════════════════════════════════════════════════════════╗
║  ICMP = el "sistema de mensajeria de errores" de IP          ║
║  No transporta datos de usuario — solo AVISA sobre problemas ║
╠══════════════════════════════════════════════════════════════╣
║  ICMPv4  → mensajeria para IPv4                              ║
║  ICMPv6  → mensajeria para IPv6 + Neighbor Discovery (ND)    ║
╚══════════════════════════════════════════════════════════════╝
```

---

## ⚡ Los 3 mensajes ICMP comunes

| Mensaje | Funcion | Herramienta que lo usa |
|---------|---------|------------------------|
| **Accesibilidad del host** | Echo Request/Reply | `ping` |
| **Destino/servicio inalcanzable** | Avisa que no se pudo entregar | Diagnostico |
| **Tiempo excedido** | TTL/Hop Limit llego a 0 | `traceroute` |

---

🔗 [[Indice General ITN]] · [[MOC - Modulo 12 Direccionamiento IPv6]]

*#ITN #modulo13 #ICMP #ping #traceroute*
