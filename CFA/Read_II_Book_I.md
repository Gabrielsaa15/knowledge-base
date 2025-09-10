# The Time Value of Money

## Module 2.1: Discounted Cash Flow Valuation

> Es lo mismo que ingeniería económica, solo necesitamos recordar:

### Fórmulas Clave

**Valor Futuro con capitalización continua:**
```
FV = PV * e^(r*t)
```
Donde:
- FV = Future Value (Valor Futuro)
- PV = Present Value (Valor Presente)
- r = tasa de interés
- t = tiempo

### Conceptos de Bonos

- **Face Value** = Valor nominal
- **Coupon Rate** = El cupón que se paga
- **Yield to Maturity** = La tasa o discount rate

**Regla importante:** Si la tasa es negativa y es un zero coupon bond, el bono se venderá con premium, lo cual significa que su precio es mayor que su valor nominal.

### Tipos de Bonos

#### Perpetual Bond
```
Precio = Payment / r
```

#### Amortizing Bond
Un amortizing bond es aquel que paga una cantidad fija cada período, incluyendo su período de vencimiento. La diferencia entre un amortizing bond y un fixed-coupon bond es que para un amortizing bond, cada pago incluye una porción del principal. Con un fixed-coupon bond, todo el principal se paga al inversionista en la fecha de vencimiento.

---

## Equity Securities

### Recordar:
- **Fixed income securities** = Renta fija
- **Equity securities** = Acciones

Como con los valores de renta fija, valoramos los equity securities (como acciones comunes y preferentes) como el valor presente de sus flujos de caja futuros. Las diferencias clave son que los equity securities no vencen, y sus flujos de caja pueden cambiar con el tiempo.

### Preferred Stock

**Stated Preferred Stock** paga un dividendo fijo que se establece como un porcentaje de su valor par (similar al face value de un bono). Como con los bonos, debemos distinguir entre el porcentaje establecido que determina los flujos de caja y la tasa de descuento que aplicamos a los flujos de caja.

Los inversionistas en equity tienen un **required return** que los inducirá a poseer una acción equity. Este required return es la tasa de descuento que usamos para valorar equity securities.

### Common Stock

**Common Stock** es un reclamo residual sobre los activos de una empresa después de satisfacer todos los demás reclamos. Las acciones comunes típicamente no prometen un pago de dividendo fijo. En su lugar, la administración de la empresa decide si pagar dividendos comunes y cuándo.

Debido a que los flujos de caja futuros son inciertos, debemos usar modelos para estimar el valor de las acciones comunes.

## Dividend Discount Models (DDMs)

Tres enfoques que los analistas usan frecuentemente:

### 1. Tasa Constante
Asume una tasa constante para cada dividendo futuro.

### 2. Modelo de Gordon
Utiliza el modelo de Gordon para crecimiento constante.

### 3. Multistage DDM
Asume una tasa de crecimiento cambiante de dividendos. Esencialmente, asumimos un patrón de dividendos en el corto plazo, como un período de alto crecimiento, seguido por una tasa de crecimiento constante de dividendos en el largo plazo.

**Proceso:**
- Descontar los dividendos esperados en el corto plazo como flujos de caja individuales
- Aplicar el DDM de crecimiento constante al largo plazo
- El DDM de crecimiento constante nos da un valor para una acción equity **un período antes** del dividendo que usamos en el numerador

> **Recordatorio del examen de Finanzas II:** Primero se llevaba lo que se indicaba el dividendo, luego con la tasa perpetua se llevaba un período más y se aplicaba el modelo de Gordon.

---

## Ejercicios Prácticos

### Ejercicio 1: Terry Corporation Preferred Stock
**Problema:** Las acciones preferentes de Terry Corporation se espera que paguen un dividendo anual de $9 a perpetuidad. Si la tasa de rendimiento requerida en una inversión equivalente es 11%, una acción de Terry preferente debería valer:

**Solución:**
```
Precio = Dividendo / r = $9 / 0.11 = $81.82
```

**Respuesta:** A. $81.82

### Ejercicio 2: Dover Company Bonds
**Problema:** Dover Company quiere emitir $10 millones de valor nominal de bonos a 10 años con una tasa de cupón anual de 5%. Si el yield requerido por los inversionistas en los bonos de Dover es 6%, la cantidad que la empresa recibirá cuando emita estos bonos será:

**Análisis:**
- **Valor nominal (face value):** $10 millones
- **Cupón anual:** 5% de 10M = $0.5 millones
- **Plazo:** 10 años
- **Rendimiento requerido:** 6%

###  Concepto Clave:
- Cuando el **cupón < yield requerido**, el bono se vende **con descuento** → el precio es **menor al valor nominal**
- Cuando el **cupón = yield requerido**, el bono se vende **a la par**
- Cuando el **cupón > yield requerido**, el bono se vende **con prima** → el precio es **mayor al valor nominal**

En este caso: **5% < 6%**, entonces el bono vale **menos que $10 millones**.

**Respuesta:** A. less than $10 million.