---
title: Direcciones IP utilizadas por el Experience Cloud
description: Si el cortafuegos de su organización bloquea las direcciones IP que se originan en el Adobe, utilice esta lista para actualizar la configuración del cortafuegos.
exl-id: 1fca8d3b-ae8b-4095-96ef-d165f912b4c6
source-git-commit: faa9b8067a85f86cc0b559bdeeaed80df2339c7d
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 11%

---

# Direcciones IP utilizadas por el Experience Cloud

Algunas configuraciones de cortafuegos bloquean las direcciones IP procedentes de los servidores de recopilación de datos de Adobe o de los servidores responsables de acceder a datos. Puede utilizar esta lista de intervalos para modificar la configuración del cortafuegos de su organización y permitir el acceso y enviar datos desde su organización. Esta página incluye sistemas entrantes (como la recopilación de datos) y salientes (como las fuentes de datos en Adobe Analytics) que utiliza Adobe.

>[!IMPORTANT]
>
>Aunque Adobe hace todo lo posible para mantener este documento actualizado, no puede garantizar que la lista de intervalos de IP sea la misma. Los posibles cambios incluyen el crecimiento y la expansión del negocio, un registro de Internet requiere cambios en el espacio de direcciones IP del Adobe o un proveedor de servicios de Internet deja de funcionar.

Además de los bloques de direcciones IP que se enumeran a continuación, los productos de Adobe Experience Cloud individuales tienen sus propias direcciones IP que utilizan:

* [Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/technotes/ip-addresses)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/ip-addresses)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo#step-allowlist-marketo-ips)

## Todos los bloqueos de direcciones IP de Adobe

La siguiente tabla abarca todas las direcciones IP de propiedad del Adobe. Esta tabla incluye todas las oficinas de empleados de Adobe y los centros de datos que gestiona Adobe globalmente. No incluye servicios alojados en nubes públicas.

| Bloque IP (Notación CIDR) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.240.0/22` |

{style="table-layout:auto"}

## Bloques de direcciones IP de FTP y recopilación de datos de Adobe Experience Cloud

Si su organización prefiere permitir intervalos de direcciones IP específicos, puede hacer referencia a la siguiente tabla. Incluye:

* Servidores de recopilación de datos para todos los productos de Experience Cloud
* Servidores FTP para todos los productos de Experience Cloud

En la tabla anterior se incluyen todos los rangos de IP de esta sección.

| Ubicación | Intervalo IP (notación CIDR) |
| --- | --- |
| Australia | `63.140.55.0/24` |
| Australia | `63.140.56.0/23` |
| California | `63.140.32.0/23` |
| California | `63.140.34.0/24` |
| Francia | `63.140.62.0/23` |
| India | `66.117.20.0/24` |
| India | `66.117.22.0/23` |
| Japón | `130.248.169.0/23` |
| Japón | `63.140.50.0/23` |
| Japón | `66.117.31.0/24` |
| Londres | `66.235.156.0/24` |
| Londres | `185.34.188.0/22` |
| Londres | `130.248.152.0/22` |
| Londres | `130.248.244.0/23` |
| Oregón | `66.235.132.0/22` |
| Oregón | `130.248.130.0/23` |
| Oregón | `130.248.150.0/24` |
| Oregón | `130.248.160.0/21` |
| Oregón | `192.243.242.0/24` |
| Singapur | `130.248.170.0/23` |
| Singapur | `130.248.240.0/24` |
| Singapur | `63.140.44.0/22` |
| Singapur | `63.140.48.0/23` |
| Singapur | `66.117.30.0/24` |
| Singapur | `172.82.240.8/29` |
| Singapur | `172.82.240.88/29` |
| Virginia | `63.140.38.0/23` |
| Virginia | `63.140.54.0/24` |
| Virginia | `67.202.5.244` |

{style="table-layout:auto"}

Adobe Experience Cloud también admite IPv6 con capacidad limitada. Estos bloques de IP tienen fines de recopilación de datos similares a los de sus homólogos de IPv4 anteriores, pero no incluyen FTP.

| Ubicación | Host |
| --- | --- |
| Australia | `2406:da1c:406:1a00::/56` |
| Australia | `2406:da1c:ce5:b400::/56` |
| California | `2600:1f1c:366:d900::/56` |
| Francia | `2a05:d012:706:d000::/56` |
| India | `2406:da1a:f34:6a00::/56` |
| Irlanda | `2a05:d018:309:600::/56` |
| Japón | `2406:da14:b07:ab00::/56` |
| Oregón | `2600:1f14:1eb:7d00::/56` |
| Oregón | `2600:1f14:9d3:2b00::/56` |
| Singapur | `2406:da18:6e8:1e00::/56` |
| Virginia | `2600:1f18:1a20:e800::/56` |
| Virginia | `2600:1f18:4fd:6000::/56` |
| Virginia | `2600:1f18:b00:e100::/56` |
| Virginia | `2600:1f18:d1f:bd00::/56` |

>[!TIP]
>
>Las conexiones FTP para las funciones de exportación de Adobe Analytics (incluidas las fuentes de datos y las Datas Warehouse) solo se originan en direcciones IPv4 en las ubicaciones de Londres, Oregón y Singapur.
