#for webscraping
#install.packages("rvest")
#install.packages("dplyr")
library(rvest)
library(dplyr)

link = "https://topnow.se/"
page = read_html(link)

title =  page%>%
  html_nodes(".titles a") %>%
  html_text()
title

mega = page%>%
  html_nodes(".card_overlay") %>%
  html_text()
mega

youtube = page%>%
  html_nodes(".streaming_icon") %>%
  html_text()
youtube

movie = data.frame(title, mega, stringAsFactors = FALSE)

write.csv(movie, "movie.csv")


site="https://guardian.ng/politics/intrigues-suspense-as-contenders-for-apc-national-chairmanship-set-for-final-battle/"
google= read_html(site)


words =  google%>%
  html_nodes(".has-preview .title") %>%
  html_text()
words
