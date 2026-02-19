---

# 🚛 Optimización Configuración – Euro Truck Simulator 2

Este documento explica los cambios realizados en el archivo `config.cfg` para mejorar el rendimiento del juego manteniendo buena calidad visual.
Llevo varios días solucionando este problema en Euro Truck Simulator 2, abria el juego y siempre se rompia y se detenia el juego, he probado a desistalarlo, a borrar los mods, pero nada, la solucion principal está en el archivo connfig
---

# 🎯 Objetivo

Optimizar el rendimiento en resolución **3440x1440 (Ultrawide 2K)** reduciendo el impacto de los elementos más pesados del juego como:

* Espejos
* Sombras
* Resolución interna
* Texturas
* Anisotropía

---

# ⚙️ Cambios Realizados

## 🔹 1. Escala de resolución interna

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

✔ Permite renderizar el juego a resolución real
✔ Elimina efecto borroso

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

✔ Mejora la calidad visual de camiones, carretera y entorno

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

✔ Mejora nitidez de texturas a distancia
✔ Carreteras más definidas

---

## 🔹 4. Optimización de espejos (para ganar FPS)

Recomendado si necesitas más rendimiento:

```
uset r_mirror_group "2"
uset r_mirror_view_distance "50"
```

✔ Reduce carga de GPU
✔ Mejora estabilidad de FPS

---

## 🔹 5. Sombras (opcional si necesitas más rendimiento)

Si el juego va justo:

```
uset r_sun_shadow_texture_size "2048"
```

✔ Reduce consumo sin perder demasiada calidad

---

# 📝 Cómo aplicar los cambios

## Paso 1️⃣ – Localizar el archivo

El archivo `config.cfg` está en:

```
Documentos > Euro Truck Simulator 2
```

---

## Paso 2️⃣ – Abrir con Visual Studio Code

1. Clic derecho sobre `config.cfg`
2. Seleccionar **Abrir con**
3. Elegir **Visual Studio Code**

---

## Paso 3️⃣ – Reemplazar contenido

1. Pulsar `Ctrl + A` → Seleccionar todo
2. Pegar la nueva configuración
3. Pulsar `Ctrl + S` → Guardar

---

# ⚠️ Importante

* Asegúrate de que el juego esté cerrado antes de modificar el archivo.
* Si el juego sobrescribe los cambios, puedes marcar el archivo como:

  * Clic derecho → Propiedades → Solo lectura

---

# ✅ Resultado Esperado

* Imagen más nítida
* Mejor rendimiento
* Menos carga en espejos
* Texturas en alta calidad
* Configuración optimizada para ultrawide

---

Espero que te haya servido :)

