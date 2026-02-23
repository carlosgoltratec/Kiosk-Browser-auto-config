# MODO KIOSKO

Modo para usar tablets como **PIN de fichaje**.
Básicamente bloquea la tablet para que **solo funcione una web**, sin poder usarla para otra cosa salvo que se desbloquee.

La aplicación debe abrir automáticamente:

```
https://trabajador.controldejornadalaboral.es
```

usando el **login PIN de la empresa** que vaya a fichar.

La aplicación Android utilizada es:
[https://www.android-kiosk.com/](https://www.android-kiosk.com/)

Este manual (Septiembre 2021) se basa en una **Samsung Galaxy Tab A 8"**.

---

## Configuración inicial de la tablet

1. Realizar el tutorial inicial de la tablet
2. Conectar a una red **WiFi**
3. Crear cuenta de **Google Play**

### Opciones importantes durante la configuración

* **No** poner PIN ni contraseña
* **Localización**: activar
* Desactivar todo lo demás

**Aplicaciones recomendadas**: desmarcar todo
**Samsung Account**: omitir

---

## Ajustes del sistema

### Pantalla

* Ajustes → Pantalla → Brillo automático → **Off**
* Ajustes → Pantalla → Tiempo de espera → **2 minutos**

### Sonido

* Sonidos y vibración → Modo de sonido → **Silencio**

### Bloqueo

* Pantalla de bloqueo → Tipo de bloqueo → **Ninguno**

### Accesibilidad

* Accesibilidad → Mejoras de visión → **Eliminar animaciones**

---

## Instalación del Kiosko

1. Abrir **Play Store**
2. Instalar **Kiosk Browser Lockdown** (ProCo IT)
3. Aceptar permisos de Google Play (es la primera app)

Mientras se instala:

* Quitar **todos los widgets y accesos**
* Dejar solo:

  * **Kiosk Lockdown**
  * **Ajustes**

---

## Configuración del launcher

1. Pulsar inicio
2. Elegir **Kiosk Browser**
3. Marcar **Siempre**
4. Saltar tutorial inicial

---

## Configuración de Kiosk Browser

Menú (⋮) → **Settings**
**Password:** `0000`

### General

* **Kiosk URL**

  ```
  https://trabajador.controldejornadalaboral.es
  ```
* **Kiosk Title**: Control de Jornada Laboral
* **Timeout (minutes)**: 30
* **Always Reload**: Activado

### Advanced

* Aggressively Hide System Dialogs → **On**
* Number of taps → **10** ⚠️

  > Importante: usar el máximo para evitar salidas accidentales

### Page & Content

* Clear WebStorage → Off
* Clear Cookies → Off
* Page Zooming → Off

### Display

* Full Screen Mode → **On**

### Toolbar

* Always Hide Toolbar → **On**
* Show Toolbar on Swipe Down → **Off**

### Permissions

* About → Permissions → **Accept** (todas)

### Hardware

* Keep Screen On → **Off**

### Admin

* Settings Password → **PIN del cliente**
  (por defecto: `481516`)

---

## Usuario PIN

* Crear un **usuario de tipo PIN**
* Introducir usuario y contraseña en la tablet

Ejemplo:

```
Usuario: pinprueba9
Password: pinprueba94815$
```

---

## Truco para desbloquear con 10 taps

Si se dejan **10 taps**, es difícil acertarlos exactos.

**Truco**:

* Pulsar entre el **tap 3 y 6**
* Un poco a la derecha
* Repetir varias veces

Así aparece la pantalla del PIN y se puede seguir pulsando sin que se cierre.

---

## Recargar el kiosko

1. Desbloquear el kiosko
2. Ir a **Settings**
3. Usar:

   * **Reload Kiosk Url**
   * (Debajo está **Clear Cache**)

---

## Configuración automática

> ⚠️ Pendiente de probar
> Ver archivo: `kiosk_settings_android.json`

---

## Problemas comunes

### No se puede sacar la ventana del PIN

* Usar el truco de los taps
* Recargar la página de inicio desde settings

---

## Enlaces útiles

* [https://trabajador.controldejornadalaboral.es/](https://trabajador.controldejornadalaboral.es/)
* [https://www.android-kiosk.com/](https://www.android-kiosk.com/)
* Tablet usada:
  [https://www.amazon.es/gp/product/B07Y2VJ3JF/](https://www.amazon.es/gp/product/B07Y2VJ3JF/)

---

