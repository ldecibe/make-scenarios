# 📌 Make Scenarios - Blueprints

Este repositorio contiene **Blueprints exportados desde Make.com**, que permiten versionar, compartir y reutilizar escenarios de automatización.

---

## 🚀 ¿Qué es un Blueprint en Make?
Un **Blueprint** es la exportación de un escenario de Make en formato **JSON**.  
- Contiene la estructura del flujo, módulos y configuraciones.  
- **No incluye credenciales ni conexiones** (por seguridad).  
- Puede importarse en cualquier cuenta de Make para replicar el escenario.  

---

## 📂 Estructura del repositorio

```
make-scenarios/
│
├── scenarios/        # Blueprints exportados (.json)
│   ├── escenario_v1.json
│   └── escenario_v2.json
│
├── docs/             # Documentación adicional (diagramas, notas, etc.)
│
└── README.md         # Este archivo
```

---

## 🔄 Flujo de trabajo recomendado

1. **Exportar un escenario desde Make**
   - Abrir escenario en Make → menú superior derecho **More (···)** → **Export Blueprint**.
   - Guardar el archivo `.json` dentro de `scenarios/`.

2. **Versionar en GitHub**
   ```bash
   git add scenarios/escenario_vX.json
   git commit -m "Añadir escenario versión X"
   git push
   ```

3. **Importar un escenario en Make**
   - Crear nuevo escenario en Make.  
   - Menú superior derecho **More (···)** → **Import Blueprint**.  
   - Seleccionar el `.json` exportado de este repo.  
   - Reasignar conexiones existentes (no es necesario crear nuevas si ya usas las mismas).

---

## 🌱 Buenas prácticas

- Mantener un escenario **estable** (`main`) y otro **experimental** (`dev`) en ramas distintas de GitHub.
- Usar nombres claros para los Blueprints (`escenario_propiedades_v1.json`, `escenario_notificaciones_v2.json`).
- Documentar en `docs/` los cambios importantes, flujos o dependencias externas.
- Reutilizar conexiones existentes en Make para evitar duplicados.

---

## 📖 Recursos útiles

- [Documentación oficial de Make - Blueprints](https://www.make.com/en/help/blueprints/blueprints)  
- [GitHub Docs - Usar Git para versionar archivos](https://docs.github.com/es/get-started)  

---

✍️ Autor: [ldecibe](https://github.com/ldecibe)  
