# Are_we_too_mean_to_the_mean_square <br>
Inspired by Andrew Ng's machine learning lectures, this project tries to answer the question "Are we too mean to the mean<br> square cost function??" in the context of logistical regression classifier model. In the lectures on Logistical regression(LR), <br>
Andrew Ng points out that we do not use mean square cost function for LR as it has non convex nature as function of <br>
weights (or coefficient). I wanted to test this idea on few datasets and see it happening. However, for the very simple datasets which are publicly available online
- Iris Dataset<br>
- Loan Prediction Dataset<br>
- Adult Income Dataset<br>
- Car Evaluation

It seems that mean square cost function works better, at least has a better computation time. The gradient decents seems <br>
to always lead to the singular minimum. So the answer to the question whether "we are ignoring the mean square function's <br>
importance or not??" is most likely "no", given the amount of literature and people working on it. However, with these <br>
example datasets, it seems, we are probably too mean to it!!<br> <br>

PS - The file meanVscrossentropy.ipynb is almost independent of any other file. However, for other files to <br> understand the story properly it is reccomended to read them as Irisdataset --> 02Loanprediction_dataset --> <br>
03Adult_income_dataset --> 04Carevaluation.

Description:<br>
**meanVscrossentropy:** implents the **class Model** with instantiation of two objects (i) with mean square (ii) with cross-entropy cost function.<br>
**Class IncreaseCost inherits** the methods from **class Model** and also creates a **function Increase**.<br>

**Irisdataset:** implements function plotfeatures with plots different classes (Y-values) with respect to all the combinations of two features (X1-X2) depending which set of feautures are input in arguments. <br>
Function plotdecisionboundary creates an decision boundary on the plotted points by plotfeatures with or without solid fill. For creating the decision boundaries without the fill it first generates the interpolated function using meshgrid of (X1,X2), then finds out the mid Y-Values (0.5, 1.5 ... etc.). <br>
**02Loanprediction_dataset,03Adult_income_dataset,04Carevaluation:** all use the function from Irisdataset, and also implement Recursive feature elimination with cross-validation from ski-learn to look for best features that could used by Classes Model and IncreaseCost.
