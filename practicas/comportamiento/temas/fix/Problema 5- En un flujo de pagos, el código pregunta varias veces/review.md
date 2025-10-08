# 🧑‍💻 Revisión de Código - Patrones de Diseño (GoF)

👤 **Revisor:** Evelyn Sánchez  
📌 **PR Revisado:** Refactor Problema #5 — Strategy (GoF)  
👩‍💻 **Autor:** Jocelin Maribel Bernal Enciso  
📚 **Materia:** Patrones de Diseño  

---

## ✅ Checklist Técnica

| Ítem | ¿Cumple? | 💬 Comentarios |
|------|-----------|----------------|
| 1. Identifica al menos un code smell estructural real | ☑️ Sí | Se identificó correctamente el uso excesivo de condicionales (if/switch) y la violación del Principio Abierto/Cerrado. |
| 2. Aplica un patrón estructural adecuado | ☑️ Sí | Se aplicó el patrón **Strategy**, el cual es totalmente apropiado para eliminar condicionales y permitir extensibilidad. |
| 3. La solución es coherente y mejora el diseño | ☑️ Sí | El diseño ahora es modular, cumple con OCP y tiene menor acoplamiento. La extensión con nuevas estrategias es sencilla. |
| 4. El código es legible y está bien estructurado | ☑️ Sí | Las clases tienen responsabilidades claras, los nombres son coherentes y el flujo es fácil de seguir. |
| 5. El PR está bien documentado y argumentado | ☑️ Sí | El archivo presenta justificación, código refactorizado, resultados esperados y diagrama ASCII del patrón. |

---

## 🧠 Observaciones Técnicas

El patrón **Strategy** fue implementado de forma sólida y clara.  
Cada tipo de tarjeta (VISA, MASTERCARD, AMEX) tiene su propia estrategia, lo cual **elimina los condicionales** y mejora la extensibilidad del sistema.  
La separación entre `Payment`, `PaymentProcessor` y las clases concretas de pago respeta el **principio de responsabilidad única (SRP)** y el **principio abierto/cerrado (OCP)**.  

Además, el uso del diccionario para registrar estrategias es una decisión acertada que facilita la búsqueda dinámica sin romper el encapsulamiento.  
El código es **autoexplicativo**, mantiene buena legibilidad y las validaciones están bien manejadas.  

---

## 🛠️ Sugerencias de Mejora

- 🔸 **Evitar registro manual:** Podrías agregar una interfaz o método que registre automáticamente las estrategias disponibles para reducir la dependencia del método `Main()`.  
- 🔸 **Pruebas unitarias:** Implementa tests sencillos que verifiquen que cada estrategia devuelve el resultado esperado.  
- 🔸 **Clase base abstracta:** Centraliza la validación de montos (`Monto inválido`) en una clase base para evitar repetición.  
- 🔸 **Mensajes reutilizables:** Extrae el formato de mensajes de aprobación a una clase de utilidades para mantener la coherencia si se agregan más tarjetas.  

---

## 🎯 Conclusión del Revisor

> ✨ Excelente aplicación del patrón **Strategy**.  
> El refactor elimina correctamente los condicionales, mejora la claridad y cumple con los principios de diseño SOLID.  
> Se nota una comprensión profunda del patrón y su utilidad práctica.  
> Solo faltaría optimizar la repetición de lógica común y añadir pruebas automatizadas.  
>  
> 💡 ¡Muy buen trabajo y excelente claridad en la documentación! 👏

---

🔗 **Repositorio de referencia:**  
[https://github.com/tectijuana/pdd/tree/main/practicas/comportamiento/temas/fix/Problema%205-%20En%20un%20flujo%20de%20pagos](https://github.com/tectijuana/pdd/tree/main/practicas/comportamiento/temas/fix/Problema%205-%20En%20un%20flujo%20de%20pagos)
