# 📘 Explicación completa de configuración Kiosk Browser (JSON)

Este documento explica **campo por campo** la configuración JSON utilizada en **Kiosk Browser Lockdown**, indicando:

- Qué hace cada opción
- Su traducción al español (entre paréntesis)
- Su impacto real en un entorno kiosko

Pensado para **uso interno, mantenimiento y soporte**.

---

## 🖼️ Screensaver (Salvapantallas)

```json
"screensaver_timeout": 5
```
**(Tiempo de espera del salvapantallas)**  
Minutos de inactividad antes de activar el salvapantallas.

```json
"custom_screensaver": false
```
**(Usar salvapantallas personalizado)**  
Si se usa contenido propio (imagen, vídeo o web).

```json
"custom_screensaver_type": "Image"
```
**(Tipo de salvapantallas personalizado)**  
Valores: Image, Video, Website.

```json
"screensaver_urls": "file:///android_asset/start.htm"
```
**(URL del salvapantallas)**  
Archivo local o web que se muestra como salvapantallas.

```json
"screensaver_slide_delay": 15
```
**(Tiempo entre diapositivas)**  
Segundos entre cambios de imagen.

```json
"screensaver_random": false
```
**(Mostrar salvapantallas aleatorio)**

---

## 🧰 Interfaz y navegación

```json
"hide_action_bar": true
```
**(Ocultar barra superior)**  
Evita acceso a controles del navegador.

```json
"display_toolbar_swipe_down": false
```
**(Mostrar barra con gesto)**  
Impide mostrar la barra deslizando hacia abajo.

```json
"show_browser_controls": false
```
**(Mostrar controles del navegador)**

```json
"show_home_icon": false
```
**(Mostrar icono inicio)**

```json
"show_back_icon": false
```
**(Mostrar botón atrás)**

```json
"show_forward_icon": false
```
**(Mostrar botón adelante)**

```json
"show_refresh_icon": false
```
**(Mostrar botón refrescar)**

```json
"show_bookmarks_icon": false
```
**(Mostrar icono marcadores)**

```json
"show_app_drawer_icon": false
```
**(Mostrar cajón de aplicaciones)**

---

## 🌐 Web principal

```json
"kiosk_url": "https://trabajador.controldejornadalaboral.es"
```
**(URL principal del kiosko)**  
Web que se carga siempre al iniciar.

```json
"custom_app_title": "Control de Jornada Laboral"
```
**(Título de la aplicación)**

---

## ⏱️ Tiempo e inactividad

```json
"enable_timeout": true
```
**(Activar tiempo de inactividad)**

```json
"idle_timeout": 30
```
**(Minutos de inactividad)**

```json
"idle_timeout_always_reload": true
```
**(Recargar siempre al expirar)**

```json
"reload_on_screen_on": true
```
**(Recargar al encender pantalla)**

---

## 🔐 Seguridad y bloqueo

```json
"multitap_settings": true
```
**(Activar acceso por múltiples toques)**

```json
"multitap_count": 10
```
**(Número de toques necesarios)**

```json
"require_password": true
```
**(Requerir contraseña de ajustes)**

```json
"settings_password": "481516"
```
**(PIN de administrador)**

---

## 🧱 Samsung Knox / Sistema

```json
"disable_recents": true
```
**(Desactivar apps recientes – Knox)**

```json
"disable_svoice": true
```
**(Desactivar Bixby/S Voice)**

```json
"hide_status_bar": true
```
**(Ocultar barra de estado)**

```json
"hide_system_dialogs": true
```
**(Ocultar diálogos del sistema)**

```json
"aggressively_hide_system_dialogs": true
```
**(Ocultación agresiva de diálogos)**

---

## 📄 Página y contenido web

```json
"page_zooming": false
```
**(Permitir zoom)**

```json
"overview_mode": true
```
**(Modo vista general)**

```json
"use_wide_viewport": true
```
**(Usar viewport ancho)**

```json
"initial_zoom": 0
```
**(Zoom inicial)**

```json
"cache_mode": "LOAD_DEFAULT"
```
**(Modo de caché)**

---

## 🧹 Cookies, caché y formularios

```json
"timeout_cacheclear": false
```
**(Limpiar caché al timeout)**

```json
"timeout_cookieclear": false
```
**(Borrar cookies al timeout)**

```json
"timeout_storageclear": false
```
**(Borrar almacenamiento web)**

```json
"timeout_formsclear": false
```
**(Borrar formularios)**

```json
"cacheclear_page_load": true
```
**(Limpiar caché al cargar página)**

---

## ⚙️ Hardware y sistema

```json
"hardware_acceleration": true
```
**(Aceleración por hardware)**

```json
"javascript_interface": true
```
**(Permitir JavaScript)**

```json
"keep_screen_on": false
```
**(Mantener pantalla encendida)**

```json
"volume_controls_enabled": true
```
**(Permitir botones de volumen)**

```json
"prevent_screen_power_off": false
```
**(Impedir apagado de pantalla)**

---

## 📷 Cámara, NFC y sensores

```json
"default_camera": "Back"
```
**(Cámara por defecto)**

```json
"camera_icon": false
```
**(Mostrar icono cámara)**

```json
"force_camera_uploads": false
```
**(Forzar subidas desde cámara)**

```json
"nfc_enabled": false
```
**(Habilitar NFC)**

---

## 🔔 Notificaciones y permisos

```json
"prevent_notification_access": true
```
**(Bloquear acceso a notificaciones)**

```json
"prevent_alert_dialogs": false
```
**(Bloquear diálogos web)**

```json
"allow_popup_windows": false
```
**(Permitir ventanas emergentes)**

---

## 🧠 Otros ajustes

```json
"theme": "Green"
```
**(Tema de color)**

```json
"rotation": "Landscape"
```
**(Orientación de pantalla)**

```json
"lock_rotation": true
```
**(Bloquear rotación)**

```json
"above_screen_lock": true
```
**(Mostrar sobre bloqueo del sistema)**

```json
"default_launcher_check": false
```
**(Comprobar launcher por defecto)**

```json
"automatic_config_download_frequency": 15
```
**(Frecuencia de descarga de configuración automática – minutos)**

---

📌 Documento pensado para **README.md o documentación técnica interna**.

