---
modulo: 11
titulo: Direccionamiento IPv4
tipo: moc
tags: [ITN, modulo11, IPv4, subnetting, VLSM]
---

# 🧮 Modulo 11 — Direccionamiento IPv4

> [!abstract] 🎯 Objetivo
> Calcular un esquema de subneteo IPv4 para segmentar eficientemente una red.

---

## 🗺 Notas del modulo

| # | Nota | Tema clave |
|---|------|-----------|
| 11.1 | [[M11 - 11.1 Estructura de Direcciones IPv4]] | Red/Host · Mascara · ANDing · Prefijo |
| 11.2 | [[M11 - 11.2 Unicast Broadcast Multicast]] | Los 3 tipos de transmision |
| 11.3 | [[M11 - 11.3 Tipos de Direcciones IPv4]] | Publicas · Privadas · Loopback · APIPA |
| 11.4 | [[M11 - 11.4 Segmentacion de Red]] | Dominios de broadcast · Por que subnetear |
| 11.5 | [[M11 - 11.5 Subnetear una Red IPv4]] | Subneteo en /24 · Numero magico |
| 11.6 | [[M11 - 11.6 Subnetear 16 y 8]] | Prefijos /16 y /8 · Bits prestados |
| 11.7 | [[M11 - 11.7 Subnetear para Requisitos]] | Maximizar subredes · Minimizar desperdicio |
| 11.8 | [[M11 - 11.8 VLSM]] | Mascara de longitud variable |
| ⚡ | [[M11 - Repaso Rapido]] | Flashcards + Tablas maestras |

---

## 🧠 El gran concepto del modulo

```
╔══════════════════════════════════════════════════════════════╗
║  SUBNETEAR = dividir una red grande en redes mas pequeñas    ║
╠══════════════════════════════════════════════════════════════╣
║  ¿Por que?                                                   ║
║  • Reduce dominios de broadcast → menos congestion           ║
║  • Mejora seguridad (politicas entre subredes)               ║
║  • Mejor organizacion (por ubicacion, funcion, dispositivo)  ║
╠══════════════════════════════════════════════════════════════╣
║  ¿Como?                                                      ║
║  Tomar bits prestados de la porcion de HOST                  ║
║  para crear mas porciones de RED                             ║
╚══════════════════════════════════════════════════════════════╝
```

---

## ⚡ Tabla maestra de subneteo /24

| Prefijo | Mascara | Subredes | Hosts/subred |
|---------|---------|----------|--------------|
| `/25` | 255.255.255.128 | 2 | 126 |
| `/26` | 255.255.255.192 | 4 | 62 |
| `/27` | 255.255.255.224 | 8 | 30 |
| `/28` | 255.255.255.240 | 16 | 14 |
| `/29` | 255.255.255.248 | 32 | 6 |
| `/30` | 255.255.255.252 | 64 | 2 |

> [!tip] 💡 Formula clave
> - **Subredes** = 2^(bits prestados)
> - **Hosts utilizables** = 2^(bits de host) − 2
> (se restan 2: direccion de red + direccion de broadcast)

---

🔗 [[Indice General ITN]] · [[MOC - Modulo 10 Config Basica Router]]

*#ITN #modulo11 #IPv4 #subnetting #VLSM*
