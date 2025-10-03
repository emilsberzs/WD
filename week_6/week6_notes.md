## Layout for differetnt devices-Practical CSS
```
<style>
tag,other tag{
    property: value;
}
.class{} (not unique)
#id{} (unique within document)

color:name or #FFFFFF or rgba(255, 255, 255, 1)

</style>
```

```
<link rel="stylesheet" href="./style.css">
```

### CSS grids

```
.container{
    display:grid;
    grid-template-columns: 1fr 1fr 1fr 1fr; (fr stands for fraction)
    or
    grid-template-columns: repeat(4, 1fr);

    grid-auto-rows: minmax(500px, auto);
}

.top-right{
    grid-column-start:3;
    grid-column-end: 4;
    grid-row-start: 1;
    grid-row-end:2;

}
```

```
<div class='container'>
    <div>1</div>
    <div class='top-right'>2</div>
    <div>3</div>
    <div>4</div>
</div>
```

### Responsive CSS
- Specify logical conditions for CSS depending on device properties (mainly depending on display size)

```
CSS
@media only screen and(min-width:768) {
    Apply this CSS only when displayed on screen no smaller than 768px in width
}
```

```
HTML
<meta name='viewport' content="width=device-width, initial-scale=1"/>
```

### CSS Frameworks

- Pre-prepared styles to speed up development of website, usually includes:
    - Typography
    - Buttons
    - Forms
    - Navigation menus
    - Grid systems
- With modern CSS, some of these framework features comes included

- TailwindCSS:
    >Utility-first CSS framework packed with classes like flex, pt-4, text-center and rotate-90 that can be composed to build any design directly in HTML
    - Default Tailwind strips all built in standart CSS from tags
    - Also comes with various components, templates and widgets (best ones are paid)

- Foundation:
    - Doesn't strip defaults
    - Comes with components, forms and widgets and stuff
    - Loads of free templates

- Bootstrap:
    - OG framework
    - Same, loads of templates, forms and widgets
    - Wide variety of options as mature framewoek
    - Has themes