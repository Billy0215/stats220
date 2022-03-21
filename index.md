# Kia ora te ao!

**Welcome to my test website!**

## GitHub repository information

I am a computer science student of UoA. Here's my GitHub page: [GitHub](https://github.com/Billy0215).
And my Stats220 page: [Stats220](https://github.com/Billy0215/stats220),
you can find the meme images that I made.

## memes

Here are the memes I made using R package: [{magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html).
![Dami](https://raw.githubusercontent.com/Billy0215/stats220/main/my_meme.png)
*I made my memes using my cat Dami's pictures, I hope u like him.*

## code
Here is the code I worte for making the memes:

library(magick)

meme_size <- image_blank(width=400,height=1070,color="#000000")%>%
  image_annotate(text="woke up \n \n \n \n \n \n \n food detected",color="#FFFFFF",size=40,font="impact",gravity="center")
meme0 <- image_read("https://raw.githubusercontent.com/Billy0215/stats220/main/meme0.png") %>% image_scale(400)
meme1 <- image_read("https://raw.githubusercontent.com/Billy0215/stats220/main/meme1.png") %>% image_scale(400)
list <- c(meme0,meme1)
meme_pre <- image_append(list,stack=TRUE)
list1 <- c(meme_pre,meme_size)
meme <- image_append(list1)
image_write(meme,"my_meme.png")


meme2 <- image_read("https://raw.githubusercontent.com/Billy0215/stats220/main/meme2.png") %>% image_scale(400)
meme3 <- image_read("https://raw.githubusercontent.com/Billy0215/stats220/main/meme3.png") %>% image_scale(400)
meme4 <- image_read("https://raw.githubusercontent.com/Billy0215/stats220/main/meme4.png") %>% image_scale(400)
meme5 <- image_read("https://raw.githubusercontent.com/Billy0215/stats220/main/meme5.png") %>% image_scale(400)
list2 <- c(meme2,meme3,meme4,meme5)
meme_animation <- image_animate(list2,fps=1)
image_write(meme_animation,"my_meme.gif")


