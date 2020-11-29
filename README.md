# continuous time markov chain simulation

```
A<-rbind(c(-0.2,0.1,0.1),
         c(0.05,-0.1,0.05),
         c(0.15,0.15,-0.3))

expm::expm(A)

tol<-0.01
Adt<-diag(3)+A*tol
result<-Adt
for(ii in 2:(1/tol))result<-result%*%Adt
result-expm::expm(A)

tol<-0.001
Adt<-diag(3)+A*tol
result<-Adt
for(ii in 2:(1/tol))result<-result%*%Adt
result-expm::expm(A)

tol<-0.0001
Adt<-diag(3)+A*tol
result<-Adt
for(ii in 2:(1/tol))result<-result%*%Adt
result-expm::expm(A)

tol<-0.00001
Adt<-diag(3)+A*tol
result<-Adt
for(ii in 2:(1/tol))result<-result%*%Adt
result-expm::expm(A)
```
