QA Automation | SauceDemo

Proyecto de automatización de pruebas funcionales End-to-End (E2E) sobre la aplicación web SauceDemo, desarrollado con Python, Selenium WebDriver y Pytest.

El objetivo es validar funcionalidades clave de una tienda online mediante pruebas automatizadas, utilizando aserciones para verificar los resultados esperados y reportes HTML para documentar las ejecuciones.

🎯 Objetivos del proyecto

Automatizar escenarios de prueba sobre funcionalidades principales de la aplicación.

Validar el inicio de sesión y el acceso al inventario.

Comprobar la visualización de productos y elementos de la interfaz.

Verificar el agregado de productos al carrito de compras.

Validar el contador del carrito y la navegación hacia sus contenidos.

Generar reportes HTML para facilitar el análisis de resultados.

🧪 Casos de prueba implementados

La suite actual contiene ocho casos de prueba:

ID

Caso de prueba

Validación

TC-01

Inicio de sesión

Verifica la redirección al inventario con credenciales válidas.

TC-02

Verificación del inventario

Comprueba el título de la página y el encabezado de productos.

TC-03

Productos visibles

Verifica que existan productos en el catálogo.

TC-04

Validación de la interfaz

Comprueba la visibilidad del menú y del selector de ordenamiento.

TC-05

Agregar producto al carrito

Verifica que el botón cambie a "Remove" después de agregar un producto.

TC-06

Contador del carrito

Comprueba que el contador muestre la cantidad esperada.

TC-07

Navegación al carrito

Verifica el acceso a la página del carrito.

TC-08

Producto en el carrito

Comprueba que el producto esperado sea "Sauce Labs Backpack".

Nota: los escenarios de carrito utilizan el estado preparado por las pruebas anteriores. Como mejora futura, se puede trabajar en la independencia de los casos de prueba para permitir su ejecución aislada.

🛠️ Tecnologías y herramientas

Python: lenguaje utilizado para desarrollar los scripts de automatización.

Selenium WebDriver: automatización de interacciones con el navegador.

Pytest: framework para organizar y ejecutar los casos de prueba.

pytest-html: generación de reportes de ejecución en formato HTML.

webdriver-manager: gestión de la instalación del controlador de Chrome.

Git y GitHub: control de versiones y publicación del proyecto.

📁 Estructura del proyecto

pre-entrega-automation-testing/
│
├── reports/
│   ├── assets/
│   │   └── style.css
│   └── reporte.html
│
├── tests/
│   └── test_saucedemo.py
│
├── utils/
│
├── .gitignore
├── conftest.py
├── pytest.ini
└── README.md

Archivos principales

tests/test_saucedemo.py: contiene los ocho casos de prueba automatizados.

conftest.py: define la fixture driver, que inicializa Chrome mediante Selenium y webdriver-manager, y cierra el navegador al finalizar.

pytest.ini: configura la generación automática del reporte HTML con las opciones de Pytest.

reports/: directorio destinado a almacenar los reportes de ejecución y los recursos complementarios.

utils/: directorio reservado para futuras funciones auxiliares reutilizables.

⚙️ Instalación y configuración

1. Clonar el repositorio

git clone <URL_DEL_REPOSITORIO>

2. Ingresar al directorio del proyecto

cd pre-entrega-automation-testing

3. Crear y activar un entorno virtual

Crear el entorno:

python -m venv .venv

En Windows PowerShell:

.\.venv\Scripts\Activate.ps1

En Linux o macOS:

source .venv/bin/activate

4. Instalar las dependencias

python -m pip install selenium pytest pytest-html webdriver-manager

Requisitos: Python compatible con las dependencias instaladas y Google Chrome disponible en el entorno de ejecución.

▶️ Ejecución de las pruebas

Desde la raíz del proyecto, ejecutar:

python -m pytest

La configuración de pytest.ini genera automáticamente el reporte HTML en reports/reporte.html.

Para ejecutar las pruebas con información detallada en la terminal:

python -m pytest -v

Si necesitás generar explícitamente el reporte HTML desde la línea de comandos:

python -m pytest -v --html=reports/reporte.html --self-contained-html

El archivo HTML permite consultar el resultado de la ejecución y revisar los casos aprobados o fallidos.

Importante: el directorio reports/ debe existir antes de generar el reporte. Si no existe, crealo previamente.

📊 Reportes de ejecución

El proyecto utiliza pytest-html para generar reportes que facilitan el seguimiento de las pruebas automatizadas.

Los resultados permiten identificar:

Passed: pruebas que finalizaron correctamente.

Failed: pruebas que no cumplieron las condiciones esperadas.

Error: problemas ocurridos durante la preparación o ejecución de una prueba.

El reporte se genera al ejecutar Pytest. Los resultados y las cantidades de pruebas deben verificarse en cada ejecución; no se presuponen resultados exitosos.

🚀 Mejoras futuras

Como posibles evoluciones del proyecto, se consideran:

Incorporar escenarios negativos de autenticación.

Agregar pruebas para eliminar productos del carrito.

Mejorar la independencia y reutilización de los casos de prueba mediante fixtures.

Centralizar la configuración y las funciones auxiliares.

Implementar el patrón Page Object Model (POM).

Crear un archivo requirements.txt para gestionar las dependencias.

Incorporar integración continua mediante GitHub Actions.

Agregar capturas de pantalla ante fallos para mejorar el diagnóstico.

👩‍💻 Sobre el proyecto

Este proyecto forma parte de mi formación en QA Automation y representa una práctica de automatización funcional con Selenium WebDriver y Pytest.

Su propósito es aplicar conocimientos de testing, validación mediante aserciones, organización de casos de prueba y generación de reportes de ejecución.

Repositorio: GitHub
