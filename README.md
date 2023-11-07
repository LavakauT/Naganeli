# Naganeli
Naganeli means my name or my identification in Rukai tribe.

![family](https://github.com/LavakauT/Naganeli/assets/132649549/2150e19e-438b-4dca-b32d-8ebe77e9dd8b)

```
# install.packages("kinship2", dependencies = TRUE)
require(kinship2, quietly = TRUE)
df <- read.csv('/Users/shalimalaolawagao/Desktop/family.csv')

family <- pedigree(id = df$Name,
                   dadid = df$Dad,
                   momid = df$Mom,
                   sex = df$Sexes, 
                   status = df$dead,
                   affected = df$Affect)



pdf('/Users/shalimalaolawagao/Desktop/family.pdf',
    width = 30, height = 5)
plot.pedigree(family)
pedigree.legend(family,
                location = "bottomright",
                labels = list("Factor VIII\nDeficiency",
                              "Myotonic\nDystrophy"), cex = 0.8, radius = 0.3)
dev.off()
```
