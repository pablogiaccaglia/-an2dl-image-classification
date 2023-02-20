# 🧠🌿 Artificial Neural Networks & Deep Learning Project

## Image Classification
- 📙 [Description](#-description)
- 🗄️ [Dataset](#%EF%B8%8F-dataset)
- ⚙ [System requirements️](#-system-requirements)
- 🚀 [Setup instructions](#-setup-instructions)
- 📃 [Project specification](Project%20Proposals.pdf)
- 🗣️ [Presentation](Presentation.pdf)
- 📜 [Report](Report.pdf)
- 🤵 [Authors](#-authors)
- 📝 [License](#-license)

# 📙 Description

The Politecnico di Milano is hosting its first challenge for the Artificial Neural Networks and Deep Learning course of 2022, and this repository serves as the platform for it. Participants will be tasked to classify various species of plants, divided into 8 categories based on their plant species. The objective of this challenge is to accurately predict the correct class label when presented with an image, making it a classification problem.

The model me and my team developed uses the transfer learning approach with ConvNeXtLarge as the base model.

Our team arrived second in the challenge, reaching an accuracy of **94.46%**, you can check the results [here](https://codalab.lisn.upsaclay.fr/competitions/8522#results)

# 🗄️ Dataset
You can find the dataset [here](original-data).

The dataset provided is structured in a single folder containing the following classes:
- Species1 : **186** images
- Species2 : **532** images
- Species3 : **515** images
- Species4 : **511** images
- Species5 : **531** images
- Species6 : **222** images
- Species7 : **537** images
- Species8 : **508** images 

<p align="center">
    <img src="https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/output.png" width="500" alt="vanilla social influence"/>
</p>

The dataset contains in total **3542** images of size **96x96**

## Examples

Species 1 |  Species 2 | Species 3 | Species 4 | Species 5 | Species 6 | Species 7 | Species 8
:-------------------------:|:-------------------------:|:-------------------------|:-------------------------|:-------------------------|:-------------------------|:-------------------------|:-------------------------:
![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species1/00000.jpg)| ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species2/00000.jpg) | ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species3/00000.jpg) | ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species4/00000.jpg) | ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species5/00000.jpg) | ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species6/00000.jpg) | ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species7/00000.jpg) | ![](https://github.com/pablogiaccaglia/an2dl-image-classification/blob/main/original_data/Species8/00000.jpg) 

---

## Models details
For more details about the model check the [Report](Report.pdf). Briefly, we used the following techniques:
1. Transfer Learning with `ConvNeXtLarge` model.
2. CutMix & MixUp & CutOut data augmentation techniques: one of these techniques was applied to each input image
3. Standard data augmentation (flip, rotate, zoom)
4. [Test-Time data augmentation](https://machinelearningmastery.com/how-to-use-test-time-augmentation-to-improve-model-performance-for-image-classification/) (self-ensemble technique) with shifts and flips
5. [Class weighting](https://www.tensorflow.org/tutorials/structured_data/imbalanced_data#class_weights) to fight the imbalance of the dataset

## Results
Our best model reached an accuracy of **95%** on the validation set and **94.46%** accuracy in the hidden test provided by the challenge host.\
F1-score table on the test set:
||Species 1|Species 2|Species 3|Species 4|Species 5|Species 6|Species 7|Species 8|
|---|---|---|---|---|---|---|---|---|
|**F1-score**|0.8909|0.9477|0.9753|0.9451|0.9526|0.9535|0.9790|0.9130|

Final position: **2** out of **300**.

# ⚙ System requirements

## Required software

- [Jupyter Notebook](https://jupyter.org) or [Google Colab](https://colab.research.google.com)
- Python modules in [requirements.txt](requirements.txt)

# 🚀 Setup instructions
Clone: 
```sh
git clone https://github.com/gccianmario/Online-learning-application-projects/
pip install -r requirements.txt
```

---

# 🤵 Authors
| Surname            | Name      | Contact Info                       |
|:-------------------|:----------|:-----------------------------------|
| Breda              | Leonardo | leonardo.breda@mail.polimi.it   |
| Giaccaglia         | Pablo     | pablo.giaccaglia@mail.polimi.it    |
| La Conca           | Alessandro      | alessandro.laconca@mail.polimi.it      |

# 📝 License

This file is part of "Artificial Neural Networks & Deep Learning Project".

"Artificial Neural Networks & Deep Learning Project" is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

"Artificial Neural Networks & Deep Learning Project" is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License along
with this program (LICENSE.txt).  If not, see <http://www.gnu.org/licenses/>
