# Cómo incluir imágenes en Marp

## Sintaxis básica
```markdown
![alt text](./imagen.png)
```

## Con directivas de tamaño/posición (exclusivas de Marp)

```markdown
<!-- Ancho fijo -->
![w:400px](./foto.png)

<!-- Alto fijo -->
![h:300px](./foto.png)

<!-- Ambos -->
![w:600px h:400px](./foto.png)
```

## Imagen de fondo (ocupa todo el slide)
```markdown
![bg](./fondo.jpg)

<!-- Con oscurecimiento -->
![bg brightness:0.4](./fondo.jpg)

<!-- A la derecha, split 50/50 -->
![bg right](./imagen.png)

<!-- Split con porcentaje -->
![bg right:40%](./imagen.png)
```

## Ejemplo en `input.md`

```markdown
# Ejemplo

![bg right:35% brightness:0.9](./vendedor.jpg)

Usuario dice:  
"Quiero vender más"

Pero realmente:
- No confía en fulfillment  
- No entiende incentivos  
```

## Filtros CSS disponibles
```markdown
![blur:5px](./img.png)
![opacity:0.5](./img.png)
![grayscale:1](./img.png)
![sepia:1](./img.png)
```

## Generar el HTML con Marp CLI

```bash
# Instalar (si no lo tienes)
npm install -g @marp-team/marp-cli

# Generar HTML con tu theme
marp input.md -o presentation.html --html
```

Las imágenes deben estar en rutas **relativas al `.md`**, así que ponlas en la misma carpeta o en `./assets/`. Para el tema MeLi que ya tienes, el flag `--theme` te permite inyectar el CSS con las variables.
