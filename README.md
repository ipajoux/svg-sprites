# SVG Sprites

```css
.icon {
  --icon-size: 24px;
  --icon-color: #000;
  
  --icon-sprite-svg: url();
  --icon-sprite-size: ; /* total icons in columns and rows (em) */
  --icon-position: 0 0;
  
  display: inline-block;
  position: relative;
  
  width: var(--icon-size);
  height: var(--icon-size);
  font-size: var(--icon-size);
}

.icon::before {
  position: absolute;
  width: 100%;
  height: 100%;
  
  -webkit-mask-image: var(--icon-sprite-svg);
  -webkit-mask-size: var(--icon-sprite-size);
  -webkit-mask-position: var(--icon-position);
  
  background-color: var(--icon-color);
  
  content: '';
}

.icon.foo {
  --icon-position: -1em 0; /* x,y index of icon (-em) */
}
```
