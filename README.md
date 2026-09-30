# Pixelízate (prototipo)

Convierte una foto en un personaje de pixel art. Todo se procesa en el navegador: las fotos no se suben a ningún servidor.

## Qué incluye

- **Foto:** 6 tamaños de personaje (32 a 360 px), 9 paletas, colores automáticos y tonos intermedios.
- **Ajustes:** quitar fondo con IA en el navegador o fondo liso al instante, borrador y limpieza de manchas, encuadre (foto completa o recortada), 6 escenarios en pixel art, limpieza de píxeles sueltos, contorno de color, líneas pixel perfect, brillos, tramado, contraste, saturación y brillo.
- **Marco:** 9 marcos en pixel art con resolución y paleta propias, y placa con texto.
- **Diversión:** 8 accesorios arrastrables, animación (rebote, respirar, flotar), cuadro de diálogo RPG, carta coleccionable con rareza (moderna o RPG clásico) y efectos de pantalla.
- **Descargas:** PNG, GIF animado y video.

Las opciones marcadas "Desbloqueo" representan el pago único previsto para la versión completa.

## Cómo probarlo

Abrí `index.html` desde un servidor web (no directamente como archivo), por ejemplo:

```bash
python3 -m http.server 8000
# luego abrí http://localhost:8000
```

O publicalo con **GitHub Pages**: Settings → Pages → Branch `main`, carpeta `/ (root)`.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | Toda la app (HTML, estilos y código). |
| `ort-wasm-simd.wasm` | Motor de ONNX Runtime Web 1.16.3 para el recorte con IA. |
| `u2netp.onnx.b64.txt` | Modelo U²-Netp de recorte de sujetos, en base64. |

El motor de ONNX Runtime (`ort.min.js`) se carga desde jsDelivr solo cuando se usa "Quitar fondo".

## Créditos de terceros

- [ONNX Runtime Web](https://github.com/microsoft/onnxruntime) — licencia MIT.
- [U²-Net / U²-Netp](https://github.com/xuebinqin/U-2-Net) — licencia Apache 2.0 (modelo distribuido por [rembg](https://github.com/danielgatis/rembg)).
- [gifenc](https://github.com/mattdesl/gifenc) — licencia MIT, incluido dentro de `index.html`.
- Fuentes Silkscreen, Atkinson Hyperlegible y JetBrains Mono desde Google Fonts (licencia SIL Open Font).
