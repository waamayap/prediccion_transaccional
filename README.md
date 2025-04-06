# prediccion_transaccional
Datos y Exploración Inicial:

El conjunto de datos procesado cuenta con 124 registros, con dos métodos de pago (CARD y TRANSFER) balanceados.

Las estadísticas descriptivas muestran una variabilidad considerable en los volúmenes de transacciones, lo que requiere modelos capaces de capturar tanto patrones generales como comportamientos atípicos.

Random Forest:

Desempeño en Conjunto de Prueba:
Con hiperparámetros ajustados, se obtuvo un MAE de aproximadamente 1.64, MAPE de 6.87%, RMSE de 1.94 y un R² de 0.75 en el período evaluado.

Validación Cruzada:
Los resultados de validación cruzada muestran cierta inestabilidad (con R² que varían incluso siendo negativos en algunos pliegues).

Conclusión:
Random Forest ofrece resultados razonables en el período de prueba, pero la variabilidad en la validación sugiere que el modelo podría beneficiarse de más datos, lo que ayudaría a definir con mayor claridad la dinámica subyacente y mejorar la robustez de las métricas evaluadas.

ARIMA:

Desempeño:
ARIMA presentó un MAE de 2.73, MAPE de 13.37%, RMSE de 3.09 y un R² de 0.36, además de advertencias sobre parámetros no estacionarios e invertibles.

Conclusión:
Este modelo tiene dificultades para capturar la dinámica de la serie con la cantidad de datos disponibles, lo que indica que, para series con alta variabilidad, un conjunto de datos más amplio podría ayudar a estabilizar la estimación de parámetros y mejorar el desempeño.

Prophet:

Desempeño:
Prophet obtuvo un MAE de 1.7051, MAPE de 8.38%, RMSE de 2.03 y un R² de 0.73, ofreciendo además una buena descomposición en componentes y capacidad para detectar anomalías.

Conclusión:
Prophet es robusto y ofrece información interpretativa valiosa (tendencia, estacionalidad y anomalías). No obstante, ampliar el conjunto de datos permitiría validar y afinar estos componentes, especialmente en escenarios con cambios estacionales o eventos atípicos.

XGBoost:

Desempeño en Conjunto de Prueba:
Con la optimización de hiperparámetros mediante GridSearchCV, XGBoost mostró un MAE de 0.61, MAPE de 2.73%, RMSE de 0.87 y un R² de 0.95, indicando una precisión muy alta.

Validación Cruzada:
Aunque XGBoost destaca en el conjunto de prueba, la validación cruzada revela una variabilidad en los pliegues, lo que sugiere que su desempeño podría mejorar aún más con más datos disponibles.

Conclusión:
XGBoost es el modelo con mejor desempeño en términos de precisión, pero para confirmar y generalizar estos resultados, es crucial disponer de un mayor volumen de datos que abarque distintos períodos y condiciones del mercado.

