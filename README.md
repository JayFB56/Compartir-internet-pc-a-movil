# Guía de Uso: Gnirehtet (Internet de PC a Android vía USB)

Este documento explica cómo compartir la conexión a internet de una computadora de oficina a un dispositivo Android utilizando el cable USB.

## ⚠️ Requisitos previos en el Celular

1. **Activar Opciones de Desarrollador:**
   - Ve a `Ajustes` > `Acerca del teléfono`.
   - Pulsa 7 veces seguidas sobre `Número de compilación`.
2. **Activar Depuración USB:**
   - Ve a `Ajustes` > `Sistema` > `Opciones de desarrollador`.
   - Activa el interruptor de **Depuración USB**.
3. **Autorizar la PC:**
   - Conecta el cable USB.
   - En la pantalla del celular aparecerá un mensaje: *"¿Permitir depuración USB?"*.
   - Marca la casilla **"Permitir siempre desde esta computadora"** y dale a **Aceptar**.

---

## 🚀 Pasos para la Ejecución

### 1. Abrir la Terminal (CMD)
Dirígete a la carpeta donde tienes el programa, haz clic en la barra de direcciones superior, escribe `cmd` y presiona `Enter`.

### 2. Verificar Conexión
Antes de iniciar, confirma que el dispositivo es visible para la PC:
```bash
adb devices
```
*Deberías ver un código alfanumérico seguido de la palabra `device`.*

### 3. Instalación (Solo la primera vez)
Instala el cliente necesario en tu teléfono:
```bash
gnirehtet install
```
*Espera a que aparezca el mensaje `Success`.*

### 4. Iniciar el Túnel de Internet
Para comenzar a navegar, ejecuta el siguiente comando:
```bash
gnirehtet run
```

---

## 📱 Acción en el Dispositivo
Una vez ejecutado el comando `run`, el teléfono solicitará permiso para crear una **Conexión VPN**. 
- Presiona **Aceptar** o **OK**.
- Aparecerá un icono de "llave" en la barra de notificaciones indicando que el internet está activo.

---

## 🛑 Cómo Detener el Servicio
Existen dos formas:
- Presiona `Ctrl + C` en la ventana del CMD.
- Cierra directamente la ventana negra (terminal).

## 💡 Consejos útiles
- **Modo de conexión:** Si no funciona, desliza la barra de notificaciones del celular y cambia el modo USB de "Solo carga" a **Transferencia de archivos (MTP)** o **PTP**.
- **Uso frecuente:** Para futuras ocasiones, ya no necesitas el comando `install`, simplemente conecta el cable y ejecuta `gnirehtet run`.
