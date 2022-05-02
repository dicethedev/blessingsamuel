
![blessingsamuel](https://user-images.githubusercontent.com/85754527/166171452-21de3c6d-e5c8-4c96-a424-aaee68c05526.PNG)


# blessingsamuel
My Portfolio Website In Progress. Built with Vue


# invoice

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### Animation of the Text behaviors ---

 npm install animate.css --save

 yarn add animate.css

 or add it this to the public folder in html

 <head>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
  />
</head>


### Responsiveness: Can be found in the _mixings.scss in styles inside assets folder

I import the _mixings.scss inside Home.vue for pixel it to mobile responsive

### Working with SCSS Files.

You will need a bit of sass/scss knowledge to begin with it

I created a file inside styles called "_mixings-method.scss" that is found in assets and inside styles i created folder named "components" inside the components in where i created a file that I want it to be mobile responsive. I went back to About.vue in views, i locate the css file that i style and copy it amd paste it inside the file that i created named "_section.scss" inside the components. Now, i went back to "_mixings-method.scss" to import the "_section.scss" in side the file so that it can work well with out errors. Then after that, i went back to About,vue inside the style i added @import "../assets/styles/_mixings-method.scss"; down below the last file so that it can work with the style in "_section.scss" for better display.


In "_mixings-method.scss" I created a this functions below:

@media (max-width: 750px){ 
     I added this @include fiunction because it is connecting to the style and display in the "_section.scss" file 
  @include section-laptop();
 }

@media (max-width: 1224px){ 
      I added this @include fiunction because it is connecting to the style and display in the "_section.scss" file 
    @include section-desktop();
 }  


And inside "_section.scss" below the style that I copy and paste inside it i went down below the styles and add this 

@mixin section-laptop(){
     .about-me {
          margin-top: 90px;
          margin-left: 50px;

          .head-numbering > h2 {
               
          }
     }
   }

   @mixin section-desktop(){

this where I will be working with my Responsiveness for that particular section in it either to mobile, tablet or desktop display.


