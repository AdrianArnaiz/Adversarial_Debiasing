# Adversarial_Debiasing

Example of how to debiasing a model using adversarial approach. Based on [Stijn Tonk](https://github.com/equialgo/fairness-in-ml)



## Contenido

Explicación de la utilización de modelo Adversarial Basado en GAN para realizar debiasing de un modelo. El modelo original realiza **predicciones de salario sesgadas por raza y sexo, visible mediante p%-rule (odds)**. 

A través de un **entrenamiento adversarial** (explicado en profundidad en el notebook), se consigue **des-sesgar** el modelo con sólo una pequeña penalización en el rendimiento.

|              	| **Clasificador** <br>**original** 	| **Clasificador**<br>**des-sesgado** 	|
|--------------	|---------------------------	|-----------------------------	|
| AUC          	| 0.9                       	| 0.82                        	|
| Accuracy     	| 0.85                      	| 0.81                        	|
| p%-rule sexo 	| 0.34                      	| **0.80**                      |
| p%-rule raza 	| 0.45                      	| **0.99**                      |

![](debiasing.gif)


## Fuentes

**Proceso ampliado, modificado, traducido y comentado de [*Fairness in ML* - *Stijn Tonk*](https://github.com/equialgo/fairness-in-ml).**

**Se ha realizado traducción de explicaciones, adición de algunas explicaciones, comentarios en el código y alguna pequeña modificación en el mismo.**

**Añadido anexo explicativo de GAN.**

* Explicación en [GoDataDriven](https://godatadriven.com/blog/towards-fairness-in-ml-with-adversarial-networks/)

* Notebook original en [EQUILAGO](https://github.com/equialgo/fairness-in-ml), basado en [UCBerkeley](https://fairmlclass.github.io/)

* Código originial en [EQUILAGO](https://github.com/equialgo/fairness-in-ml)

-----------
**Bibliografía del anexo sobre GANs**
1. Amini, A. (Enero de 2019). MIT 6.S191 (2019): Deep Generative Modeling. Obtenido de https://www.youtube.com/watch?v=yFBFl1cLYx8 
 
2. Goodfellow, I. (9 de Diciembre de 2016). Introduction to Generative Adversarial Networks. NIPS 2016 Workshop on Adversarial Training. Barcelona. Obtenido de http://www.iangoodfellow.com/slides/2016-12-9-gans.pdf 
 
3. Goodfellow, I. (2017 de Agosto de 24). Introduction to GANs, NIPS 2016 | Ian Goodfellow, OpenAI. Obtenido de https://www.youtube.com/watch?v=9JpdAg6uMXs 
 
4. Goodfellow, I., Pouget-Abadie, J., Mirza, M., Xu, B., Warde-Farley, D., Ozair, S., . . . Bengio, Y. (2014). Generative Adversarial Networks. En Z. Ghahramani, & M. Welling, Advances in Neural Information Processing Systems 27 (págs. 2672-2680). Curran Associates, Inc. Obtenido de http://papers.nips.cc/paper/5423generative-adversarial-nets.pdf

