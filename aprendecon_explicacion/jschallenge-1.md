# Day 1/100: JavaScript Challenge

## 🔍 Challenge: What’s the result of this simple addition?

console.log(0.1 + 0.2);

Options:

🔹 0.3
🔹 0.30000000000000004
🔹 0.2999999999999999
<br>
<br>
Resultado abajo ⤵️
<br>
<br>
El resultado de console.log(0.1 + 0.2); en JavaScript es **0.30000000000000004.**

### ¿Por qué ocurre esto?

Esto se debe a la forma en que los números de coma flotante se representan en binario. No todos los números decimales pueden representarse con precisión en binario, lo que provoca errores de redondeo. Este es un problema común en muchos lenguajes de programación.

### ¿Cómo solucionarlo?

Aunque no siempre es posible eliminar por completo estas imprecisiones, he aquí algunas técnicas para mitigarlas:

1. **Redondeo:**
Utiliza el método toFixed() para redondear el resultado a un número específico de decimales:
**JavaScript**

        console.log((0.1 + 0.2).toFixed(2)); 

2. **Number.EPSILON:** 
Utiliza Number.EPSILON para comparar números con una cierta tolerancia: 
**JavaScript** 

        const result = 0.1 + 0.2; 
            if (Math.abs(result - 0.3) < Number.EPSILON) { 
            console.log("El resultado es aproximadamente 0.3"); 
        }

3. **Bibliotecas:** 
Considere el uso de bibliotecas como bignumber.js o decimal.js para cálculos más precisos, especialmente cuando se trata de cálculos financieros u otros escenarios donde la precisión es crítica. 

_Al comprender las limitaciones de la aritmética de punto flotante y aplicar estas técnicas, puede minimizar el impacto de los errores de redondeo en sus aplicaciones JavaScript._
<br>
<br>

##### Fuente: 
###### Day 1/100: JavaScript Challenge, Rohtash Sethi. LinkedIn: https://www.linkedin.com/posts/rohtashsethi_100daysofjavascript-javascriptchallenge-webdevelopment-activity-7254885170149761025-R4La?utm_source=share&utm_medium=member_desktop
###### Floating-Point Arithmetic in JavaScript: https://g.co/gemini/share/1c3bb96d6c45