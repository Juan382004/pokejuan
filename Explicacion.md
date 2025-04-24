# 🚀 ¡Despliega tu Pokedex en Azure con Estilo! 🌟

**🔗 Link de la web en la nube:**  
[https://delightful-field-02ef8bb10.6.azurestaticapps.net/](https://delightful-field-02ef8bb10.6.azurestaticapps.net/)
**📂 Repositorio:** [Juan Cardenas en GitHub](https://github.com/Juan382004/juanpoke)  

---

## ¡Prepárate para llevar tu Pokedex a la nube de una manera súper sencilla y visual! ☁️

### 1. 🍴 ¡A Bifurcar el Código! (Forking Time!) 🛠️

- Ve al código original:  
  [Repositorio base de Pokedex](https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab)
- Haz clic en **Fork** y crea tu propia copia (ej: `albertacho`).

### 2. 🗺️ ¡Navegando a la Ubicación Correcta! (App Location Adventure!) 🧭

- Ve a: `albertacho/.github/workflows/`
- Encuentra el archivo `.yml` (como `azure-static-web-apps-delightful-field-02ef8bb10.yml`)
- Edita el campo:

```yml
app_location: "./sistemas-distribuidos/poke-dex-lab/source/pokedex-angular"
```
- Guarda los cambios con Commit changes ✅

### 3. 🚦 ¡Luces, Cámara, Actions! (Checking the Magic!) ✨

- Haz clic en la pestaña **Actions** del repositorio.  
- Verifica que el flujo de trabajo se complete correctamente ⏳

---

### 4. 🚀 ¡Despegue a la Nube de Azure! (Azure Deployment!) ☁️

- Ve a tu recurso en **App Services**.  
- Haz clic en **Ir al recurso**.  
- Visita el **enlace web** de tu app 🌐 ¡y listo! 👀

### 5. 🛡️ ¡Añadiendo Escudos de Seguridad y Rutas Inteligentes! (Security & Navigation!) 🧭

- Crea un archivo llamado `staticwebapp.config.json` en:  
  `sistemas-distribuidos/poke-dex-lab/source/pokedex-angular/`

```json
{
  "globalHeaders": {
    "Content-Security-Policy": "default-src 'self'; img-src 'self' https://raw.githubusercontent.com https://pokeapi.co https://assets.pokemon.com; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; font-src 'self' https://fonts.gstatic.com; connect-src 'self' https://beta.pokeapi.co",
    "X-Frame-Options": "DENY",
    "Permissions-Policy": "geolocation=(), microphone=(), camera=()"
  },
  "navigationFallback": {
    "rewrite": "/index.html",
    "exclude": ["/images/", "/css/", "/js/*", "/favicon.ico"]
  }
}
```
- Guarda los cambios y espera a que se complete el workflow de GitHub Actions ✨

### 6. 🖼️ ¡Dando Vida a los Pokémon con Imágenes! (Loading Pokemon Images!) 🎨

- Edita el archivo:  
  `pokedex-angular/src/environments/environment.prod.ts`

Reemplaza o ajusta la ruta de las imágenes dentro del archivo, de modo que quede así:

```ts
export const environment = {
  production: true,
  imagesPath: '/assets/images',
  // otras variables de entorno si las hay
};
```
- Guarda los cambios y confirma que el deployment se realice correctamente ✅
