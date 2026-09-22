# Cauce Solutions — landing

Web estática de [caucesolutions.es](https://caucesolutions.es), desplegada como Cloudflare Worker con assets estáticos.

- `public/` — todo lo que se publica.
- `wrangler.jsonc` — configuración del Worker `caucesolutions`. Las rutas inexistentes (p. ej. `/portal/`) sirven `404.html`.

Cada push a `main` despliega automáticamente vía Workers Builds (`npx wrangler deploy`).

En local basta con abrir `public/index.html` o servir la carpeta:

```bash
python -m http.server 8080 --directory public
```
