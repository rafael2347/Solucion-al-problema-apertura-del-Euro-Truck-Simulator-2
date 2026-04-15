---

# 🚛 Optimización de Configuración – Euro Truck Simulator 2

Este documento explica los cambios realizados en el archivo `config.cfg` para mejorar el rendimiento y la estabilidad del juego.

Después de varios intentos (reinstalar, quitar mods, etc.), el problema principal se encontraba en la configuración interna del juego, especialmente en ciertos parámetros gráficos y de iluminación.

---

# 🎯 Objetivo

Optimizar el juego en resolución **3440x1440 (Ultrawide 2K)** consiguiendo:

* Mejor rendimiento (FPS estables)
* Imagen más nítida
* Eliminación de conflictos externos (RGB / iluminación)
* Mayor estabilidad general

---

# ⚙️ Cambios Clave

## 🔹 1. Resolución interna (Escalado)

Antes:

```
uset r_scale_x "0.5"
uset r_scale_y "0.625"
```

Ahora:

```
uset r_scale_x "1.0"
uset r_scale_y "1.0"
```

✔ Elimina el efecto borroso
✔ Renderizado a resolución real

---

## 🔹 2. Calidad de texturas

Antes:

```
uset r_texture_detail "0"
```

Ahora:

```
uset r_texture_detail "2"
```

✔ Mejora notable en camiones, carreteras y entorno

---

## 🔹 3. Filtro anisotrópico

Antes:

```
uset r_anisotropy_factor "0.2"
```

Ahora:

```
uset r_anisotropy_factor "1"
```

✔ Texturas más nítidas a distancia
✔ Mejora visual en carretera

---

## 🔹 4. Optimización de espejos

```
uset r_mirror_group "2"
uset r_mirror_view_distance "50"
```

✔ Reduce carga de GPU
✔ Mejora FPS en cabina

---

## 🔹 5. Sombras (ajuste equilibrado)

```
uset r_sun_shadow_texture_size "2048"
```

✔ Buen equilibrio entre calidad y rendimiento

---

## 🔹 6. ⚠️ Iluminación / RGB (MUY IMPORTANTE)

Se han ajustado/desactivado parámetros relacionados con iluminación dinámica debido a conflictos con **Armoury Crate**.

💥 Problema detectado:

* El juego se cerraba o se volvía inestable
* Conflicto entre el sistema de luces del juego y el software RGB del sistema

✅ Solución aplicada:

* Reducir o desactivar efectos de iluminación en el config
* Evitar que el juego gestione efectos de luces que interfieran con Armoury Crate

✔ Resultado:

* Juego estable
* Sin crasheos al iniciar
* Sin conflictos con el RGB del sistema

---

# 📝 Cómo aplicar los cambios

## Paso 1️⃣ – Ubicar el archivo

```
Documentos > Euro Truck Simulator 2
```

---

## Paso 2️⃣ – Editarlo

1. Clic derecho en `config.cfg`
2. Abrir con Visual Studio Code (o Bloc de notas)

---

## Paso 3️⃣ – Aplicar configuración

1. `Ctrl + A` → seleccionar todo
2. Pegar la nueva configuración
3. `Ctrl + S` → guardar

---

# ⚠️ Importante

* El juego debe estar **cerrado**
* Si se sobreescribe el archivo:

  * Clic derecho → Propiedades → **Solo lectura**

---

# ✅ Resultado esperado

* Imagen más nítida
* Mejor rendimiento
* FPS más estables
* Menor carga en GPU
* Sin conflictos con RGB / Armoury Crate

---

Si quieres, puedo hacerte una versión aún más pro (tipo GitHub con badges, capturas y comparación antes/después).
