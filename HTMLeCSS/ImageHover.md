# Como criar um image hover 

1. Primeiro definimos o estilo do image hover:
```css
.container {
  position: relative;
  width: 50%;
}

.image {
  display: block;
  width: 100%;
  height: auto;
}
.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .5s ease;
  background-color: #f3920085;
}
.text {
  color: white;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}

.container:hover .overlay {
  opacity: 1;
}

```
2. Agora podemos finalizar com o HTML:
```html
<h2>Fade in Overlay</h2>
<p>Hover over the image to see the effect.</p>

<div class="container">
  <img src="https://mk0nationaltodayijln.kinstacdn.com/wp-content/uploads/2019/12/national-letter-writing-day-640x514.jpg" class="image">
  <div class="overlay">
    <div class="text">Hello World</div>
  </div>
</div>
```
<strong>Obs.: Definimos o conteúdo a ser exibido no hover através da <code>div class="overlay"</code>. </strong> 

### Referências:
- https://www.w3schools.com/howto/howto_css_image_overlay.asp
