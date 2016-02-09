# quiz1gas
getting and cleaning data

##> setwd("~/Desktop/assignment")
##> download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fdata%2FDATA.gov_NGAP.xlsx",destfile = "gas")
##> library(xlsx)
##> full<-read.xlsx("gas",1,header = FALSE)
##> chunk <- apply(full[c(18:23),c(7:15)],1, function(x){paste(x, collapse="\t")})
##> dat<-read.table(text=chunk,header=TRUE,sep="\t") #note:chunk is not a file so use text= to get the text out 
##> sum(dat$Zip*dat$Ext,na.rm=T)
