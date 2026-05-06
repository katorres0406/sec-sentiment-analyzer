# LinguaQ — Traductor con Qwen2-0.5B

**Traducción de idiomas 100% en el navegador, sin servidor, sin API keys.**

Usa [onnx-community/Qwen2.5-0.5B-Instruct](https://huggingface.co/onnx-community/Qwen2.5-0.5B-Instruct) ejecutado localmente mediante [Transformers.js](https://huggingface.co/docs/transformers.js).

---

## Demo rápida

Abre `translator.html` directamente en tu navegador (Chrome/Edge recomendado).

> ⚠️ La **primera carga** descarga el modelo (~250–400 MB en versión q4). Las siguientes cargas usan caché del navegador y son instantáneas.

---

## Ejemplos que funcionan

| Entrada (Inglés) | Salida (Español) |
|---|---|
| I like soccer | Me gusta el fútbol |
| How are you? | ¿Cómo estás? |
| What time is it? | ¿Qué hora es? |

---

## Características

- ✅ Sin backend ni servidor
- ✅ Sin API keys de ningún tipo
- ✅ Modelo cuantizado q4 (menor tamaño, buena calidad)
- ✅ Caché automático en IndexedDB del navegador
- ✅ Soporte para 8 idiomas: Inglés, Español, Francés, Alemán, Portugués, Italiano, Japonés, Chino
- ✅ Intercambio rápido de idiomas
- ✅ Ejemplos predefinidos con 1 clic
- ✅ Modo oscuro

---

## Tecnologías

| Librería | Uso |
|---|---|
| [Transformers.js v3](https://github.com/huggingface/transformers.js) | Inferencia en WebAssembly/WebGPU |
| [Qwen2-0.5B-Instruct](https://huggingface.co/Qwen/Qwen2-0.5B-Instruct) | Modelo de lenguaje |
| HTML + CSS + JS puro | Interfaz (sin frameworks) |

---

## Uso

```bash
# Clona el repo
git clone https://github.com/TU_USUARIO/linguaq-translator.git
cd linguaq-translator

# Abre en navegador (no necesita servidor)
open translator.html
# o en Linux:
xdg-open translator.html
```

También puedes servirlo con cualquier servidor estático:

```bash
npx serve .
# o
python3 -m http.server 8080
```

---

## Requisitos

- Navegador moderno con soporte ES Modules (Chrome 90+, Edge 90+, Firefox 90+, Safari 15+)
- Conexión a Internet solo para la primera descarga del modelo
- ~500 MB de espacio en caché del navegador

---

## Notas

- El modelo q4 (cuantizado 4 bits) reduce el tamaño y acelera la inferencia en CPU
- Para mejores resultados en traducción, las frases cortas-medianas funcionan mejor
- El modelo es un LLM de propósito general; para producción se recomendaría un modelo especializado en traducción (ej. Helsinki-NLP/opus-mt-*)

---

## Licencia

MIT
