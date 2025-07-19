# PadelMate Frontend Deployment op Render.com

## Stap-voor-stap Deployment

### 1. Render.com Account
- Ga naar [render.com](https://render.com)
- Maak een account aan of log in

### 2. Nieuwe Static Site
- Klik "New +"
- Kies "Static Site"
- Verbind met je GitHub account
- Selecteer de `padelmate-frontend` repository

### 3. Configuratie
- **Name**: `padelmate-frontend`
- **Build Command**: `npm install && npm run build`
- **Publish Directory**: `dist`
- **Environment Variables**:
  - `VITE_API_BASE_URL`: `https://padelmate-backend.onrender.com`

### 4. Deploy
- Klik "Create Static Site"
- Render zal automatisch de build uitvoeren
- Na succesvolle build krijg je een URL zoals: `https://padelmate-frontend.onrender.com`

### 5. Custom Domain (Optioneel)
- Ga naar Settings → Custom Domains
- Voeg je eigen domein toe

## Troubleshooting

### Build Errors
- Controleer of alle dependencies correct zijn geïnstalleerd
- Zorg dat `package.json` correct is geconfigureerd

### API Connection Issues
- Controleer of `VITE_API_BASE_URL` correct is ingesteld
- Test de backend URL: `https://padelmate-backend.onrender.com`

### Routing Issues
- Zorg dat `_redirects` bestand aanwezig is in `public/` directory
- Controleer of alle routes correct werken

## Environment Variables

| Variable | Value | Description |
|----------|-------|-------------|
| VITE_API_BASE_URL | https://padelmate-backend.onrender.com | Backend API URL |

## Build Process

1. `npm install` - Installeert dependencies
2. `npm run build` - Bouwt de productie versie
3. Render serveert de `dist/` directory

## Monitoring

- Ga naar je Render dashboard
- Bekijk logs voor eventuele errors
- Monitor performance en uptime 