library(RISmed)
search_topic <- c("SEER and lung cancer")
search_query2 <- EUtilsSummary(search_topic,db="pubmed", retmax=10000,datetype='pdat', mindate=2015, maxdate=2020)
summary(search_query2)

QueryId(search_query2)

##获取检索结果
records<- EUtilsGet(search_query2,Sys.sleep(0.1))
class(records)
str(records)

##提取检索结果
pubmed_data <- data.frame('Title'=ArticleTitle(records),
                          'Year'=YearAccepted(records),
                          'journal'=ISOAbbreviation(records))


head(pubmed_data,1)
pubmed_data[1:3,1]
write.csv(pubmed_data,file='lncRNA.csv')









