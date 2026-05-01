---
theme: uncover
paginate: true
font-size:30px
---

## [Prueba técnica](https://github.com/marcoisrael/DefaultCCC/blob/master/prueba-tecnica-Marco-Israel-Rodriguez-Cornejo.ipynb)
## Ciencia de Datos

Marco Israel Rodríguez Cornejo


---

El objetivo es implementar modelos de machine learnig para predecir las variables "PAY_AMT4" y "default payment next month"
usando la base de datos ["Default of Credit Card Clients"]("https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients")

---

Para la variable "default payment next month" se implementaron lo siguientes modelos.
<center>

|Modelo|Accuracy|F1 score|ROC AUC|
|------|--------|--|-------|
|LogisticRegression|0.7892|0.1085|0.5255|
|DecisionTreeClassifier|0.7965|0.2946|0.5795|
|ExtraTreesClassifier|0.7835|0.3224|0.5861|
|Neural Network|0.7973|0.3665|0.6844|
</center>

---


Para la variable "PAY_AMT4" se implementaron los siguientes modelos.
<center>

|Modelo|$R^2$|RMSE|
|------|-----|----|
|LinearRegression|0.1456|14756|
|GradientBoostingRegressor|0.5507|10700|
|ExtraTreesRegressor|0.6187|9857|
|Neural Network|-0.1758|0.0189|

</center>

---

## Conclusiones
La variable 'default payment next month' se logro modelar con una valor de Accuracy cercano a 0.8 en los tres modelos de clasificación y  el modelo de  red neuronal.


En la practica el modelo acierta en predecir si el cliente pagara su deuda crediticia el mes próximo 4 de cada 5 casos. Este nivel de precisión es muy bajo y de implementarse puede causar una gran número de falsos positivos. Implementar variables externas como la inflación, festividades y ciclos empresariales podría aumentar la precisión de las predicciones así como suministrar datos adicionales de los clientes.

---

La variable 'PAY_AMT4' obtuvo un rendimiento muy inferior, el mejor modelo en las pruebas fue ExtraTreesRegressor con un valor de $R^2$=0.6187 y RMSE=9857. En este caso el nivel de precisión del mejor modelo no es confiable para predecir pagos individuales pero podria dar un aproximado  del ingreso total de los pagos recibidos para el mes próximo.

---

## Referencias

Yeh, I-Cheng. "Default of Credit Card Clients." UCI Machine Learning Repository, 2009, https://doi.org/10.24432/C55S3H.
