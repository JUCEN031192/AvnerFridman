# AvnerFridman
Este repositorio contiene un modelo matemático espaciotemporal basado en ecuaciones de reacción-difusión diseñado para simular la dinámica de la infección por el Virus de la Hepatitis B (VHB), la respuesta del sistema inmunológico y la subsecuente progresión hacia la fibrosis hepática.El código resuelve numéricamente un sistema acoplado de 39 Ecuaciones Diferenciales Parciales (EDPs) utilizando el método de diferencias finitas sobre una malla bidimensional que representa el microambiente del tejido hepático.

## ✨ Características Principales
* Modelo Espacial Bidimensional: Simula la difusión de viriones, citocinas y el movimiento quimiotáctico de células inmunes en una sección transversal de tejido.
* Dinámica Inmunológica Compleja: Modela las interacciones entre macrófagos (M1/M2), células T (Th1/Th2), y una amplia red de citocinas (IL-2, IL-6, IL-10, TNF-α, TGF-β, entre otras).
* Progresión Fenotípica: Rastrea la transición desde la inflamación aguda hasta la acumulación de matriz extracelular (ECM) y la formación de cicatrices (fibrosis).
* Calibración Fenomenológica: Incluye un módulo de visualización comparativa que replica curvas fenomenológicas de literatura médica para la validación del comportamiento dinámico.
  
## 🏗️ Arquitectura del Código
El código base está estructurado de manera modular para facilitar su lectura y modificación, ideal para fines de investigación académica:
* Configuración de Parámetros Biológicos: Diccionario completo de tasas de proliferación, muerte celular y constantes de saturación de Michaelis-Menten.
* Inicialización de Matrices y Dominios: Creación del dominio espacial ($10 \times 10$) y establecimiento de las condiciones iniciales de homeostasis e infección.
* Parámetros Numéricos y Estabilidad: Implementación del criterio de estabilidad de Courant-Friedrichs-Lewy (CFL) para determinar el paso de tiempo ($\tau$).
* Funciones de Interacción y Operadores: Métodos para calcular la difusión (Laplaciano) y quimiotaxis (Gradiente Central).
* Motor de Simulación Reacción-Difusión: Bucle principal de integración numérica que resuelve el sistema a lo largo de 180 días virtuales.
* Visualización y Análisis: Herramienta de graficación para interpretar la evolución temporal de las 30 variables clave del ecosistema hepático.

## ⚙️ Requisitos y DependenciasEl proyecto está escrito en Python 3 y utiliza librerías estándar de computación científica.
Bashpip install numpy matplotlib.

##🚀 Uso
Para ejecutar la simulación, simplemente clona el repositorio y corre el script principal. Dependiendo de las capacidades de tu equipo, la simulación de los 180 días puede tomar algunos minutos debido a la densidad del cálculo de las EDPs espaciales.
Bashgit clone https://github.com/JUCEN031192/AvnerFridman.git
cd AvnerFridman
python simulacion_vhb.py

Al finalizar el cálculo del motor, el script desplegará automáticamente una cuadrícula interactiva con 30 paneles mostrando la evolución poblacional y molecular a lo largo del tiempo.

📚 Contexto Académico
Este modelo forma parte del desarrollo metodológico de mi tesis de investigación [Opcional: "Título de tu tesis"]. Busca proporcionar un marco teórico y computacional para entender cómo la heterogeneidad espacial inicial del virus afecta la cronicidad de la enfermedad y el daño tisular a largo plazo.
