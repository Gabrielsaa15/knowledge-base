## Inferencia Causal mediante Ensayos Controlados Aleatorizados (RCTs)

En los **Randomized Control Trials (RCTs)** o ensayos controlados aleatorizados, las unidades de estudio se dividen al azar en dos grupos: uno recibe el tratamiento y el otro no. La idea central es que, al garantizar la aleatoriedad, se eliminan diferencias sistemáticas entre los grupos, permitiendo atribuir cualquier cambio en los resultados al tratamiento mismo. Esto convierte a los RCTs en el “estándar de oro” para la inferencia causal, ya que evitan confusiones entre correlación y causalidad.

Para entender esto, es fundamental conocer el **marco de resultados potenciales** (*Potential Outcomes Framework*). Este marco plantea que cada individuo tiene dos posibles resultados: \( Y(1) \), el que obtendría si recibe el tratamiento, y \( Y(0) \), el que tendría si no lo recibe. Estos valores son llamados **contrafactuales**, porque nunca se pueden observar al mismo tiempo: un mismo individuo no puede estar simultáneamente tratado y no tratado. Por eso, hablamos de lo **factual** (lo que efectivamente se observa) y lo **contrafactual** (lo que habría pasado bajo un escenario alternativo).

El **efecto individual del tratamiento** se define como la diferencia entre ambos escenarios:

$$
Y(1) - Y(0).
$$

Sin embargo, como no es posible observar ambos valores en una misma persona, lo que hacemos es estimar su promedio en la población, lo que se conoce como el **Average Treatment Effect (ATE)**:

$$
\delta = E[Y(1) - Y(0)] = E[Y(1)] - E[Y(0)].
$$

Este ATE nos dice, en promedio, cuánto cambia el resultado esperado cuando una población recibe el tratamiento comparada con cuando no lo recibe.

En la práctica, solemos tener datos **observacionales** además de datos **experimentales**. Con datos observacionales, lo que podemos calcular directamente es el **Average Predictive Effect (APE)**:

$$
\pi = E[Y \mid D = 1] - E[Y \mid D = 0],
$$

que simplemente mide la diferencia de medias entre los que recibieron el tratamiento (donde \( D = 1 \) indica tratamiento asignado) y los que no. Aunque este valor es identificable a partir de los datos, no necesariamente coincide con el ATE verdadero. De hecho, generalmente \( \delta  no es igual pi \), porque las personas que se exponen al tratamiento pueden diferir sistemáticamente de las que no lo hacen. A esta diferencia la llamamos **sesgo de selección (Selection Bias)**, y aparece porque:

$$
E[Y(d) \mid D = 1] \neq E[Y(d)],
$$

es decir, la asignación al tratamiento está correlacionada con factores que también influyen en los resultados potenciales. Este sesgo surge cuando el tratamiento no es aleatorio y está influido por variables no observadas o comportamientos individuales que afectan tanto la selección como el resultado.

### Ejemplo de Sesgo de Selección

Un ejemplo clásico del sesgo de selección se ilustra con el impacto del consumo de marihuana en la longevidad. Supongamos que fumar marihuana no tiene ningún efecto causal en la duración de la vida:

$$
Y = Y(0) = Y(1),
$$

por lo que el ATE es:

$$
\delta = E[Y(1)] - E[Y(0)] = 0.
$$

Sin embargo, en datos observacionales, el comportamiento de fumar (\( D \)) no es asignado al azar. Supongamos que las personas que fuman marihuana también tienden a tener hábitos de salud pobres, como beber alcohol en exceso, lo cual sí reduce la expectativa de vida. En este caso, observamos que, lo que genera un APE negativo:

$$
\pi = E[Y \mid D = 1] - E[Y \mid D = 0] < 0 = \delta.
$$

Aquí, el APE negativo refleja una correlación espuria debido al sesgo de selección: el hábito de fumar está asociado con otros factores negativos para la salud, no porque la marihuana en sí acorte la vida. Si realizáramos un RCT donde el consumo se asigna al azar, el sesgo desaparecería y \( \pi = \delta = 0 \).

La **aleatorización en los RCTs** resuelve este problema: al asignar el tratamiento de forma puramente al azar, se rompe la relación entre la decisión de tratamiento y los resultados potenciales, eliminando así el sesgo de selección.

Ahora bien, no siempre basta con estimar un efecto promedio. Muchas veces queremos entender cómo varía el impacto de un tratamiento según características específicas de los individuos, como edad, género o nivel de ingresos. Para ello usamos el concepto de **Conditional Average Treatment Effect (CATE)**:

$$
\delta(W) = E[Y(1) \mid W] - E[Y(0) \mid W],
$$

que nos permite estimar efectos de tratamiento condicionados en un conjunto de covariables ## Inferencia Causal mediante Ensayos Controlados Aleatorizados (RCTs)

En los **Randomized Control Trials (RCTs)** o ensayos controlados aleatorizados, las unidades de estudio se dividen al azar en dos grupos: uno recibe el tratamiento y el otro no. La idea central es que, al garantizar la aleatoriedad, se eliminan diferencias sistemáticas entre los grupos, permitiendo atribuir cualquier cambio en los resultados al tratamiento mismo. Esto convierte a los RCTs en el “estándar de oro” para la inferencia causal, ya que evitan confusiones entre correlación y causalidad.

