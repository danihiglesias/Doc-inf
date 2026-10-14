# Guía del doctorando: requisitos y plazos 🎓

Libro electrónico bilingüe (español / inglés) con los requisitos y plazos que deben conocer los doctorandos del **Programa de Doctorado en Ingeniería Informática** de la Universidad de Salamanca durante el curso **2026-27**.

## Contenido

1. **El curso 2026-27**: calendario del curso; Studium, RAPI y cuadro resumen de entregas.
2. **Requisitos del programa**: actividades formativas, expediente y seguimiento anual, plazos de permanencia y fecha límite de depósito.
3. **La tesis**: qué se necesita para el depósito, tipos de tesis y casos particulares (compendio, mención internacional).
4. **Normativa**: normativa aplicable y contactos.

## Cómo compilar el libro en local

Requisitos: Python 3.12 (y Git). El resto lo instala el script.

```bash
python scripts/setup_env.py --yes      # crea .venv e instala dependencias
python scripts/build_book.py           # genera HTML en book/_build/html/
python scripts/launch_preview.py       # vista previa en http://localhost:8000
```

Para exportar el PDF:

```bash
python scripts/setup_env.py --yes --extras pdf
python scripts/setup_latex.py --yes
python scripts/export_pdf.py --engine auto
```

## Publicación

Cada `push` a `main` lanza el workflow `deploy-book` (GitHub Actions), que genera los PDF (español e inglés), compila el HTML y lo publica en GitHub Pages. En el repositorio debe estar configurado **Settings → Pages → Source: GitHub Actions**.

## Plantilla y licencia

Construido con la [plantilla TeachBook USAL](https://github.com/elloza/teachbook_usal_template) de Álvaro Lozano Murciego y André Filipe Sales Mendes (Jupyter Book / TeachBooks). Contenido bajo licencia [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
