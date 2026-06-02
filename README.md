# Informes — Club de Programación ULSA

Repositorio central de informes y métricas del Club de Programación de la Universidad La Salle, Cancún.

## Estructura

```
informes/
├── docs/                  → GitHub Pages (HTML publicado)
│   ├── index.html          → Portal de informes
│   └── 2026/
│       ├── IC/
│       │   └── informe_cuatrimestral/
│       │       ├── index.html
│       │       ├── img/
│       │       └── informe_files/
│       ├── IIC/            → (futuro)
│       └── IIIC/           → (futuro)
│
├── 2026/                   → Fuentes del ciclo 2025–2026
│   ├── IC/
│   │   └── informe_cuatrimestral/
│   │       ├── data/       → Datos crudos (CSV)
│   │       ├── analysis/   → Notebooks de análisis (EDA)
│   │       ├── report/     → Fuente del informe (QMD, SCSS, img)
│   │       └── build/      → Artefactos generados (regenerable)
│   ├── IIC/
│   │   └── informe_cuatrimestral/  → (futuro)
│   └── IIIC/
│       └── informe_cuatrimestral/  → (futuro)
│
└── README.md
```

## Convenciones

| Directorio  | Propósito                                    |
|-------------|----------------------------------------------|
| `data/`     | Datos fuente (CSV, JSON, etc.)               |
| `analysis/` | Notebooks y scripts de análisis              |
| `report/`   | Fuente del informe (QMD, SCSS, img)          |
| `build/`    | Artefactos generados por el toolchain        |

### Organización por año y cuatrimestre

```
{año}/
├── {cuatrimestre}/
│   └── informe_cuatrimestral/
│       ├── data/
│       ├── analysis/
│       ├── report/
│       └── build/
```

- **Cuatrimestres:** `IC`, `IIC`, `IIIC`
- **Año:** el del cierre del ciclo (ej. `2026` para 2025–2026)

## Publicar

1. Compilar el informe desde `report/` (Quarto, etc.)
2. Copiar el HTML + assets a `docs/{año}/{cuatrimestre}/informe_cuatrimestral/`
3. Renombrar el HTML a `index.html`
4. Agregar enlace en `docs/index.html`
5. Pushear a `main` — GitHub Pages despliega automáticamente

## Licencia

Uso interno del Club de Programación ULSA.
