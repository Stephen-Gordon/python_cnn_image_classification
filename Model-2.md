
![[Pasted image 20231215133849.png]](./Pasted%image%20231215133849.png)
- Doubling up layers in the base model gets 73% accuracy
---


  ![[Pasted image 20231215133940.png]]
  - Model overfits almost instantly
  - Possibly add some dropout here
---
![[Pasted image 20231215134406.png]]
- Remove the last Conv2D Layer
- **Accuracy 72%**

---
![[Pasted image 20231215135123.png]]
- **Almost 76% Accuracy 
- Best performance yet
---

![[Pasted image 20231215141434.png]]
- However it still overfits   
---
Can start to see, changing the layers is making much more of a difference 

---

![[Pasted image 20231215143254.png]]
- Adding in 3 Dropouts
- 1 after each pooling layer
---
![[Pasted image 20231215143635.png]]
- Improves accuracy by 2% to 78%
- Now takes more epochs before overfitting
  
  ---
  ![[Pasted image 20231215163541.png]]
  - Increase the dropout deeper in the network
  - reduces a neurons reliance on each other
  - Too much dropout here 

---
![[Pasted image 20231215164720.png]]
- Slowly increase the dropout
- Model got to 80%
---
Adding augmentation on top of Dropout
Model underfits

  
  
