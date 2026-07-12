# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Location-Based Methods for Boundary Discontinuity Design Use rd2d With (In) R Software
install.packages("rd2d")

library("rd2d")
# Estimation Location-Based Methods for Boundary Discontinuity Design Use rd2d With (In) R Software
rd2d_ = read.csv("https://raw.githubusercontent.com/timbulwidodostp/rd2d_/main/rd2d_/rd2d_.csv",sep = ";")
Y <- rd2d_$Y
X1 <- rd2d_$X1
X2 <- rd2d_$X2
assignment <- rd2d_$assignment
X <- cbind(X1, X2)
b <- matrix(c(0, 0, 0, 1), ncol = 2)
rd2d <- rd2d(Y, X, assignment, b, params.cov = "main", masspoints = "off", bwcheck = 10)
summary(rd2d)
summary(rd2d, cbands = "main")
# Location-Based Methods for Boundary Discontinuity Design Use rd2d With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished