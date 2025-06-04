# Guía de Port Forwarding en el Router para SSH, HTTP y HTTPS


## 1. Configurar Port Forwarding para SSH en la Raspberry Pi

Para permitir conexiones SSH desde Internet hacia tu Raspberry Pi, abriremos un puerto externo (por ejemplo, 2222) y lo redirigiremos a la IP interna de la Raspberry Pi en el mismo puerto.

1. **Acceder a la interfaz web del router**
   - Abre un navegador y navega a la dirección del router (por ejemplo, `http://192.168.1.1` o `http://192.168.0.1`).  
   - Inicia sesión con credenciales de administrador.

2. **Localizar la sección de Port Forwarding (Reenvío de Puertos)**
   - El apartado puede llamarse “Port Forwarding”, “Virtual Server”, “NAT” o similar.

3. **Crear una nueva regla de reenvío**
   - **Nombre/Descripción**: SSH Raspberry (puede ser cualquier etiqueta descriptiva).  
   - **Protocolo**: TCP
   - **Puerto externo (External Port)**: `2222` 
   - **Dirección IP interna (Internal IP)**: IP local Raspberry
   - **Puerto interno (Internal Port)**: `2222`

---

## 2. Configurar Port Forwarding para HTTP (puerto 80) y HTTPS (puerto 443)

3. **Crear una regla para HTTP (puerto 80)**
   - **Nombre/Descripción**: HTTP Web Server  
   - **Protocolo**: TCP  
   - **Puerto externo (External Port)**: `80`  
   - **Dirección IP interna (Internal IP)**: IP local Raspberry
   - **Puerto interno (Internal Port)**: `80` 

4. **Crear una regla para HTTPS (puerto 443)**
   - **Nombre/Descripción**: HTTPS Web Server  
   - **Protocolo**: TCP  
   - **Puerto externo (External Port)**: `443`  
   - **Dirección IP interna (Internal IP)**: IP local Raspberry
   - **Puerto interno (Internal Port)**: `443` 

