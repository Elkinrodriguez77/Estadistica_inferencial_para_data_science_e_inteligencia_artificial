# Para conectar con API de Kaggle seguir estos pasos:

1. Instalar biblioteca de kaggle

<p>
pip install kaggle
</p>

2. Configuración de la API:

Ve al sitio web de Kaggle.
Haz clic en tu perfil de usuario en la esquina superior derecha.
Ve a "Account" (Cuenta).
Busca la sección de "API" y haz clic en “Create New API Token” (Crear nueva token de API). Esto descargará un archivo llamado kaggle.json.
Coloca este archivo en la ruta: ~/.kaggle/kaggle.json en sistemas Unix/Linux o C:\Users\<Windows-username>\.kaggle\kaggle.json en Windows.
Cambia los permisos del archivo para mantenerlo seguro:

<p>
chmod 600 ~/.kaggle/kaggle.json
</p>

3. Ejecutar el código para descargar el dataset:

<p>
import kaggle

# Descargar el conjunto de datos
kaggle.api.authenticate()  # Autenticarte con la API de Kaggle
kaggle.api.dataset_download_files('alessandrolobello/the-ultimate-earthquake-dataset-from-1990-2023', path='.', unzip=True)

</p>