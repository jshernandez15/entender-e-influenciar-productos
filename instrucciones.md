# Generar el HTML con Marp CLI

```bash
# Instalar (si no lo tienes)
npm install -g @marp-team/marp-cli

# Generar HTML con tu theme
marp input.md -o index.html --html
```

Las imágenes deben estar en rutas **relativas al `.md`**, así que ponlas en la misma carpeta o en `./img/`. Para el tema MeLi que ya tienes, el flag `--theme` te permite inyectar el CSS con las variables.

## Generar PDF con imágenes locales

```bash
marp --pdf --allow-local-files input.md -o presentation.pdf
```
