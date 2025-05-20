**1NF:** Any relational schema R is said to be in 1NF if domain of all the attributes of Reln are atomic (domains must be indivisible)

**2NF:** Reln schema R is said to be in 2NF if it is in 1NF and there should not be any non-primary key attribute which is fully functional dependent on subset of primary key

**3NF**: should be in 2NF and must not contain any transitive dependency
all alpha -> beta 
beta != Non Primary
![[Pasted image 20250305064859.png]]
![[Pasted image 20250512190339.png]]

![[Pasted image 20250305054036.png]]
Pseudo Transitive
$$\alpha \rightarrow \beta,\space \beta \gamma \rightarrow \delta, \space \alpha \gamma \rightarrow \delta$$

**BCNF:** R is said to be in BCNF under F if all the FDs under F+ of the type alpha -> beta where alpha, beta are subset of R one of the following condition is true -
1. alpha -> beta is a trivial FD
2. alpha is super key

![[Pasted image 20250512190441.png]]

![[Pasted image 20250514192258.png]]
![[Pasted image 20250514192310.png]]

![[Pasted image 20250514200359.png]]

![[Pasted image 20250515104445.png]]

![[Pasted image 20250515104453.png]]

![[Pasted image 20250515104502.png]]

![[Pasted image 20250515112926.png]]