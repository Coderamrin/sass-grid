# **SASS Grid**

## Simple responsive grid with Sass mixin.

## **What**

Sass grid is a responsive 12 column grid. built with sass mixin.

## **How to use it**

1. Downlad the \_grid.scss file from this repo.
2. copy it over to your project
3. import it to your main.scss file.
4. Now all use it.

## **Example**

```scss
div {
  @include @container;

  .div-child-1 {
    @include @column (6, medium);
  }

  .div-child-2 {
    @include @column (6, medium);
  }
}
```

## **How this works?**

If you've used bootstrap grid or anyother grid system.
You know that you need to add .container class to the parent then the row then to the child you add the columns with the media quearies.

So, what we are doing here is we are adding the **container** mixin to the parent. Then the **column** mixin to the child elements.

Note: the column takes 2 parameter first one is the column $size the second one is the breakpoint.

```scss
@mixin column($size, $breakpoint: medium) {
  @include breakpoint-up($breakpoint) {
    box-sizing: border-box;
    flex-grow: 0;
    width: ($size * 100% / $grid-columns);
  }
}
```
