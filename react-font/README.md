# How to add Fonts to a React Project


## Using @font-face
```
@font-face {
  font-family: 'Open Sans';
  font-style: normal;
  font-weight: 400;
  src: url('../fonts/open-sans-v13-latin-regular.eot'); /* IE9 Compat Modes */
  src: local('Open Sans'), local('OpenSans'),
       url('../fonts/open-sans-v13-latin-regular.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../fonts/open-sans-v13-latin-regular.woff2') format('woff2'), /* Super Modern Browsers */
       url('../fonts/open-sans-v13-latin-regular.woff') format('woff'), /* Modern Browsers */
       url('../fonts/open-sans-v13-latin-regular.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../fonts/open-sans-v13-latin-regular.svg#OpenSans') format('svg'); /* Legacy iOS */
}
body {
  font-family: 'Open Sans';
}
```

## @font-face 
**[Titillium Web](https://fonts.google.com/?selection.family=Titillium+Web:300,400,700)**
To quickly add the fonts to our react project, simple open public/index.html and paste the embed code provided within the tags.
```
<link href="https://fonts.googleapis.com/css?family=Titillium+Web:300,400,700" rel="stylesheet">
```
Save the file and edit the src/index.css and add this:
```
body {
  font-family: 'Titillium Web', sans-serif
}
.heading {
  font-weight: 700;
}
.subheading {
  font-weight: 300;
}
```

## Using Web Font Loader
```
npm install webfontloader --save
```
Open src/index.js and add the following code
```
import WebFont from 'webfontloader';

WebFont.load({
  google: {
    families: ['Titillium Web:300,400,700', 'sans-serif']
  }
});
```