# Metodos_Raices_Numericas
Este documento registra los prompts usados y las sugerencias aceptadas o rechazadas por GitHub Copilot durante el desarrollo de los métodos numéricos solicitados en el Laboratorio No. 4.

Método de Bisección
Prompt usado:
Escribe en Python una función para aplicar el método de bisección con una tolerancia de 1e-5, que incluya el conteo de iteraciones y valide el cambio de signo en el intervalo.
Sugerencia de Copilot:
Copilot generó la estructura correcta de la función, incluyendo la validación de f(a)*f(b)>0 y el cálculo del punto medio.
Decisión: Aceptada
Resultado: Implementación funcional con control de signo y conteo de iteraciones.

Método de Falsa Posición (Regula Falsi)
Prompt usado:
Implementa el método de falsa posición en Python y muéstrame cómo calcular la raíz de f(x) = x³ + x² - 1 con tolerancia 1e-6.
Sugerencia de Copilot:
Incluyó la fórmula de interpolación lineal para calcular c = b - f(b)*(a-b)/(f(a)-f(b)).
Decisión: Aceptada
Resultado: El método funcionó correctamente, pero mostró estancamiento en un extremo.

Método de Falsa Posición Modificada (Illinois)
Prompt usado:
Modifica el método de falsa posición para que no se estanque, usando el método de Illinois.
Sugerencia de Copilot:
Propuso dividir por dos el valor de f(a) o f(b) según el extremo que no cambiaba.
Decisión: Aceptada
Resultado: Mejoró notablemente la convergencia reduciendo el número de iteraciones.

Método del Punto Fijo
Prompt usado:
Escríbeme el método de punto fijo en Python que compare dos formas de g(x) y determine cuál converge.
Sugerencia de Copilot:
Propuso una función iterativa con control de tolerancia y error absoluto.
Decisión: Aceptada
Resultado: Se aplicó correctamente con g₁(x)=e⁻ˣ (no converge) y g₂(x)=-ln(x) (sí converge).

Método de Newton-Raphson
Prompt usado:
Crea una función para el método de Newton-Raphson que maneje errores cuando la derivada sea cero o muy grande.
Sugerencia de Copilot:
Incluyó condición de seguridad para evitar divisiones por derivadas cercanas a cero o infinitas.
Decisión: Aceptada
Resultado: Previno divergencia al aplicar f(x)=x^(1/3) cerca de x=0.

Método de la Secante
Prompt usado:
Implementa el método de la secante para f(x)=cos(x)-x y compara sus resultados con Newton-Raphson.
Sugerencia de Copilot:
Generó correctamente la fórmula x₂ = x₁ - f₁*(x₁-x₀)/(f₁-f₀).
Decisión: Aceptada
Resultado: Convergió hacia x≈0.7391, requiriendo más iteraciones que Newton-Raphson.

