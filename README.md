
# ScssBreakpoints

This is my got to mediaquery mix-in for SCSS.
This was built over the past few months from bits and pieces I found on-line and lot's and lot's of testing.

## Requirements 

1. understand SCSS
2. understand MediaQueries
3. have a working scss flow where you can plug this in.

## References

The original Mixin code and artice explaining why and how it works can be found here:

[https://css-tricks.com/snippets/sass/mixin-manage-breakpoints/](# ScssBreakpoints

This is my got to mediaquery mix-in for SCSS.
This was built over the past few months from bits and pieces I found on-line and lot's and lot's of testing.

## Requirements 

1. Understand SCSS
2. Understand MediaQueries
3. Have a working SCSS flow where you can plug this in.

## What you need to know
**This is a mobile first mixin**
Download the _breakpoint.scss file into your working directory (I kept it self-contained on purpose).
In your main 'SCSS' file, import it before importing other files.

### How to use it in a nutshell

Once the file is imported, you can use it by invoking the mixin passing in the breakpoint you wish to use as the example shows:

```scss
h1.title{
  &::after{
    content:'NOT IPHONE 7 PLUS';
    color:orangered;
    background:palegoldenrod;
    padding:5px;
  }
  @include respond-to('iphone7+') {
   &::after{
     content:'IPHONE7 Plus';
     color:orangered;
     background:palegoldenrod;
     padding:5px;
   }
  }
}
```

```html
<!-- ... -->
<h1 class="title">TITLE -</h1>
<!-- ... -->
```

With the following example, if you open this html on anything but an i-phone7Plus,  you will get something like

**TITLE - NOT IPHONE 7 PLUS**

and if you open it on an iPhone7+:

**TITLE - IPHONE7 Plus**

## THE LIST OF BREAKPOINTS
Below is a complete list of breakpoints available at the moment:

### Device Specific Breakpoints
These can come in handy when you have a very specific problem with a device - they should not be you *GO TO* solution.

- appleWatch
- motoWatch
- iphone4
- iphone4port
- iphone4land
- iphone5
- iphone5port
- iphone5land
- iphone7
- iphone7port
- iphone7land
- iphone7+
- iphone7+port
- iphone7+land
- iphonex
- iphonexport
- iphonexland
- ipad1
- ipad1port
- ipad1land
- ipad3
- ipad3port
- ipad3land
- ipadpro
- ipadproport
- ipadproland
- ipadpro12
- ipadpro12port
- ipadpro12land
- laptop
- retina

<sub><sup>I'll be posting descriptions shortly</sup></sub>

### Less specific breakpoints
Here are some breakpoints that I commonly have come across depending on my layouts and specific clients.

- tiny - Small cellphones
- small - Standard cellphone
- medium - Tablets
- large - Laptops
- xlarge - Retinas/Desktops
- xlargeh - Very large displays like TVs
- 1366x768 - Very common resolution in clients
- landscape - Landscape viewport
- portrait - Portrait viewport

<sub><sup>I'll be posting descriptions shortly</sup></sub>

## References

The original Mixin code and artice explaining why and how it works can be found here:
[Mixin to Manage Breakpoints](https://css-tricks.com/snippets/sass/mixin-manage-breakpoints/) - article by [Hugo Giraudel](https://css-tricks.com/author/hugogiraudel/)

Most of my very specific breakpoints are taken from the article [Media Queries for Standard Devices](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/)
