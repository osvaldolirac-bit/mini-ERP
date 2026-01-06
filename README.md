[README.md](https://github.com/user-attachments/files/24456206/README.md)
# MiniERP (Local) — Streamlit + SQLite (Chile)

Esta alternativa **NO usa Colab ni Gradio**. Corre en tu Mac/PC y guarda la base de datos en una carpeta local (persistente).
Puedes abrirlo en tu iPhone **desde la misma Wi‑Fi**.

## 1) Requisitos
- Python 3.10+ (recomendado 3.11)
- macOS / Windows / Linux

## 2) Instalación (Mac)
Abre Terminal dentro de esta carpeta y ejecuta:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## 3) Ejecutar
```bash
streamlit run app.py --server.address 0.0.0.0 --server.port 8501
```

- En tu computador: abre `http://localhost:8501`
- En tu iPhone (misma red Wi‑Fi): abre `http://IP_DE_TU_MAC:8501`
  - Para ver la IP en Mac: `ipconfig getifaddr en0` (Wi‑Fi) o `ifconfig`

## 4) Usuario inicial
- usuario: `admin`
- clave: `admin123`

## 5) Dónde se guarda la base de datos
Por defecto queda dentro de la carpeta `data/mini_erp.db` (persistente mientras no borres esta carpeta).

Si quieres guardarla en otra ubicación, puedes definir la variable:
```bash
export MINIERP_DATA_DIR="/ruta/donde/quieres/guardar"
```

## 6) Qué incluye (versión estable)
- Multi-empresa (crear y cambiar empresa)
- Usuarios (admin crea usuarios y asigna empresas)
- Familias / Productos (crear, editar, borrar)
- Proveedores (crear, editar, borrar)
- Compras (Factura proveedor) con **proveedor en el ingreso**, fecha, vencimiento, CC y líneas
- Movimientos de stock (IN/OUT/ADJ) con fecha + historial
- Gastos no-factura (con CC)
- Reporte mensual por Centro de Costo (compras + gastos)
- Exportación a Excel

> Nota: Esta versión apunta a ser **muy estable** para uso diario. Si luego quieres recuperar módulos “contables completos”
> (asientos, balance, IVA, etc.) los podemos agregar, pero primero te dejo una base que corre siempre.
