# Agent Loop Básico de Inventario con IA

Proyecto compuesto por:

- API REST con FastAPI.
- Persistencia del inventario en `products.csv`.
- Agente con LLM y tool calling.
- Registro append-only en `conversation_log.csv`.

## Crear el entorno virtual

```bash
python -m venv myenv
```

Activar en Windows:

```bash
myenv\Scripts\activate
```

Activar en Codespaces, Linux o macOS:

```bash
source myenv/bin/activate
```

## Instalar dependencias

```bash
pip install -r requirements.txt
```

## Variables de entorno

Crear `.env`:

```env
GROQ_API_KEY=tu_clave_aqui
```

## Ejecutar la API

Terminal 1:

```bash
uvicorn api.app:app --reload
```

## Ejecutar el agente

Terminal 2:

```bash
python agent.py
```

## Detener

Presionar:

```text
Ctrl + C
```

Primero en el agente y después en la API.

```

---

# 36. Revisar que `.env` no se vaya a subir

Antes de hacer commit ejecutamos:

```bash
git status
```

No debería aparecer:

```text
.env
```

Si aparece, revisamos:

```text
.gitignore
```

y confirmamos que tenga:

```gitignore
.env
```

---