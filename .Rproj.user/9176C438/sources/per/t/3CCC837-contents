
# Create the dend:
dend <- as.dendrogram(hclust(dist(mtcars)))

# Create a vector giving a color for each car to which company it belongs to
car_type <- rep("Other", length(rownames(mtcars)))
is_x <- grepl("Merc", rownames(mtcars))
car_type[is_x] <- "Mercedes"
is_x <- grepl("Mazda", rownames(mtcars))
car_type[is_x] <- "Mazda"
is_x <- grepl("Toyota", rownames(mtcars))
car_type[is_x] <- "Toyota"
car_type <- factor(car_type)
n_car_types <- length(unique(car_type))
cols_4 <- colorspace::rainbow_hcl(n_car_types, c = 70, l  = 50)
colIf <- cols_4[car_type]


### plots
par(mar = c(4,1,1,12))
plot(dend,horiz=T)
sw<-c(rep("00",12),rep("7c",20))
colored_dots(cbind(k234[,3:1], colIf), dend, rowLabels = c(paste0("k = ", 4:2), "Car Type"),horiz=T,alf=sw)