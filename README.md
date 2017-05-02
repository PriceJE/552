# 552
Usage Analysis (CAN)
> library(readr)
> R_552 <- read_csv("R_552.csv")
Parsed with column specification:
cols(
  BIID = col_character(),
  MODEL_ID = col_character(),
  REPORTABLE_PR_NAME = col_character(),
  PRINTER_FAMILY = col_character(),
  TECH_SPLIT = col_character(),
  PLATFORM_NM = col_character(),
  SN = col_character(),
  HOST_SUPPLY = col_integer(),
  INSTALL_DATE = col_character(),
  COLOR = col_character(),
  PEN_CHANGE_CNT = col_integer(),
  LEAD_COLOR = col_character(),
  LAG_COLOR = col_character(),
  LAG_DATE = col_character(),
  DATE_DIFF = col_integer()
)
|===================================================================================================================| 100%   89 MB
> View(R_552)
> attach(R_552)
> summary(R_552)
> install.packages("ggplot2")

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM=x$PLATFORM_NM), FUN=sum)

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM=x$PLATFORM_NM), FUN=mean)

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM=x$PLATFORM_NM), FUN=median)
           
> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM=x$PLATFORM_NM), FUN=mode)

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM=x$PLATFORM_NM), FUN=max)

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM=x$PLATFORM_NM), FUN=min)

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM, COLOR), FUN=mean)

> aggregate(x$DATE_DIFF, by=list(PLATFORM_NM, COLOR), FUN=median)
