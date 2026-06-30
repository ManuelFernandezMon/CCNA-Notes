---
modulo: 12
titulo: Direccionamiento IPv6
tipo: moc
tags: [ITN, modulo12, IPv6, GUA, LLA, SLAAC]
---

# 🌐 Modulo 12 — Direccionamiento IPv6

> [!abstract] 🎯 Objetivo
> Implementar un esquema de direccionamiento IPv6 — representacion, tipos de direcciones, configuracion estatica y dinamica, y subneteo.

---

## 🗺 Notas del modulo

| # | Nota | Tema clave |
|---|------|-----------|
| 12.1 | [[M12 - 12.1 Problemas de IPv4]] | Necesidad de IPv6 · Dual-stack · Tunneling |
| 12.2 | [[M12 - 12.2 Representacion de IPv6]] | Hextetos · Regla 1 (ceros) · Regla 2 (::) |
| 12.3 | [[M12 - 12.3 Tipos de Direcciones IPv6]] | GUA · LLA · Unicast/Multicast/Anycast |
| 12.4 | [[M12 - 12.4 Configuracion Estatica]] | ipv6 address · GUA y LLA manual |
| 12.5 | [[M12 - 12.5 Direccionamiento Dinamico GUA]] | RS/RA · SLAAC · DHCPv6 · EUI-64 |
| 12.6 | [[M12 - 12.6 Direccionamiento Dinamico LLA]] | LLA automatica · EUI-64 vs aleatorio |
| 12.7 | [[M12 - 12.7 Direcciones Multicast]] | FF02::1 · FF02::2 · Nodo solicitado |
| 12.8 | [[M12 - 12.8 Subnetear IPv6]] | ID de subred · /64 · Sin desperdicio |
| ⚡ | [[M12 - Repaso Rapido]] | Flashcards del modulo |

---

## 🧠 Las 2 direcciones que SIEMPRE tiene un dispositivo IPv6

```
╔══════════════════════════════════════════════════════════════╗
║  GUA (Global Unicast Address)                               ║
║  → Como una IP publica IPv4 · enrutable en Internet         ║
║  → Empieza con 2000::/3 (decimal 2 o 3)                     ║
╠══════════════════════════════════════════════════════════════╣
║  LLA (Link-Local Address)                                   ║
║  → Solo para el enlace local · NO enrutable                 ║
║  → Empieza con FE80::/10                                    ║
║  → OBLIGATORIA en toda interfaz IPv6                        ║
╚══════════════════════════════════════════════════════════════╝
```

---

## ⚡ Prefijos IPv6 clave de un vistazo

| Prefijo | Tipo |
|---------|------|
| `2000::/3` | GUA (global unicast, enrutable) |
| `FE80::/10` | LLA (link-local) |
| `FC00::/7` | ULA (local unica, tipo privada) |
| `FF00::/8` | Multicast |
| `FF02::1` | Multicast todos los nodos |
| `FF02::2` | Multicast todos los routers |
| `::1` | Loopback |

---

🔗 [[Indice General ITN]] · [[MOC - Modulo 11 Direccionamiento IPv4]]

*#ITN #modulo12 #IPv6 #GUA #LLA #SLAAC*
