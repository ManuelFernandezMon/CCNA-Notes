---
modulo: 12
tema: repaso
tipo: repaso
tags: [ITN, modulo12, repaso, flashcards, IPv6, examen]
---

# ⚡ Repaso Rapido — Modulo 12

> [!tip] 📖 Como usar este repaso
> Intenta responder antes de expandir. ✅

---

> [!question] ¿Cuales son las 3 tecnicas de migracion a IPv6?
>> [!done]- ✅ Respuesta
>> 1. **Dual Stack** → ejecuta IPv4 e IPv6 simultaneamente (preferido)
>> 2. **Tunneling** → encapsula IPv6 dentro de IPv4
>> 3. **Translation (NAT64)** → traduce entre IPv6 e IPv4

---

> [!question] ¿Cuales son las 2 reglas para comprimir una direccion IPv6?
>> [!done]- ✅ Respuesta
>> - **Regla 1**: omitir ceros iniciales de cada hexteto (no los finales)
>> - **Regla 2**: `::` reemplaza una cadena de hextetos en cero (solo UNA vez)

---

> [!question] Comprime: 2001:0db8:0000:1111:0000:0000:0000:0200
>> [!done]- ✅ Respuesta
>> `2001:db8:0:1111::200`

---

> [!question] ¿Cuales son las 3 categorias de direcciones IPv6?
>> [!done]- ✅ Respuesta
>> - **Unicast** → una interfaz especifica
>> - **Multicast** → grupo de destinos
>> - **Anycast** → al dispositivo mas cercano del grupo
>> (IPv6 NO tiene broadcast)

---

> [!question] ¿Que diferencia hay entre GUA y LLA?
>> [!done]- ✅ Respuesta
>> - **GUA** → enrutable en Internet, como IP publica, empieza con **2000::/3**
>> - **LLA** → solo enlace local, NO enrutable, obligatoria, empieza con **FE80::/10**

---

> [!question] ¿Cual es el prefijo recomendado para LANs IPv6 y por que?
>> [!done]- ✅ Respuesta
>> **/64** — porque SLAAC usa 64 bits para el ID de interfaz y facilita la administracion de subredes.

---

> [!question] ¿Cuales son los 3 metodos del mensaje RA?
>> [!done]- ✅ Respuesta
>> 1. **SLAAC** → el dispositivo se configura solo, sin DHCP
>> 2. **SLAAC + DHCPv6 stateless** → SLAAC la GUA, DHCP la info extra
>> 3. **DHCPv6 stateful** → el servidor da todo (como IPv4)

---

> [!question] ¿Que hace el proceso EUI-64?
>> [!done]- ✅ Respuesta
>> Convierte la MAC de 48 bits en un ID de interfaz de 64 bits:
>> 1. Inserta **FFFE** en el medio de la MAC
>> 2. Invierte el 7º bit
>> Reconocible por el **ff:fe** en el medio.

---

> [!question] ¿Que significan FF02::1 y FF02::2?
>> [!done]- ✅ Respuesta
>> - **FF02::1** → multicast de todos los nodos (como broadcast)
>> - **FF02::2** → multicast de todos los routers

---

> [!question] ¿Como se subnetea en IPv6?
>> [!done]- ✅ Respuesta
>> Usando el campo **ID de subred** dedicado. Solo se incrementa el hexteto de la ID de subred. Con un ID de 16 bits → 65,536 subredes /64. Sin calcular mascaras ni preocuparse por desperdicio.

---

## 🗺 Mapa completo del modulo

```
  DIRECCIONAMIENTO IPv6
  ├── POR QUE: IPv4 agotado · migracion (dual-stack/tunnel/NAT64)
  ├── FORMATO: 128 bits hex · 8 hextetos
  │   Regla 1: omitir ceros iniciales
  │   Regla 2: :: para ceros consecutivos (una vez)
  ├── TIPOS: unicast · multicast · anycast (sin broadcast)
  ├── 2 UNICAST: GUA (2000::/3 enrutable) + LLA (FE80::/10 local)
  ├── CONFIG ESTATICA: ipv6 address X::1/64 + no shutdown
  ├── CONFIG DINAMICA: RS/RA · SLAAC · DHCPv6 · EUI-64
  ├── MULTICAST: FF00::/8 · FF02::1 nodos · FF02::2 routers
  └── SUBNETEO: campo ID subred · solo incrementar hexteto · /64
```

---

🔗 [[MOC - Modulo 12 Direccionamiento IPv6]]

*#ITN #modulo12 #repaso #flashcards #IPv6 #examen*
