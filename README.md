# PDBothHistograms
# This is the code for creating the histograms for the PD data for SEL for the NASP conference presentation
both =read.csv("both.csv", header = TRUE)
both = both[, 2:3]; both
hist(both$PD)
both1 = both[both$Category %in% c(1), ]
both2 = both[both$Category %in% c(2), ]
hist(both1$PD)
hist(both2$PD)
 
