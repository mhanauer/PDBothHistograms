# PDBothHistograms
# This is the code for creating the histograms for the PD data for SEL for the NASP conference presentation
setwd("~/Desktop/DBDA2Eprograms")
both =read.csv("both.csv", header = TRUE)
both = both[, 2:3]; both
hist(both$PD)
both1 = both[both$Category %in% c(1), ]
both2 = both[both$Category %in% c(2), ]
hist(both1$PD, ylab = "SEL Satisfaction Score", xlab = "Frequency", main = "Primary SEL Satisfaction")
hist(both2$PD, ylab = "SEL Satisfaction Score", xlab = "Frequency", main = "Secondary SEL Satisfaction")


