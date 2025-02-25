---
Lecture-Date: 2024-10-28
Finish?: false
Study-Date:
---
---



# Types of ML Models

1. Geometric Models
	1. Linear Regression 
2. Logical Models
	1. Decision Tree
3. Probabilistic Models
	1. Logistic Regression

# Linear Regression Model 

![[Pasted image 20241215145106.png]]
## Cost Function 

![[Pasted image 20241215145240.png]]


![[Pasted image 20250101094058.png]]
الصورة تشرح كيفية اختيار قيمة **α\alpha** (معامل التعلم) في خوارزمية الانحدار التدريجي **Gradient Descent**.

### الحالات:

1. **α\alpha صغيرة جدًا:**
    
    - يحدث تقارب بطيء (Slow Convergence).
    - تستغرق الخوارزمية وقتًا أطول للوصول إلى الحد الأدنى (Minimum).
2. **α\alpha كبيرة جدًا:**
    
    - قد تتجاوز النقطة الحد الأدنى (Overshoot the Minimum).
    - قد تفشل الخوارزمية في التقارب (Fail to Converge).
    - قد تنحرف النتائج تمامًا (Diverge).

### الحل:

- لمراقبة أداء الانحدار التدريجي:
    1. قم بطباعة قيمة دالة التكلفة **J(θ)J(\theta)** بعد كل تكرار.
    2. إذا لم تنخفض القيمة مع كل تكرار، قم بتعديل **α\alpha** إلى قيمة مناسبة.




- لما تكون كبيرة ممكن متوصلش لل Target بالظبط و بيكون فيه نسب احسن بس مش عارف توصلها بسب الكبر بتاعها 
- لما تكون صغيرة هتاخد ايام و اسابيع عشان توصل للتاريجت 