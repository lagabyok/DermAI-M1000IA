<h1 align="center">PROYECTO DermAI</h1>

- [Las imagenes que se usan de prueba](https://github.com/mariaelisaaraya/M1000IA/tree/2e90d79719e22be8ebb1adfe6bec1046ff995cfe/test/test_images)
- [Archivo que se utiliza con pytest para hacer las pruebas](https://github.com/mariaelisaaraya/M1000IA/blob/2e90d79719e22be8ebb1adfe6bec1046ff995cfe/testModel/test_predictModel.py)
- [Modelos Completo en versión Tensor Flow h5](https://github.com/mariaelisaaraya/M1000IA/blob/master/modelo%20ajustado%2099%25/modelo_final.h5) 
- [Modelos Completo en versión Tensor Flow keras](https://github.com/mariaelisaaraya/M1000IA/blob/master/modelo%20ajustado%2099%25/dermai_model.keras)

Sección: Imágenes y Consideraciones Éticas
Uso de Imágenes en el Proyecto DermAI

Este proyecto utiliza imágenes dermatológicas con fines exclusivamente educativos, de investigación y prueba del modelo.

Las imágenes de prueba utilizadas para el entrenamiento y validación del modelo provienen de repositorios públicos, accesibles para investigación académica y desarrollo tecnológico.

Aun cuando estas imágenes son de acceso público, muchas de ellas pueden considerarse sensibles, ya que corresponden a afecciones médicas de la piel.

Consideraciones Éticas

Por razones éticas y de buenas prácticas:

Se debe tener especial cuidado en el uso, redistribución y visualización de las imágenes.

Las imágenes no deben utilizarse con fines comerciales, ni presentarse como diagnósticos médicos reales.

El proyecto no reemplaza la evaluación de un profesional de la salud.

Se recomienda no asociar las imágenes a datos personales, identidades reales ni información clínica sensible.

Cualquier reutilización del material debe respetar las licencias originales del repositorio de origen.

Archivo de Imágenes Sensibles

El archivo/carpeta que contiene imágenes sensibles pertenece a un repositorio público, pero se incluye en este proyecto únicamente con fines de prueba y demostración técnica.

Por ética profesional, se solicita a los colaboradores:

No difundir las imágenes fuera del contexto del proyecto.

No modificar ni reutilizar las imágenes sin verificar previamente sus condiciones de uso.

Tratar el contenido con respeto y responsabilidad.

Nota Importante

DermAI es un proyecto experimental orientado al aprendizaje en visión por computadora y machine learning aplicado a dermatología.
Los resultados generados por el modelo no constituyen un diagnóstico médico.


# Guía para Levantar la Interfaz de la Aplicación 
- ### Carpeta Interfaz

## Requisitos Previos

1. Asegúrate de que el entorno virtual esté activado (debería verse como `(env)` en la terminal).
2. Debes estar dentro de la carpeta `interfaz`.

## Pasos para Ejecutar la Aplicación

1. Abre la terminal en la parte inferior (donde dice `bash - interfaz`).
2. Ejecuta el siguiente comando para correr la aplicación:

   ```bash
   python apiokc.py
   ```


## Errores Comunes

1. Error: El archivo modelo_entrenadomok.pth no se encuentra
Verifica que el archivo modelo_entrenadomok.pth esté en la misma carpeta que el script apiokc.py. Si está en otra carpeta, debes proporcionar la ruta completa o mover el archivo al directorio correcto.

2. Verifica el Funcionamiento del Servidor Flask
Tu aplicación Flask está funcionando correctamente en el servidor de desarrollo. Puedes acceder a ella abriendo un navegador web y visitando la dirección:

```bash
http://127.0.0.1:5000
```

Puedes probar la ruta básica:

```bash
@app.route('/')
def index():
    return "Bienvenido a la aplicación Flask"
```

3. Si encuentras errores relacionados con Flask o CORS, asegúrate de instalarlos dentro del entorno virtual:

```bash
pip install Flask
pip install flask-cors
```

## Error al Abrir el HTML

Si abres el archivo HTML usando file://, no funcionará correctamente. Usa un servidor local como http-server para servir tu frontend o ábrelo desde Flask si es posible. También puedes usar un servidor local como Live Server en Visual Studio Code (disponible como una extensión que puedes instalar).

## Flujo Completo de la Aplicación

1. El usuario carga una imagen en index.html.
2. app.js envía los datos al servidor Flask en la ruta /predict.
3. Flask procesa los datos, predice el resultado y devuelve una respuesta.
4. El usuario es redirigido a resultado.html con los resultados.
5. appb.js muestra los resultados en la página.
