# Responsive CSS

Responsive CSS is a way to style websites so they'll render optimally on any device no matter the screen size.

## Objectives

- Discern the difference between fluid and responsive design
- Know how to make CSS responsive
- What is mobile first

## Fluid design

In fluid design a page is styled using using a fluid grid. A fluid grid uses percentages rather than fixed pixel widths or other units. As the browser window grows and shrinks the design changes to fit the window area.

## Responsive design

At a certain point fluid designs begin to break down and look bad. They may squish to fill the available screen space but the content gets too mashed together and a whole new layout is required.

To remedy this situation we have a new feature in CSS3 called Media Queries. Media Queries allow you to ask the browser how much viewable space it has vertically and horizontally and apply special styles to it based on those measurements.

### Example

An example of this is easy. Load just about any website in a browser. Then change the browser window size to the point where its really small. Then pull out your phone and visit that same site on your phone. You'll notice the changes and differences. That's responsive web design. Most sites do it right. Hopefully you don't choose some weird site that's doing it wrong.

Responsive CSS with media queries is available in CSS3 but the great news is that it is __very__ widely supported and you should have no need to worry about browser support for media queries.

## Media Queries

Media queries are CSS code you load *last* in your CSS files. They can target a type of screen, device, or even paper (for printing) and they can also target mininum and maximum screen sizes (at the same time). Here's an example:

```css
@media only screen and (max-width: 1023px) {

  body {
    font-size: 0.8em;
    line-height: 1.5em;
  }

}

@media handheld, only screen and (max-device-width: 450px) {
  .mobile-show { display: inline-block; }

  // Grid styling
  body, .container, .row, .row-loose {
    font-size: 1.1rem;
    width: 100%;
    min-width: 0;
    margin-left: 0;
    margin-right: 0;
    padding-left: 0;
    padding-right: 0;
  }

  .col-1,
  .col-1,
  .col-3,
  .col-4,
  .col-5,
  .col-6,
  .col-7,
  .col-8,
  .col-9,
  .col-10,
  .col-11,
  .col-12 {
    width: 100%;
  }
}
```

In the above example we're  making the font size and line height slightly smaller for when browser windows are less than the desired 1140px (which is what the grid this code came from specified). Then we target handheld devices only (like phones and tablets) and set the entire grid so everything stacks on top of each other. This is deal for mobile devices. We could get more specific and target as many devices as we wanted to but in this case we just target "screens slightly smaller than our ideal" and "any mobile device screen".

## Mobile First

Mobile first is the idea that you design for mobile devices first, creating a design meant for small screens, then expand your design physically from there.

There are [others who](http://www.html5rocks.com/en/mobile/responsivedesign/) can [explain it better than me](https://abookapart.com/products/mobile-first).

## Activity / Lab / Practice

Make your personal profile page (your GitHub pages page) responsive! This isn't homework, it's practice.
