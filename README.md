# Proyecto de Limpieza de Datos Electorales y Creación de Base de Datos

Este proyecto está diseñado para automatizar la limpieza de datos electorales y la creación de una base de datos modular utilizando R. La estructura está basada en **Cookiecutter** para garantizar un entorno organizado y reproducible.

---

## **Estructura del Proyecto**

### **Raíz del Proyecto**

```
.
├── README.md              # Documento principal con la descripción del proyecto
├── cookiecutter.json      # Configuración de Cookiecutter
├── docs/                  # Documentación generada del proyecto
├── model/                 # Scripts de modelado
└── {{cookiecutter.project_slug}}/  # Carpeta con datos y notebooks del proyecto
```

### **Carpeta `docs/`**

```
docs/
├── 01_transformacion_datos.html  # Reporte de la primera etapa de transformación
├── 02_transformacion_datos.html  # Reporte de la segunda etapa de transformación
├── 03_transformacion_datos.html  # Reporte de la tercera etapa de transformación
├── index.html                   # Página principal del sitio generado
├── custom.css                   # Estilo personalizado para el sitio
├── site_libs/                   # Librerías necesarias para el sitio
└── search.json                  # Archivo para búsqueda en el sitio
```

### **Carpeta `model/`**

```
model/
├── DESCRIPTION            # Metadatos del proyecto en R
├── NAMESPACE              # Control de funciones exportadas e importadas
├── R/                     # Scripts de R
│   └── script.R           # Script principal con las funciones del modelo
└── model.Rproj            # Proyecto de RStudio para organizar el trabajo
```

### **Carpeta `{{cookiecutter.project_slug}}/`**

```
{{cookiecutter.project_slug}}/
├── data/                  # Datos de entrada y conjuntos de datos
├── notebooks/             # Notebooks de Quarto
└── README.md              # Documentación del proyecto
```

---

## **Requisitos Previos**

Para ejecutar este proyecto, necesitas tener instalados:

- R (versión 4.3.3 o superior).
- Paquetes necesarios en R: 
  ```R
  install.packages(c("tidyverse", "quarto", "data.table"))
  ```
- Quarto CLI para renderizar documentación.
- Cookiecutter para generar estructuras modulares.
  ```bash
  pip install cookiecutter
  ```

---

## **Uso del Proyecto**

### **1. Generación de la estructura**

Usa Cookiecutter para crear la estructura del proyecto:
```bash
cookiecutter gh:tu-repositorio/cookiecutter-template
```

### **2. Limpieza de datos**

1. Carga los datos crudos en la carpeta `data/`.
2. Ejecuta el script de transformación desde `R/script.R` para procesar los datos.
3. Los datos procesados se guardarán en la carpeta `data/`.

### **3. Modelado**

Ejecuta los scripts en la carpeta `model/` para construir los modelos basados en los datos procesados.

### **4. Documentación**

La documentación del proyecto está disponible en `docs/index.html`. Puedes generar o actualizar esta documentación con Quarto:
```bash
quarto render
```

---

## **Mantenimiento**

- **Actualizar dependencias**: Asegúrate de mantener las bibliotecas actualizadas.
  ```R
  update.packages()
  ```
- **Agregar nuevos datos**: Coloca los archivos en la carpeta `data/` y ajusta los scripts si es necesario.
- **Expandir análisis**: Utiliza notebooks en la carpeta `notebooks/` para experimentación adicional.

---

## Visualización del Proyecto:

[Visita el Sitio Web]()

---

## **Contribuciones**

Las contribuciones son bienvenidas. Por favor, crea un fork del repositorio y abre un pull request con tus mejoras o sugerencias.

---

## **Licencia**

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

## Contacto:

Para cualquier consulta, puedes escribirme: eduardobareapoot@outlook.com

