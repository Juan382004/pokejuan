# ☁️ Guía para Crear una Cuenta en Azure y Configurar una Red Virtual Estática

## 📌 Índice

1. [Creación de una Cuenta en Azure](#1-creación-de-una-cuenta-en-azure)
2. [Configuración de una Red Virtual Estática](#2-configuración-de-una-red-virtual-estática)
3. [Conclusión](#3-conclusión)

---

## 1. 🧾 Creación de una Cuenta en Azure

Sigue estos pasos para crear tu cuenta en Microsoft Azure:

### ✅ Paso 1: Ir al Sitio Web de Azure

- Abre tu navegador y visita: [https://azure.microsoft.com](https://azure.microsoft.com)

### ✅ Paso 2: Iniciar el Registro

- Haz clic en el botón **"Empieza gratis"**.
- Selecciona **"Comenzar gratis"** para acceder al crédito gratuito inicial (USD 200 por 30 días).

### ✅ Paso 3: Iniciar Sesión o Crear Cuenta Microsoft

- Si ya tienes una cuenta Microsoft (como Outlook o Hotmail), inicia sesión.
- Si no, selecciona **"Crear una nueva cuenta"**.

### ✅ Paso 4: Verificación de Identidad

- **Teléfono:** Se enviará un código de verificación SMS.
- **Tarjeta de Crédito:** Se realiza una verificación simbólica (no se te cobra).

### ✅ Paso 5: Finalizar Registro

- Acepta los términos y condiciones.
- Haz clic en **"Registrarse"**.

---

## 2. 🌐 Configuración de una Red Virtual Estática

Una red virtual (VNet) en Azure permite que varios recursos se comuniquen de manera segura. Aquí te explico cómo crear una VNet con una subred de IP estática.

### 🔧 Paso 1: Acceder al Portal de Azure

- Visita [https://portal.azure.com](https://portal.azure.com)
- Ve al buscador y escribe `Redes virtuales`, luego selecciona **"Crear"**.

### 🔧 Paso 2: Configurar la Red Virtual

1. **Nombre del recurso**:  
   Escribe un nombre descriptivo (ej. `vnet-pokedex`).

2. **Región**:  
   Selecciona la región más cercana a tus usuarios (ej. `East US`).

3. **Espacio de direcciones IPv4**:  
   Define un bloque CIDR, por ejemplo:  
   `10.0.0.0/16`

4. **Subred**:  
   Crea una subred dentro del bloque, por ejemplo:  
   - Nombre: `subnet-principal`  
   - Rango de IP: `10.0.1.0/24`

5. **Asignación IP Estática (Opcional)**:  
   Para una IP estática, crea una máquina virtual y luego:
   - Ve a la configuración de red.
   - Selecciona la interfaz de red (NIC).
   - Configura una IP privada estática manualmente.

## 3. ✅ Conclusión

Con estos pasos ya tienes:

- Una cuenta activa en Azure con crédito gratuito.
- Una red virtual configurada para tus recursos.
- Opcionalmente, una subred con IPs estáticas.

> 💡 **Recomendación:** Siempre usa nombres descriptivos para tus recursos y organiza por grupos de recursos según el proyecto.

---

### 📚 Referencias

- [Documentación oficial de Azure - Redes virtuales](https://learn.microsoft.com/es-es/azure/virtual-network/)
- [Planes gratuitos de Azure](https://azure.microsoft.com/es-es/free/)
