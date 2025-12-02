# 🛠️ GameAssetForge

**Automated Python Pipeline for Game Development Assets**

Un script de automatización diseñado para optimizar el flujo de trabajo de artistas y desarrolladores en Unity/Unreal Engine. Elimina el trabajo manual de preparar cientos de texturas, asegurando consistencia y optimización de memoria.

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat&logo=python&logoColor=white)
![Automation](https://img.shields.io/badge/Automation-CLI-orange?style=flat)

## 🚀 Características Principales

Este pipeline ejecuta 3 procesos críticos en lote:

1.  **Normalización de Formatos:** Detecta y convierte automáticamente imágenes (JPG, BMP, TIFF) al estándar `.png` para mantener la transparencia y calidad.
2.  **Smart Resizing (POT):** Redimensiona texturas grandes a la "Potencia de 2" más cercana (ej. 1024x1024, 512x512) para optimizar el uso de VRAM en tarjetas gráficas.
3.  **Estandarización de Nombres:** Aplica prefijos y sufijos configurables para mantener el orden en la carpeta `Assets` (ej. `tex_suelo_01.png`).

## 💻 Uso

Ejecuta el script apuntando a tu carpeta de recursos "crudos":

```bash
python asset_forge.py --input "./raw_assets" --output "./unity_assets" --resize 1024 --prefix "tex_"
