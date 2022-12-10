# Study-Notes
Statistics/ML/Coding notes

2022.12.9
Multiple Testing

Intuition: 
- \alpha is the probability of false positive, Type I error (we need to control this)
- everything is fine in independent test
- but if we do 10000 tests with \alpha=0.05, then 10000*0.05=500 false positives 
    * if in medical situation, this is problematic 
- and P(at least one false positive)=1-(1-\alpha)^m, where m is the number of tests
    * this value goes up quickly 

Solution:
- Bonferroni correction (belongs to controlling Family-Wise Error Rate)
      -New \alpha*=\alpha/m, where m is the number of tests
      -But this method could make false negative slip away as well
      -Generally don't use it
- False Discovery Rate(FDR)
      -Commonly used
      -Check the algorithm on your own on ZhiHu
