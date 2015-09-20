# Coursera-Getting-and-cleaning-data
Quiz

fileurl<-

download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fdata%2Fss06hid.csv?accessType=DOWNLOAD",destfile = "E:/Study_Materials/Coursera/Getting_Started_and_Cleaning/hid.csv")

list.files


da<-read.csv("E:/Study_Materials/Coursera/Getting_Started_and_Cleaning/hid.csv")

head(da$VAL)

valu<-subset(da,da$VAL>=24,na.rm=T)


length(valu$VAL)



# Q.2

da$FES


1000000-1000000


#Q.3 Downloadin excel file
download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fdata%2FDATA.gov_NGAP.xlsx?accessType=DOWNLOAD",destfile="E:/Study_Materials/Coursera/Getting_Started_and_Cleaning/gov.xslx")

install.packages("xlsx")
library(xlsx)

gov<-read.xlsx("E:/Study_Materials/Coursera/Getting_Started_and_Cleaning/getdata-data-DATA.gov_NGAP.xlsx",sheetIndex=1,header=TRUE)
head(gov)

dat<-gov[nrow=18:23,ncol=7:15]
  
sum(dat$Zip*dat$Ext,na.rm=T)

#Q.4 read xml
install.packages("xml")
library(XML)
download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fdata%2Frestaurants.xml?accessType=DOWNLOAD",destfile="E:/Study_Materials/Coursera/Getting_Started_and_Cleaning/amer.xml")


ameri<-xmlTreeParse("E:/Study_Materials/Coursera/Getting_Started_and_Cleaning/amer.xml",useInternal=TRUE)

rootNode<-xmlRoot(ameri)

xmlName(rootNode)

rootNode[[1]][[1]][[2]]==21231

c<-xmlSApply(rootNode,"//row_id[@zipcode=='21231']",xmlValue)

rootNode[[1]][[1]][[2]]

zipcode21231


