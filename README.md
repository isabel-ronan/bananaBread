# Banana Bread - Cake or Bread?

## Overview
- This repository houses all code related to the proving that banana bread is a bread and not a cake. 
- The dataset is a series of recipes scraped from the BBC Good Food website. The cake labels are derived from the [Classic Cakes Collection](https://www.bbcgoodfood.com/recipes/collection/classic-cake-recipes), the bread labels are derived from the [Bread Recipes Collection](https://www.bbcgoodfood.com/recipes/collection/bread-recipes). Banana breads are in their own category and are kept separately until prediction time. 

## Experiment 1 `knnClassifier.ipynb`
- Uses KNN with various hyperparameters to determine bread-cake classifier wih highest accuracy. 
- Obtains 93.3% accuracy on sample test data. 
- Predicts the majority of banana breads as cakes (14 cakes and 8 breads).

## Experiment 2 `moreClassifiers.ipynb`
- Fueled by lack of success using simple KNN, a variety of classic ML algorithms are used to train several classifiers. The one with the highest accuracy will subsequently be used to assess banana breads. 
- was the best algorithm.
- Still predicts the majority of banana breads as cakes (15 cakes and 7 breads).

## Experiment 3 `simpleLLM.ipynb`
- As there must be some experiment to show that banana bread is in fact bread, I have resorted to LLMs.
- Compare vectors of 'cake' vs 'bread' vs 'banana bread'
- Using cosine similarity, we are finally getting somewhere. 
- 'Bread' is closer in vector space to 'banana bread' than 'cake' is to 'banana bread'.

## Experiment 4 `allIngredientsLLM.ipynb`
- Use an LLM to make sense of the ingredients for either cake, bread, or banana bread.
- Which is closer, cake or bread in vector space to banana bread (with ingredients considered). 
- The distance between the cake to banana bread embeddings is greater than the distance from the bread to banana bread embeddings, meaning that cake is less similar to banana bread than bread. 