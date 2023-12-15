- Optimiser = Adam
- Epochs = 20
---


# Model
![[Pasted image 20231213144507.png]]
- **Accuracy: 70%**
- Model is from Kaggle
- No Dropout / Augmentation

---
![[Pasted image 20231213145101.png]]
- Same Model but with 3 drop out layers
- One after each pooling layer
- And one at the end before the last dense layer

- 67% accuracy 
- Too many drop out layers

---
![[Pasted image 20231213145525.png]]
- 2 dropout layers
- 1 after each pooling layer
- Removed the third dropout layer at the end
- **Accuracy: 74%**
- Removing the dropout at the end increases the accuracy 

---
![[Pasted image 20231213151828.png]]
- increase the 2 dropout layers to 0.5
- **Accuracy 71%**
- perhaps too much dropout
---
![[Pasted image 20231213150228.png]]
- 1 dropout layer
- at the end before the last dense layer
- **Accuracy 72.6%**

---
![[Pasted image 20231213150758.png]]

- 1 dropout layer
- Increased the Dropout to 0.5
- at the end before the last dense layer
- Almost no increase in accuracy 
- **Accuracy 72.8%**

---
![[Pasted image 20231213152834.png]]
- No Dropout layers
- 1 Augmentation layer
- Random flip, Random rotation, random zoom
- careful not to augment it too much
- **Accuracy: 68%**
- Possibly too much augmentation

---
![[Pasted image 20231213154826.png]]
- Removed random rotation
- **Accuracy 74%**
- Nice improvement
- If the image is augmented too much the useful features from the images are gone

---
![[Pasted image 20231213155539.png]]
- Only augmenting the width and height by 10%
- **Accuracy of 74%**
---
![[Pasted image 20231213160724.png]]
- Combine the two together 
- **Accuracy 72%** 
- Too much augmentation
---

![[Pasted image 20231213162142.png]]
- Combine the best dropout model and the best augmentation model
- Model starts to underfit 
- Accuracy of 73%
---

 ![[Pasted image 20231213162214.png]]
---

![[Pasted image 20231215122555.png]]
- Some Augmentation & 1 dropout layer
- Underfits
- **Accuracy: 67%**

---

## Summary So Far
- 2 Dropout layers 1 after each pooling layer got 74%
- Image augmentation can get also get up to 74% 
- Augmenting the width/height, or the zoom and image flip produce the best result
- Have to be careful not to dropout too much or augment too much

## Takeaways
- Don't use too much dropout, careful where the dropout layers are. Too much dropout leads to underfitting
- 