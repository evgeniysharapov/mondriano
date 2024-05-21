# History 

Piet Mondrian was a [dutch abstractionist painter](https://www.theartstory.org/artist/mondrian-piet/) who is most
famous for his work is 

![Composition with Large Red Plane, Yellow, Black, Gray and Blue](https://www.theartstory.org/images20/works/mondrian_piet_4.jpg "Composition with Large Red Plane, Yellow, Black, Gray and Blue")

Theare are pleny of inspired work that could be found on the internet. Here we try to generate similar art using [ConTeXt](https://wiki.contextgarden.net/Main_Page)

# Generating Images 

Normally we are given a page do we will use it's dimensions `\paperwidth` and `\paperheight`.

We start with a layout setup 

```tex
\setuppapersize[A4,landscape]
\setupcolors[state=start]
```

Then we will proceed with the following:

- split our current rectangle in two by randomly chosing a splitting point. Splitting could be randomly chosen horizontal or vertical
- after drawing a line we randomly choose what segments of that line to remove
- this is repeated for N times 
- have a grid ready to be filled

We will use `MetaPost` for the whole page so it's appropriate 

```tex
\starttext
\startMPpage

  ... actual code ...

\startMPpage
\stoptext
```


Generating image is as simple as running [ConTeXt](https://wiki.contextgarden.net/Main_Page)


```shell 
context mondriano.tex
```

