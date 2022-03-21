# Assignment One
## Part A
**Meme**

![myMeme](https://user-images.githubusercontent.com/102003798/159208311-4c50f373-e547-4e5a-8cf0-051e51360d4a.png)


*Here is the code that generated it*

```r
library(magick)
Bachelors <- image_read("https://i.kym-cdn.com/photos/images/original/000/796/301/5c5.png") %>%
  image_scale(400)

Masters <- image_read("https://i.kym-cdn.com/photos/images/original/000/838/384/c62.png") %>%
  image_scale(400)

Doctorate <- image_read("https://i.imgur.com/9yBu9Pr.png") %>%
  image_scale(400)


GraduateRole <- image_read("https://i.imgflip.com/53e2uy.png") %>%
  image_scale(400)

imageVector <- c(Bachelors, Masters, Doctorate, GraduateRole) %>%
  image_append(stack = TRUE)


firstBox <- image_blank(height = 175, color = "#000000", width = 400) %>%
  image_annotate(text = "Undergrad", color = "#989898", size = 60, font = "Calibri", gravity = "center")

secondBox <- image_blank(height = 400, color = "#000000", width = 400) %>%
  image_annotate(text = "Masters", color = "#989898", size = 60, font = "Calibri", gravity = "center")

thirdBox <- image_blank(height = 400, color = "#000000", width = 400) %>%
  image_annotate(text = "Doctorate", color = "#989898", size = 60, font = "Calibri", gravity = "center")

fourthBox <- image_blank(height = 175, color = "#000000", width = 400) %>%
  image_annotate(text = "First Day of Work", color = "#989898", size = 40, font = "Calibri", gravity = "center")

textVector <- c(firstBox, secondBox, thirdBox, fourthBox) %>%
  image_append(stack = TRUE)


meme <- c(imageVector, textVector) %>%
  image_append()

image_write(meme, "myMeme.png")
```

This meme was generated to resonate with University students who endure long years of study and can sometimes feel a little overwhelmed. It serves two purposes:
- to provide a sense of catharsis 
- expand the reach and influence of spongebob squarepants

Here is a source list for the images used:
1. https://i.kym-cdn.com/photos/images/original/000/796/301/5c5.png
2. https://i.kym-cdn.com/photos/images/original/000/838/384/c62.png
3. https://i.kym-cdn.com/photos/images/original/000/838/384/c62.png
4. https://i.imgflip.com/53e2uy.png
