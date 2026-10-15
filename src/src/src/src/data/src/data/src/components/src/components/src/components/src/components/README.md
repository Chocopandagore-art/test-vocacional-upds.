# Test de Orientación Vocacional CHASIDE – UPDS Sucre

App web 100% client-side (React 18 + Vite + TailwindCSS + Recharts). Sin backend, sin login, sin cookies.

## Instalación

```bash
npm install
npm run dev        # http://localhost:5173 (también accesible desde tu red local)
```

Coloca el logo institucional en `public/logo-upds.png` antes de compilar.

## Build local

```bash
npm run build
npm run preview
```

## Deploy en Vercel

Opción A (GitHub):
1. Sube el proyecto a un repositorio.
2. En vercel.com → Add New → Project → importa el repo.
3. Vercel detecta Vite automáticamente (Build: `npm run build`, Output: `dist`). Deploy.

Opción B (CLI):
```bash
npm i -g vercel
vercel --prod
```

## Generar el QR para la feria

1. Copia la URL final (idealmente un dominio propio o uno corto de Vercel).
2. Genera el QR con cualquier generador (por ejemplo qr-code-generator.com o goqr.me) o por terminal:
```bash
   npx qrcode -o qr-feria.png -w 800 "https://tu-app.vercel.app"
```
3. Descarga en alta resolución (PNG 800 px o SVG), con corrección de errores nivel alta.
4. Imprime con fondo blanco y alto contraste, mínimo 8×8 cm, y pruébalo con 2 o 3 celulares distintos antes del evento.

## Configuración

- Pesos de afinidad (60/40): constantes `PESO_INTERES` y `PESO_APTITUD` al inicio de `src/data/carreras.js`.
- Plantilla oficial de corrección y textos: `src/data/preguntas.js` (valida al cargar que los 98 ítems aparezcan una sola vez).

Instrumento orientativo. CHASIDE ® – De León & Rodríguez.