Para entender esto, es fundamental conocer el **marco de resultados potenciales** (*Potential Outcomes Framework*). Este marco plantea que cada individuo tiene dos posibles resultados: \( Y(1) \), el que obtendría si recibe el tratamiento, y \( Y(0) \), el que tendría si no lo recibe. Estos valores son llamados **contrafactuales**, porque nunca se pueden observar al mismo tiempo: un mismo individuo no puede estar simultáneamente tratado y no tratado. Por eso, hablamos de lo **factual** (lo que efectivamente se observa) y lo **contrafactual** (lo que habría pasado bajo un escenario alternativo).

El **efecto individual del tratamiento** se define como la diferencia entre ambos escenarios:

$$
Y(1) - Y(0).
$$

Sin embargo, como no es posible observar ambos valores en una misma persona, lo que hacemos es estimar su promedio en la población, lo que se conoce como el **Average Treatment Effect (ATE)**:

$$
\delta = E[Y(1) - Y(0)] = E[Y(1)] - E[Y(0)].
$$

Este ATE nos dice, en promedio, cuánto cambia el resultado esperado cuando una población recibe el tratamiento comparada con cuando no lo recibe.

En la práctica, solemos tener datos **observacionales** además de datos **experimentales**. Con datos observacionales, lo que podemos calcular directamente es el **Average Predictive Effect (APE)**:

$$
\pi = E[Y \mid D = 1] - E[Y \mid D = 0],
$$

que simplemente mide la diferencia de medias entre los que recibieron el tratamiento (donde \( D = 1 \) indica tratamiento asignado) y los que no. Aunque este valor es identificable a partir de los datos, no necesariamente coincide con el ATE verdadero. De hecho, generalmente \( \delta \neq \pi \), porque las personas que se exponen al tratamiento pueden diferir sistemáticamente de las que no lo hacen. A esta diferencia la llamamos **sesgo de selección (Selection Bias)**, y aparece porque:

$$
E[Y(d) \mid D = 1] \neq E[Y(d)],
$$

es decir, la asignación al tratamiento está correlacionada con factores que también influyen en los resultados potenciales. Este sesgo surge cuando el tratamiento no es aleatorio y está influido por variables no observadas o comportamientos individuales que afectan tanto la selección como el resultado.

### Ejemplo de Sesgo de Selección

Un ejemplo clásico del sesgo de selección se ilustra con el impacto del consumo de marihuana en la longevidad. Supongamos que fumar marihuana no tiene ningún efecto causal en la duración de la vida:

$$
Y = Y(0) = Y(1),
$$

por lo que el ATE es:

$$
\delta = E[Y(1)] - E[Y(0)] = 0.
$$

Sin embargo, en datos observacionales, el comportamiento de fumar (\( D \)) no es asignado al azar. Supongamos que las personas que fuman marihuana también tienden a tener hábitos de salud pobres, como beber alcohol en exceso, lo cual sí reduce la expectativa de vida. En este caso, observamos que \( E[Y \mid D = 1] < E[Y \mid D = 0] \), lo que genera un APE negativo:

$$
\pi = E[Y \mid D = 1] - E[Y \mid D = 0] < 0 = \delta.
$$

Aquí, el APE negativo refleja una correlación espuria debido al sesgo de selección: el hábito de fumar está asociado con otros factores negativos para la salud, no porque la marihuana en sí acorte la vida. Si realizáramos un RCT donde el consumo se asigna al azar, el sesgo desaparecería y \( \pi = \delta = 0 \).

La **aleatorización en los RCTs** resuelve este problema: al asignar el tratamiento de forma puramente al azar, se rompe la relación entre la decisión de tratamiento y los resultados potenciales, eliminando así el sesgo de selección.

Ahora bien, no siempre basta con estimar un efecto promedio. Muchas veces queremos entender cómo varía el impacto de un tratamiento según características específicas de los individuos, como edad, género o nivel de ingresos. Para ello usamos el concepto de **Conditional Average Treatment Effect (CATE)**:

$$
\delta(W) = E[Y(1) \mid W] - E[Y(0) \mid W],
$$

que nos permite estimar efectos de tratamiento condicionados en un conjunto de covariables \( W \).

De manera análoga, a partir de datos se puede calcular el **Conditional Average Predictive Effect (CAPE)**:

$$
\pi(W) = E[Y \mid D=1, W] - E[Y \mid D=0, W],
$$

aunque, al igual que con el APE, este valor puede diferir del CATE verdadero si la asignación no es aleatoria.

En síntesis, el marco de resultados potenciales nos permite formalizar los efectos causales, el ATE nos da una medida promedio poblacional, y los RCTs —al eliminar el sesgo de selección mediante la aleatorización— aseguran que las comparaciones entre tratados y controles reflejen efectos causales y no simples correlaciones. Además, el uso de covariables a través del CATE y CAPE nos abre la puerta a estudiar la heterogeneidad de los efectos, algo clave para personalizar políticas y tratamientos. W \).

De manera análoga, a partir de datos se puede calcular el **Conditional Average Predictive Effect (CAPE)**:

$$
\pi(W) = E[Y \mid D=1, W] - E[Y \mid D=0, W],
$$

aunque, al igual que con el APE, este valor puede diferir del CATE verdadero si la asignación no es aleatoria.

En síntesis, el marco de resultados potenciales nos permite formalizar los efectos causales, el ATE nos da una medida promedio poblacional, y los RCTs —al eliminar el sesgo de selección mediante la aleatorización— aseguran que las comparaciones entre tratados y controles reflejen efectos causales y no simples correlaciones. Además, el uso de covariables a través del CATE y CAPE nos abre la puerta a estudiar la heterogeneidad de los efectos, algo clave para personalizar políticas y tratamientos.