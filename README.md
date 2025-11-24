# ☀️ SolarCalc Pro - Herramienta de Ingeniería Fotovoltaica

Una aplicación web avanzada para la generación de cartas solares estereográficas y el cálculo de inclinación óptima de paneles fotovoltaicos. Diseñada con fines educativos y profesionales, permite alternar entre modelos académicos simplificados y algoritmos de ingeniería.

🔗 **[Ver Demo en Vivo](https://rafasalaesteve.github.io/calculadora-solar/)**

## 🚀 Características Principales

### 1. Doble Algoritmo de Cálculo
* 🎓 **Modo Escolar:** Aplica estrictamente las fórmulas simplificadas para prácticas académicas (`Latitud + 10°`, `Latitud - 20°`).
* 👷 **Modo Profesional (Ingeniería):** Utiliza el **Método de Lewis** y factores de corrección de irradiación difusa (`Latitud + 15°`, `Latitud * 0.87`) para escenarios de instalación real.

### 2. Carta Solar Estereográfica en Canvas
* Generación gráfica en tiempo real usando **HTML5 Canvas API**.
* Visualización precisa de trayectorias solares en Solsticios (Verano/Invierno) y Equinoccios.
* Sin imágenes estáticas: el gráfico se dibuja matemáticamente píxel a píxel según la latitud exacta.

### 3. Datos en Tiempo Real
* Cálculo de la posición solar instantánea (Elevación y Azimut) basándose en la hora y fecha del sistema del usuario.

### 4. Informe Técnico
* Generación automática de tablas con elevaciones máximas y ángulos de incidencia perpendicular puros.
* Exportación de gráficos a formato PNG.

## 🛠️ Stack Tecnológico

* **Core:** HTML5, CSS3, JavaScript (ES6+).
* **Estilos:** [Tailwind CSS](https://tailwindcss.com/) (vía CDN) para un diseño responsive y moderno.
* **Iconografía:** FontAwesome.
* **Despliegue:** Página estática (Single Page Application), ideal para **GitHub Pages**. No requiere Backend.

## 📦 Instalación y Uso

Este proyecto no requiere compilación ni instalación de dependencias (Node.js, NPM, etc.). Funciona directamente en el navegador.

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/solarcalc-pro.git](https://github.com/tu-usuario/solarcalc-pro.git)
    ```
2.  **Ejecutar:**
    Simplemente abre el archivo `index.html` en cualquier navegador web moderno (Chrome, Firefox, Edge).

## 🧮 Fórmulas Utilizadas

### Declinación Solar ($\delta$)
Se utiliza el algoritmo de Cooper (1969):
$$\delta = 23.45 \cdot \sin\left(360 \cdot \frac{284 + n}{365}\right)$$
*Donde $n$ es el día del año (1-365).*

### Posición Solar
Se resuelven las ecuaciones trigonométricas esféricas básicas para elevación ($\alpha$) y azimut ($\psi$):
$$\sin(\alpha) = \sin(\delta)\sin(\phi) + \cos(\delta)\cos(\phi)\cos(\omega)$$
*Donde $\phi$ es la latitud y $\omega$ el ángulo horario.*

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la [Licencia MIT](LICENSE).

---
