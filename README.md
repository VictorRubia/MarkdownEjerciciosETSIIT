# Generador de PDF mediante Eisvogel para Markdown

> Autor: Victor Rubia

Generar un documento PDF bien estructurado mediante la plantilla Eisvogel para documentos escritos en Markdown. Como requisito previo, es necesario tener Docker instalado en el sistema.

## Uso

```bash
docker run --rm \
       --volume "$(pwd):/data" \
       --user $(id -u):$(id -g) \
       pandoc/extra example.md -o example.pdf --template eisvogel --listings
```

Las imágenes deben ir en la carpeta `imgs` y en el código se deberá referenciar mediante `/data/imgs/nombre_imagen.png`.