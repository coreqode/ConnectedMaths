---
title: "Covariance"
---

- Covariance gives us the relation of how the two data points are related. The data points may be multidimensional. 
- Data may be related with positive or negative trend, or no trend at all.
- Covariance only tells us if the data is positively or negatively related, but tells nothing about the strength of the relation. 
- They are sensitive to scaling.
- $cov(x,y) = \sum_{i=1}^n \frac{(x_i-\hat x) (y_i-\hat y)}{n}$
- **Covariance is an Inner Product in a vector space, more specifically the Quotient Space**.


# Correlation
- Used to calculate the strength of a relation of the data.
- Correlation equals $\pm1$ if we can draw a straight line through all the points.
- $corr(x,y) = \frac {cov(x,y)}{\sqrt{\sigma(x) \sigma(y)}}$
	The denominator makes sure that the data is between 0-1.	
	
	
# p-values
- Used to test the null-hypothesis.