# Homework1
Homework1 from 10.03.2022 By AleksandarKirilov 200 028 FEBA AFDA 
# Problem 1
for(i in 1:10) {
  print(i*3)
}

# Problem 2
for(i in rnorm(1:10)){
  if(i>1){
    print(i) 
  }
}

# Problem 3 
#1 will be for men and 0 for women
people <- c(rep("1", 6), rep("0", 8))
ResultVector <- NULL

for (i in 1:10000){ 
  choose <- sample(people, size = 5, replace = FALSE)
  
  if (sum(choose=="1")==3){
    ResultVector<-c(ResultVector,1)
  } else{
    ResultVector<-c(ResultVector,0)
  }
  
}
sum(ResultVector)/10000

# Problem 4

profit = 0
for(k in 10:1000){
  price <- 100
  for (x in 1:100){
    price <- price + rnorm(1, mean = 0, sd=7)
  }
  if(price >= 120){
    profit <- profit + (price - 120)
  }
}
print(profit/1000)
  
