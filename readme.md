<h1 align="center">TUSG</h1>
<p align="center">The Ultimate SCSS Grid</p>

Creates global grid utility classes to be used in your project.

- 2kb gzipped (with default settings) 📦
- fully customizable ⚙️
- responsive ✨

Inititation:
```scss
// global.scss
@import "~tusg/grid.scss";

// tusg-config:
// [size-name] [breakpoint] [gutter-width]
$tusg-config: (
  xl 1240px 40px,
  lg 1024px 32px.
  md 768px 24px,
  sm 480px 16px
);

@include tusg($tusg-config, 12, "all"); // initiate with breakpoints and 12 columns
```

Basic usage:
```html
<div class="grid">
  <div class="grid__item 
    grid__col-6/12
    grid__lg-col-8/12
    grid__md-col-12/12
  "></div>
  <div class="grid__item 
    grid__col-6/12
    grid__lg-col-4/12
    grid__md-col-12/12
  "></div>
</div>
```

Grids within grids:
```html
<div class="grid">
  <div class="grid__item 
    grid__col-6/12
  ">
    This container is 6 columns on the main grid.

    <div class="grid">
      <div class="grid__item grid__col-4/6">
        This container is 4 columns on the main grid.
      </div>
    </div>
  </div>
</div>
```