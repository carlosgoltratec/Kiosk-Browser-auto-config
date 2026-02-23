# 📱 Modo Kiosko Android – Samsung Knox

> Documentación oficial de configuración de **Kiosk Browser Lockdown (ProCo IT)** para tablets Android usadas como **PIN de Control de Jornada Laboral**.

Basado en el manual interno **MODO_KIOSKO (PDF)** y preparado para uso en **GitHub**.

---

## 📑 Índice

1. Requisitos
2. Descripción general
3. Estructura del repositorio
4. Configuración por apartados de la aplicación

   * General
   * Display
   * Toolbar
   * Page & Content
   * Advanced
   * Hardware
   * Admin / Seguridad
   * Knox (Samsung)
   * Auto-configuración
5. Campos que se modifican habitualmente
6. Recomendaciones finales

---

## 1️⃣ Requisitos

* Tablet **Samsung** compatible con **Knox**
* Android configurado sin PIN ni contraseña
* App **Kiosk Browser Lockdown** (ProCo IT)
* Conexión WiFi

---

## 2️⃣ Descripción general

El modo kiosko permite **bloquear completamente la tablet** para que solo muestre una web de fichaje:

* Sin acceso a otras apps
* Sin notificaciones
* Sin barra de sistema
* Sin posibilidad de salir sin PIN

---

## 3️⃣ Estructura del repositorio (GitHub)

```
/kiosk-config
 ├── README.md
 ├── empresa1.json
 ├── empresa2.json
 └── default.json
```

Cada archivo JSON corresponde a **un cliente o empresa**.

---

## 4️⃣ Configuración por apartados de la aplicación

### 🔹 GENERAL

```json
"kiosk_url": "https://trabajador.controldejornadalaboral.es",
"custom_app_title": "Control de Jornada Laboral",
"enable_timeout": true,
"idle_timeout": 30,
"idle_timeout_always_reload": true,
"reload_on_screen_on": true
```

* **kiosk_url** (URL del kiosko) ⭐
* **custom_app_title** (título de la app) ⭐
* **enable_timeout** (activar inactividad)
* **idle_timeout** (minutos sin uso) ⭐
* **idle_timeout_always_reload** (recargar al expirar)
* **reload_on_screen_on** (recargar al encender pantalla)

---

### 🔹 DISPLAY

```json
"fullscreen_mode": true,
"lock_rotation": true,
"rotation": "LANDSCAPE",
"theme": "Green"
```

* **fullscreen_mode** (pantalla completa)
* **lock_rotation** (bloquear rotación)
* **rotation** (orientación fija)
* **theme** (color visual)

---

### 🔹 TOOLBAR

```json
"hide_action_bar": true,
"display_toolbar_swipe_down": false
```

* **hide_action_bar** (ocultar barra)
* **display_toolbar_swipe_down** (mostrar con gesto)

---

### 🔹 PAGE & CONTENT

```json
"page_zooming": false,
"overview_mode": true,
"use_wide_viewport": true,
"timeout_cacheclear": false,
"timeout_storageclear": false,
"timeout_cookieclear": false,
"timeout_formsclear": false
```

* **page_zooming** (permitir zoom)
* **overview_mode** (vista general)
* **use_wide_viewport** (viewport ancho)
* **timeout_*clear** (limpieza de datos)

📌 **Importante:** no borrar cookies ni storage.

---

### 🔹 ADVANCED

```json
"use_device_backbutton": false,
"hide_system_dialogs": true,
"aggressively_hide_system_dialogs": true,
"prevent_notification_access": true,
"allow_popup_windows": false
```

* **use_device_backbutton** (usar botón atrás)
* **hide_system_dialogs** (ocultar diálogos)
* **aggressively_hide_system_dialogs** (modo agresivo)
* **prevent_notification_access** (bloquear notificaciones)
* **allow_popup_windows** (permitir popups)

---

### 🔹 HARDWARE

```json
"keep_screen_on": false,
"hardware_acceleration": true,
"javascript_interface": true
```

* **keep_screen_on** (mantener pantalla encendida)
* **hardware_acceleration** (aceleración HW)
* **javascript_interface** (JS activo)

---

### 🔹 ADMIN / SEGURIDAD

```json
"require_password": true,
"multitap_settings": true,
"settings_password": "481516"
```

* **require_password** (pedir PIN)
* **multitap_settings** (activar taps múltiples)
* **settings_password** (PIN administrador) ⭐

---

### 🔹 SAMSUNG KNOX (solo Samsung)

```json
"disable_recents": true,
"disable_svoice": true,
"hide_status_bar": true
```

* **disable_recents** (bloquear apps recientes)
* **disable_svoice** (bloquear Bixby/S Voice)
* **hide_status_bar** (ocultar barra superior)

---

### 🔹 AUTO-CONFIGURACIÓN

```json
"automatic_config_url": "https://raw.githubusercontent.com/USUARIO/REPO/main/empresa1.json"
```

* **automatic_config_url** (URL de configuración remota) ⭐

Permite actualizar la configuración **sin tocar la tablet**.

---

## 5️⃣ Campos que se modifican habitualmente ⭐

* `kiosk_url`
* `custom_app_title`
* `idle_timeout`
* `settings_password`
* `automatic_config_url`

---
