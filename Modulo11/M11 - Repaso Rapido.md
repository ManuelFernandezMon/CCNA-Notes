---
modulo: 11
tema: repaso
tipo: repaso
tags: [ITN, modulo11, repaso, flashcards, subnetting, examen]
---

# ⚡ Repaso Rapido — Modulo 11

> [!tip] 📖 Como usar este repaso
> El subneteo se domina practicando. Intenta resolver cada ejercicio antes de ver la respuesta. ✅

---

> [!question] ¿Que es ANDing y para que sirve?
>> [!done]- ✅ Respuesta
>> Es la operacion AND logica bit por bit entre la IP y la mascara para obtener la **direccion de red**. Solo `1 AND 1 = 1`, todo lo demas da 0.

---

> [!question] En 192.168.10.0/24, ¿cuales son las 3 direcciones especiales?
>> [!done]- ✅ Respuesta
>> - **Red**: 192.168.10.0 (todos los bits de host en 0)
>> - **Broadcast**: 192.168.10.255 (todos los bits de host en 1)
>> - **Hosts utilizables**: .1 a .254

---

> [!question] ¿Cuales son los 3 rangos de direcciones privadas (RFC 1918)?
>> [!done]- ✅ Respuesta
>> - `10.0.0.0/8` → 10.0.0.0 a 10.255.255.255
>> - `172.16.0.0/12` → 172.16.0.0 a 172.31.255.255
>> - `192.168.0.0/16` → 192.168.0.0 a 192.168.255.255

---

> [!question] ¿Que es 169.254.x.x y que indica?
>> [!done]- ✅ Respuesta
>> Direccion **APIPA / link-local**. Indica que el DHCP **no respondio** y el host se auto-asigno una direccion.

---

> [!question] ¿Que dispositivo detiene los broadcasts? ¿Cual los propaga?
>> [!done]- ✅ Respuesta
>> - El **router** DETIENE los broadcasts (cada interfaz = dominio separado)
>> - El **switch** los PROPAGA por todas sus interfaces

---

> [!question] ¿Cuales son las dos formulas clave del subneteo?
>> [!done]- ✅ Respuesta
>> - **# subredes** = 2^(bits prestados)
>> - **# hosts utilizables** = 2^(bits de host) − 2

---

> [!question] ¿Que es el numero magico y como se calcula?
>> [!done]- ✅ Respuesta
>> El tamaño de cada bloque de subred. **256 − (octeto de la mascara)**.
>> Ejemplo: /26 = mascara .192 → 256 − 192 = 64. Las subredes van de 64 en 64.

---

> [!question] Subnetea 192.168.10.0/26 — lista las 4 subredes.
>> [!done]- ✅ Respuesta
>> Numero magico = 64:
>> - 192.168.10.0 (hosts .1-.62, broadcast .63)
>> - 192.168.10.64 (hosts .65-.126, broadcast .127)
>> - 192.168.10.128 (hosts .129-.190, broadcast .191)
>> - 192.168.10.192 (hosts .193-.254, broadcast .255)

---

> [!question] ¿Que es VLSM y cual es su regla de oro?
>> [!done]- ✅ Respuesta
>> **Variable Length Subnet Mask** — permite usar diferentes mascaras para diferentes subredes, evitando desperdicio.
>> **Regla de oro**: empieza siempre por la subred **mas grande** y avanza hacia las mas pequeñas.

---

> [!question] ¿Por que VLSM es ideal para enlaces WAN?
>> [!done]- ✅ Respuesta
>> Un enlace WAN punto a punto solo necesita 2 direcciones. Con VLSM usas /30 (2 hosts) en vez de desperdiciar 28+ direcciones con una mascara grande.

---

## 📊 Tabla maestra de subneteo (memorizar)

```
  SUBNETEO DE UN /24
  Prefijo  Mascara          Magico  Subredes  Hosts
  ───────  ───────────────  ──────  ────────  ─────
  /25      255.255.255.128   128       2       126
  /26      255.255.255.192    64       4        62
  /27      255.255.255.224    32       8        30
  /28      255.255.255.240    16      16        14
  /29      255.255.255.248     8      32         6
  /30      255.255.255.252     4      64         2

  POTENCIAS DE 2
  2^1=2   2^4=16   2^7=128    2^10=1024
  2^2=4   2^5=32   2^8=256    2^11=2048
  2^3=8   2^6=64   2^9=512    2^12=4096
```

---

## 🗺 Mapa completo del modulo

```
  DIRECCIONAMIENTO IPv4
  ├── ESTRUCTURA: red + host · mascara · ANDing · prefijo
  ├── 3 DIRECCIONES: red (todos 0) · broadcast (todos 1) · hosts
  ├── TRANSMISION: unicast · broadcast · multicast (224-239)
  ├── TIPOS: publicas · privadas (RFC1918) · loopback · APIPA
  ├── NAT: privada → publica en el router perimetral
  ├── SEGMENTACION: routers detienen broadcasts · subnetear
  ├── SUBNETEO: tomar bits prestados · numero magico
  └── VLSM: mascaras variables · de mayor a menor · sin desperdicio
```

---

🔗 [[MOC - Modulo 11 Direccionamiento IPv4]]

*#ITN #modulo11 #repaso #flashcards #subnetting #VLSM #examen*
