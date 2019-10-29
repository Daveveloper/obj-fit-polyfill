# obj-fit-polyfill

## Project setup
```
npm install
```

## Implementation:
```
import objectFitImages from 'object-fit-images';
in Mount hook call objectFitImages:
  mounted() {
    objectFitImages();
  }
Add to your CSS classes:
font-family: 'object-fit: cover; object-position: left bottom;';
```

