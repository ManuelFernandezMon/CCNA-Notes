---
modulo: 14
titulo: Capa de Transporte
tipo: moc
tags: [ITN, modulo14, TCP, UDP, puertos, capa4]
---

# 🚚 Modulo 14 — Capa de Transporte

> [!abstract] 🎯 Objetivo
> Comparar el funcionamiento de los protocolos de la Capa de Transporte (TCP y UDP) en la comunicacion de extremo a extremo.

---

## 🗺 Notas del modulo

| # | Nota | Tema clave |
|---|------|-----------|
| 14.1 | [[M14 - 14.1 Transporte de Datos]] | Funcion de Capa 4 · Segmentacion · Multiplexacion |
| 14.2 | [[M14 - 14.2 TCP]] | Caracteristicas · Encabezado · Con estado |
| 14.3 | [[M14 - 14.3 UDP]] | Caracteristicas · Encabezado simple |
| 14.4 | [[M14 - 14.4 Numeros de Puerto]] | Sockets · Rangos de puertos · netstat |
| 14.5 | [[M14 - 14.5 Proceso de Comunicacion TCP]] | 3-way handshake · Terminacion sesion |
| 14.6 | [[M14 - 14.6 Confiabilidad y Control de Flujo]] | Secuencia · Retransmision · MSS |
| 14.7 | [[M14 - 14.7 Comunicacion UDP]] | Bajo overhead · Sin reordenar |
| ⚡ | [[M14 - Repaso Rapido]] | Flashcards del modulo |

---

## 🧠 TCP vs UDP — la decision fundamental

```
╔══════════════════════════════════════════════════════════════╗
║   TCP — CONFIABLE               UDP — RAPIDO                 ║
╠════════════════════════════════╦═══════════════════════════════╣
║  Orientado a conexion          ║  Sin conexion                ║
║  3-way handshake               ║  Envia directo                ║
║  Garantiza entrega             ║  Mejor esfuerzo               ║
║  Garantiza orden                ║  Sin garantia de orden        ║
║  Control de flujo               ║  Sin control de flujo         ║
║  Mayor overhead                 ║  Overhead minimo              ║
╠════════════════════════════════╬═══════════════════════════════╣
║  HTTP · FTP · SSH · Email      ║  DNS · DHCP · VoIP · Video    ║
╚════════════════════════════════╩═══════════════════════════════╝
```

---

## ⚡ Puertos bien conocidos — tabla de referencia

| Puerto | Protocolo | Servicio |
|--------|-----------|---------|
| 20/21 | TCP | FTP (datos/control) |
| 22 | TCP | SSH |
| 23 | TCP | Telnet |
| 25 | TCP | SMTP |
| 53 | UDP/TCP | DNS |
| 67/68 | UDP | DHCP (servidor/cliente) |
| 69 | UDP | TFTP |
| 80 | TCP | HTTP |
| 110 | TCP | POP3 |
| 143 | TCP | IMAP |
| 161 | UDP | SNMP |
| 443 | TCP | HTTPS |

---

🔗 [[Indice General ITN]] · [[MOC - Modulo 13 ICMP]]

*#ITN #modulo14 #TCP #UDP #puertos #capa4*
