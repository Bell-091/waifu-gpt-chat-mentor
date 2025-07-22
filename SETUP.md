# 🔑 Configuración de API Key - Waifu GPT

## ⚠️ IMPORTANTE: Configurar la Clave API

Para que Waifu GPT funcione correctamente, necesitas obtener una clave API de OpenRouter. Sigue estos pasos:

## 📋 Pasos para Obtener la Clave API

### 1. Crear Cuenta en OpenRouter

1. Ve a [OpenRouter.ai](https://openrouter.ai/)
2. Haz clic en "Sign Up" (Registrarse)
3. Crea tu cuenta con email o GitHub
4. Verifica tu email si es necesario

### 2. Obtener Créditos Gratuitos

OpenRouter ofrece **$1 USD en créditos gratuitos** para nuevos usuarios, suficiente para muchas conversaciones de prueba.

### 3. Generar API Key

1. Una vez logueado, ve a tu dashboard
2. Busca la sección "Keys" o "API Keys"
3. Haz clic en "Create Key" o "Generate New Key"
4. Dale un nombre descriptivo (ej: "Waifu GPT")
5. Copia la clave generada (empieza con `sk-or-v1-...`)

### 4. Configurar en tu Proyecto

Abre el archivo `.env.local` en la raíz del proyecto y reemplaza:

```env
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

Por:

```env
OPENROUTER_API_KEY=sk-or-v1-tu-clave-real-aqui
```

### 5. Reiniciar el Servidor

```bash
# Detén el servidor (Ctrl+C)
# Luego reinicia:
npm run dev
```

## 💰 Costos Aproximados

Con OpenRouter y GPT-4o:
- **Costo por mensaje**: ~$0.001-0.005 USD
- **$1 USD**: ~200-1000 mensajes
- **Muy económico** para uso personal

## 🚀 Despliegue en Vercel

### Variables de Entorno en Vercel

1. Ve a tu proyecto en [Vercel Dashboard](https://vercel.com/dashboard)
2. Settings → Environment Variables
3. Añade:
   - **Name**: `OPENROUTER_API_KEY`
   - **Value**: Tu clave API real
   - **Environment**: Production, Preview, Development

### Deploy Automático

Una vez configurada la variable de entorno:

```bash
git add .
git commit -m "Add Waifu GPT chat interface"
git push origin main
```

Vercel desplegará automáticamente.

## 🔒 Seguridad

- ✅ La clave API se mantiene en el servidor (no se expone al cliente)
- ✅ Variables de entorno seguras
- ✅ Validación de entrada en la API
- ✅ Manejo de errores apropiado

## 🧪 Probar la Configuración

1. Reinicia el servidor: `npm run dev`
2. Ve a `http://localhost:8000`
3. Envía un mensaje como: "¿Qué es JavaScript?"
4. Yuki-chan debería responder con una explicación detallada

## ❓ Solución de Problemas

### Error: "falta la clave API"
- Verifica que el archivo `.env.local` existe
- Verifica que la clave empiece con `sk-or-v1-`
- Reinicia el servidor después de cambiar la clave

### Error: "Error al comunicarse con el servicio de IA"
- Verifica que la clave API sea válida
- Verifica que tengas créditos en OpenRouter
- Revisa la consola del servidor para más detalles

### La aplicación no responde
- Verifica que el servidor esté corriendo en puerto 8000
- Revisa la consola del navegador (F12) para errores

## 📞 Soporte

Si tienes problemas:
1. Revisa los logs del servidor en la terminal
2. Revisa la consola del navegador (F12)
3. Verifica que todos los archivos estén guardados
4. Reinicia el servidor de desarrollo

---

¡Una vez configurada la API key, tendrás tu propia Waifu GPT funcionando! 🌸✨
