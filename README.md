# Documentacion-api
Un api para automatizar mas tus transcrips de discord.js
Documentación de la API de Transcripción
Introducción
Esta API permite la subida de archivos y la gestión de transcripciones asociadas.

Requisitos Previos
Node.js y Express: Asegúrate de tener Node.js y Express instalados en tu entorno.
Librerías:
express
multer
path
fs
moment
Endpoints
POST /upload
Descripción: Sube un archivo de transcripción.
Parámetros:
file: Archivo a subir.
Ejemplo de Uso:

// Ejemplo de código para subir un archivo usando Axios
const formData = new FormData();
formData.append('file', file, `${interaction.user.id}.html`);
axios.post('https://nublar-transcript-api.squareweb.app/upload', formData, {
  headers: {
    'Content-Type': 'multipart/form-data'
  }
}).then(response => {
  // Manejo de la respuesta
}).catch(error => {
  // Manejo del error
});

GET /transcripts/:filename
Descripción: Obtiene el archivo de transcripción por nombre de archivo.
Parámetros:
filename: Nombre del archivo de transcripción.
Ejemplo de Uso:
// Ejemplo de URL para obtener un archivo de transcripción
// https://nublar-transcript-api.squareweb.app/transcripts/mi_transcripcion.html

Ejemplo de Código de Referencia

if (customId === "cerrar") {
  // ... (código omitido para brevedad)
  const formData = new FormData();
  formData.append('file', file, `${interaction.user.id}.html`);
  axios.post('https://nublar-transcript-api.squareweb.app/upload', formData, {
    headers: {
      'Content-Type': 'multipart/form-data'
    }
  }).then(response => {
    // Manejo de la respuesta
  }).catch(error => {
    // Manejo del error
  });
}
