# Layout

Layout covers the critical compositional aspect of interface design. These handy lessons will create an immutable personal framework for all of your future projects.

---

## The Box Model

> [!NOTE]
> Auto Layout wasn’t yet a a feature in Figma when I originally recorded this guide. Please feel free to use Auto Layout when you’re working through this homework assignment!

### Why

From this point forward, I want you to see every piece of interface as a box—with a left and right edge and a top and bottom edge. Every single thing.

Every string of text, every folder that contains multiple elements, every image—round or not. Consider every single piece of interface as a block.

Why do I want you to do this? Because it will make your life as a designer about 1,000,000 times easier.

This is really non-negotiable. From now on, everything... and I mean everything...

...is a box.

### What

The term box-model comes from HTML...

It consists of 4 main properties...

- content

- padding

- border

- margin

### How

In a lot of minimally designed websites and apps, there aren't many borders. I'm not opposed to that by any means, but if you did enable borders on all elements you would be able to see the bounds of every single element on the web page.

In fact, many developers trouble shooting CSS issues have a `.debug` class or something similar that puts adds `border: 1px solid red` to any object. I've done this many times myself.

Applying this box-model thinking to every possible element you design will give you a much better process for creating clean and structured layouts.

Margin refers to how far away an object is from another objects or screen edge. Whereas, padding is built-in spacing inside the actual box.

In the above example your content is 24px from the edge, but what's really going on behind the scenes is a very calculated amount of margin, plus padding to total the full amount.

This can and will be done whether the margin and padding is visible or not.

In general if you DO have a visible content background that is different than your main background, you'd want the margin and padding to be roughly equal to each other.

However if you know for a fact that you will have no difference at all with your background color and content background color, then you could theoretically go with a 0px margin and a 24px padding to achieve the same look.
## Grids & Containers

### Why

"The Grid" is firmly rooted in early graphic design. While studying graphic design in college, one of the first things we did in our layout classes was establish a grid. Then we would make "thumbnails" or small sketches of our would-be layout at tiny sizes to see if anything interesting popped up.

Grids are important because they create boundaries. They create structure. They serve as a foundation to base everything from.

They exist because the idea of a grid, creates a source of truth—rigid and immovable.

- Creates clarity and consistency

- Improves design comprehension

- Helps with responsive design

- Speeds up the design process

- Makes the design easier to modify and reuse

- Easier to systematize and facilitate collaboration

### What

Although the idea of using a grid implies a fixed and firm X or Y coordinate along with a fixed pixel count for height and width...

In the context of interfaces, that is just not the case.

In interface design, grids are stretchy and malleable. They serve as a dynamic structure that contains interface elements.

This brings us to **containers. **Containers are the Grid’s children. They are the fixed constraints of any particular interface element or group of elements, or both.

Think of a frame or an artboard as a container. Think of any layer in your design document as a tiny container of that specific object. And especially think of any group of elements as a container.

Take the title bar of an app for example. You commonly have a large container for the following elements, which are in fact 5 smaller containers:

- Status bar (contains its own child elements—time, service, battery, etc.)

- Left action (sometimes a container for multiple things)

- Title (sometimes a container for multiple things)

- Right action (sometimes a container for multiple things)

- Background (sometimes a container for multiple things)

For a marketing website you might have the following containers

- Header (logo, navigation, action buttons)

- Hero Section (Title, Subtitle, CTA, Background, Hero Image)

- Additional Content

### How

I like to use the "content-out" approach for designing. Rather than come up with some random grid and force everything to fit in that grid...

I design the contents of one container first and assume it to be "stretchy" or 100% width. Which is another reason why designing for mobile first can make your life easier. If you're doing this, you have an automatic cutoff for the width—375px for an iPhone X, etc.

You can also have padding built into your container that keeps your designs any number of pixels from the edge—4, 8, 16, 20, 24, etc. are all common "edge" margins.

So let's say I'm designing a small list of people with avatars, name, subtext, and an icon on a mobile screen, and I want the content to have some nice negative space around it...

I'll create a container with those elements and "bake in" the necessary padding. So if I use 375 as my full-width, with 20px of margin on each side I'm going to have the content of my container touching each edge of 335px.

`see video for examples`

At this point, I'm relatively unaware of the exact grid I'm using. The container and the way the content looks inside the container is driving my decision behind what amount of padding I should use, and ultimately dictates the grid I'm adhering to.

There is no actual rigid grid that interfaces click into magically. Anything that happens is all programmed individually based on components, parent components, etc.

This goes against the idea of something like Bootstrap as a web scaffolding, which has predefined numbers and percentages for column widths, etc. These are often used for quick start projects with a decent-enough looking layout to get by with early on.

### Key Takeaways

- Grids are important, use them.

- Remember, a screen itself is its own 1x1 grid. Divide it in half and its a 4x4 grid, etc.

- Don't expect a grid to do all of your designing for you.

- Start with a easy to use 12 column grid and adjust as necessary.

- The grid is a tool to serve the higher purpose of intentional alignment.

- Grids can be fully stretchy or have fixed constraints.
## Implicit Grid

### Why

The implicit grid is an implied grid. It's like a soft grid. This is a very practical way to use the good aspects of a grid in a "don't tell me what to do" kind of way.

Using an implicit grid—and following it closely—will give your designs that "clean" feel. Your spacing will be on point. Careful consideration will be giving to every single increment on the page.

Used correctly, the implicit grid will become a lens you look through when observing a design.

Using an implicit grid will establish a nice and balance design rhythm without forcefully locking you into some arbitrary explicit grid.

### What

The implicit grid is the systematic negative space between all interface elements. That's all. The negative space.

Traditional grids are explicit and very helpful. I use implicit grids because unlike traditional layouts with a fixed size of paper, we have dynamic widths for browser windows and device sizes. This creates the need for width percentages, which creates dynamic numbers (with a maximum if desired). It's also unlikely to have fixed vertical spacing due to the nature of dynamic content created by users—text length, image widths, and so much more. **Think of grids more as "flexible containers" that will likely need to be 100% wide at small sizes, then have a constraint introduced to them as they get larger.**

Start with the idea of an explicit grid, but make sure that it works implicitly when you realize the grid will break. Breakpoints.

- Explicit grids define a set amount of horizontal and vertical space

- Use explicit grids in a general sense, not letter of the law

- Implicit grids are *implied* and not plainly expressed with huge horizontal or vertical lines

- I use implicit grids **heavily** in my designs

I recommend increments of 4px as a good starting point (4, 8, 12, 16, 20, 24, 28, 32, 36, 40, etc.) Stick to this and be very diligent to stay consistent. This will help your designs IMMENSELY. There's also not hard and fast rule that says you can't break this rule by knowingly using "half an increment" to increase or decrease by 2px.

There are a number of designers who love an 8px grid and relying heavily on multiples of 8 for any and all spacing. There's absolutely nothing wrong with that.

My personal preference is the 4px implicit grid. This is how I *see* all of my designs in the beginning, while refactoring and editing, and also when creating final~ design system components.

Why not 5 or 10? Well, no one's gonna stop you from doing that, but even numbers have far more flexibly because of their ability to be divided in half.

There is a measurement in typography called the `em`. This is the width of the letter `m` in any given typeface. This is also where the term `emdash` and `endash` come from. `Endash` being a dash that is the width of the letter `n`, where as an `emdash` is the width of the letter `m`.

So on the web, 1em is a unit of measurement based on the *base* type size determined by a browser. This base unit of measurement, as decided by default HTML, is 16px. So in web terminology, specifically CSS, 1em equals 16px.

With CSS you can change the value of 1em by changing the default font size. It's as simple as declaring:

```Scss
html {
	font-size: 16px // this equals 1em by default (you could change this to 18px and all instances of "em" would be affected)
}

h1 {
	font-size: 1.5em // this would equal 24px (16*1.5)
}

h2 {
	font-size: .25em // this would equal 4px (16*.25)
}

```

All this to say that 16px and 1em is a pretty standard digital measurement that has deep roots in typography.

Ok, so that's my big soapbox speech about using 4px as an implicit grid number.

How does that apply to my interface designs?

One of the first instances of an implicit grid that will need a decision is your page's padding. This might not be visible at large sizes when a large web page's layout has a max-width of 1280 and the screen-width is 1440, but it will become very apparent as the browser window transforms to an equal width as the content.

A good starting place would be 16px and then you can adjust down to 8-4px or up to 20-24px.

In most cases you'll need to experiment with a few different options before moving forward. Plus you can always go back and adjust this later as you design more screens.

Often times, you will make a decision for say a 24px margin and then later have a new screen that works **really** well with a tighter 16px margin. You then have a decision to make, should you go with a standard 16px margin for every screen, or is the design and context different enough to warrant a difference of 8px.

A difference of 8px, seriously? Yes, I'm absolute serious. Even a 4px difference can greatly impact the tiny details of a design. This is, after all, where the devil lives. 😈

We built the Use Contrast Figma plugin AFTER I recorded this guide’s video. This is my favorite way to check color contrast now. Yes, I’m biased. 😉

### How

First of all make a decision about your implicit grid. And don't let the idea of an implicit grid overwhelm you. This simply means the negative space (margin and padding) between and around all elements will equal multiples of 4.

**Examples in spacing**

Make sure you have definitions for *every increment of space* in your design.

1. logo or icon from borders

1. spacing around icons in its container and from another icon

1. in between navigation elements

1. in between line items or cards

1. in between a title and its body

1. in between a title and its underline and its body copy

1. an avatar and its label

1. an avatar from the edge

1. from the bottom of the content to the bottom of the page

1. in between two related sections

1. in between two un-related sections

1. an arrow from the edge of the screen

**Spacing in the gaps**

- relational spacing definitions—0px, 4px, 8px, 16px, 24px

- all spacing should have meaning and value assigned to it

- margin and padding have *meaning*

**Element Relationships**

Define how closely elements are related with the distance that separates them.
## Negative Space

### Why

You will die without oxygen. It is required for life.

Negative space is design oxygen. Your designs will die without it.

Negative space let's things breathe.

It's often the most overlooked aspect in design.

Think about airline seats...

- Volume is luxury

- Space is premium

One of the most critical skills to develop nice and clean, well-balanced layouts.

You need to become a **master **of negative space.

If we remember that "everything is a box" when it comes to UI. Every box needs its own breathing room. We don't want to create tiny coffins for all of our elements to live in. Negative space is design oxygen that allows design elements breathe and thrive!

In design school, we would joke about a blank piece of paper graded "F" for not enough white space.

### What & How

Think of white space as the equivalent of actual space in architecture. There are specific guidelines for how wide a doorway to a bedroom should be, or how far away a kitchen island needs to be from a corner cabinet.

"OFF" negative space can really hurt a layout and make it feel unbalanced.

When you find yourself struggling with a certain piece of interface, it's likely you don't have sufficient negative space.

**Rule of thumb for width and height padding for small UI elements:**

Find a good side margin/padding distance by multiplying the top and bottom values by a minimum of 1.5 and up.

So a button with 8px of padding on the top and bottom would look nice with 12, 16, or 24px of padding on the sides.

In interface design, there is way more leeway for creative vertical negative space on screens than horizontal negative space. Screens and browser windows only grow so wide, but scrolling is a universal screen experience.

Below is another great example of this principal front and center of the current [https://developer.apple.com/design/](https://developer.apple.com/design/) page.

You can argue that swiping left to right is universal as well and you would be correct to a certain extent, but not for large amount of content. Swiping works well for chunks, but only for 3 to 5 swipes. Anything more than that becomes labor intensive.

Another way to think about the dominance of vertical space over horizontal is to think about Facebook, Instagram, Twitter, Pinterest, etc. How do you browse the content on those sites or apps? You scroll and scroll and scroll and scroll.

The terms *white space* and *negative space* are synonymous. They mean the same thing.

**Define Your Negative Space**

For example...

- 16px will be the minimum side margin

- Line items will have 8px of vertical margin

- Buttons will have 4px of top and bottom margin

- Siblings will have 8px of margin

- *Cousins* will have 16px of margin (I’m only using the terms “cousins” loosely to explain something loosely related)

I don't often think of the Sibling/Cousin metaphor when designing, but it serves as a helpful teaching tool to more succinctly say closely related vs. semi-related... =)

You can **define** what 8px of negative space means vs. 24px of negative space.

Fibrestream Billing Dashboard
## Optical vs. Mathematical Alignment

### Why & What

There's a big difference between mathematically aligning objects and optically aligning them.

- One quick example in UI design is the play button icon inside of a circle.

- Typography example of square letterforms vs. rounded letterforms

`refer to video for visual examples`

Think of mathematical alignment as the **Science** behind the design.

Think of optical alignment as the **Art** behind the design.

### How

1. Use math as a primary alignment method. Use optical as a secondary method.

1. Use what feels right for your context. Mathematical, grid-based layout is hard to beat, but often times you need to do what feels like the right balance—build and your design gut by looking at kerning.

**Kerning exercise**

- [https://type.method.ac/](https://type.method.ac/)

📝 **Great article on optical alignment vs. mathematical alignment**

[Link: When it comes to design, your eyes are way better than maths](https://uxdesign.cc/when-it-comes-to-design-your-eyes-maths-aae720fb8222?gi=c4368f8c3394)

**Dealing with abnormal shapes**

Optical alignment is superior to mathematical alignment when it comes to abnormal shapes like icons.

You will use mathematical alignment more often than optical alignment in your day to day design process with standard UI components, but will need to constantly be aware of optical issues.

Do what *feels* right.

### **Homework**

Create two designs for the assigment.

1. **Design some thumbnail options for a video.**
  Pick a really nice image from Unsplash (the [Figma plugin works great](https://www.figma.com/c/plugin/738454987945972471/Unsplash))

  Try the following variations

  - Triangular play button icon inside a circle icon, centered over the image

  - Try the same icon with a stroke circle bg and a solid color bg

  - Make sure to optically align the arrow slightly to the right so it **feels** centered

  Try a few more variations

  - Round the edges of the thumbnail by 4-12px. Experiment with different increments

  - Try aligning the play button to the lower left or the lower right.

  Combine the thumbnail with a title and a small paragraph

  - Try a two-column layout with the thumbnail on one side and the title and paragraph lockup on the other side

  - Try giving the entire thumbnail/title/paragraph layout a background container

  **Pay attention to this**

  Pay special attention to how you're aligning the play icon inside the thumbnail. And also pay close attention to the format you choose for aligning the thumbnail to the title and paragraph. You may need to resize and adjust your thumbnail to get it to fit the same vertical space as your text. Keep experimenting until it *feels *right.

**2. Design a version of the expand/collapse module similar to the Figma file above.**

Decide on where to align the arrows, the checkboxes, and the button edge based on the style of elements you choose.
## Alignment

### Why

The trifecta of beautiful design is good type, good negative space, and good alignment.

"I've got everything all lined up."

"Ok, children line up at the door."

"Look at this line up tonight!"

Lining things up has a quality for creating order, balance, and efficiency for many aspects of life.

In interface design, the constant search for the alignment and definition of things will result in the tightest, cleanest, and nicest UIs in existence.

### What & How

Using proper alignment, with good type sizes, and healthy negative space will take you very very far. Don't underestimate these fundamentals!

If you're consistently thinking about a grid-like structure while designing, this should become a very natural process for you.

Look for opportunities to line things up...

**Aligning for Usability**

- Scan-ability of objects, lists, etc.

- Line of continuation at play (gestalt principles)

- If you can align something, do it. More alignment is better than less alignment—unless you have a very specific reason for not aligning something.
## High & Low Density

### What

Density refers to the "tightness" or "airiness" of a design. Think compact vs. roomy.

High density equals heavy, compact, and tight.

Low density equals light, roomy, and loose.

A spreadsheet has very high density by default.

A calculator app has very low density by default.

The density is determined in large part by the complexity of the interface features. Squeezing more interface into a single screen, means less usage of negative space.

On a spreadsheet there are multiple actions per cell and even multiple edit modes of each cell. Therefore the density is very high. Tolerances are very tight.

On a calculator app, there is very limited functionality. You have the freedom to be more liberal with your pixels. Not carefree and uncalculated, but rather more generous with the quantity.

Low density simply means more generous with negative space. More generous padding and margin sizes. 24, 32, 40px margins versus the high density 4 and 8px margins.

### Why

High density interfaces are more complex and complicated. Sometimes it is necessary (think of any creative desktop applications like After Effects, or even your design tool. Those are relatively high density to accommodate so many features.

But more often than not high density is too complicated.

It's best to shoot for medium or low density interfaces unless you have a very good reason not to.

### How

Determine the density your project needs by considering the complexity of features. As a general rule, the more complex your project, the denser your pixel usage will be.

A highly complex project might require tighter tolerances of only 4 and 8px margins to account for such a high number of features and or content.

In high density interfaces, look for opportunities to offset the interface elements with generous white space. Tight spacing in one area maybe necessary, while generous negative space can be given to other areas.
## Scale, Weight, & Hierarchy

### Why

The visually heaviest elements on the screen are often going to command attention first.

Making something the biggest on the screen is one way to command attention, but that doesn't mean that you can put a giant button on the screen that says BUY NOW. It will certainly command attention, but it's very unlikely someone will click and pay money for something they can't even see.

Think of scale as the volume at which you're speaking, or even as music notes. Masterful speakers and storytellers use volume to OVER EMPHASIZE something, and then gentle whispers and silence to deliver a special kind of emphasis.

`refer to video for examples`

### What

In the history of the internet there's been a sort of meme that's emerged about typeface, scale, and hierarchy. Here's my rendition:

### How

There is not a 100% exact science for properly creating scale and hierarchy in your designs as it is always context dependent.

Let's take a look at how we can use scale for a dashboard design. This screen is specifically for the billing section of a Toronto-based internet provider.

Note the large headline below surrounded by lots of white space. As large as the type is, it comes in second place, in terms of pure visual weight. This is intentional.

Having an outstanding balance in the billing section can be a problem for this business, so they want to accentuate that section so a user is not going to miss it. That doesn't mean it needs to be obnoxiously large and compete with the headline.

It just means there needs to be something helps it stand out more. An easy way to accomplish this is by reversing the color of the background. By having a large block of dark bg it naturally pulls more focus. And since our primary button style is orange, it will work on the black bg as well as the white bg and doesn't feel out of place.

1. We want to use weight and focal points to draw attention to specific areas of an interface. Sometimes it's subtle, sometimes it's loud. Design accordingly.

1. Ways to add visual weight and focal points

1. Always remember the** context** you're designing for and the "conversation" you're trying to have with the user.

**Ways to add weight for stronger focal points **

- Interruption of color (background color, etc. even dark vs. white)

- Type size style

- More negative space

- Z-axis (shadows)

- Borders

- color

- size

- space

- visual interruption of any kind

Focal points should be the largest indication of next desired action—can be "look at this and read..." or "sign up for this thing" or "click this button" depends on context.

Think whether someone needs to take immediate action or if they are in a dashboard of sorts with many different options. Singular strong weight or evenly weighted objects...

**Focal points can and should evolve with the experience**

- there can be evolving focal points based on interaction

- put the users' attention where you want it with clear hierarchy and focal points

Example of weight without much scale change: [https://www.nytimes.com/2019/09/06/sports/tennis/us-open-hugs.html](https://www.nytimes.com/2019/09/06/sports/tennis/us-open-hugs.html)  Note the "create a free account or log in to access more of the Times" module.
## Affordance

### Why

Generally speaking, interfaces exist for people to use and do things with. Use and do are both actions.

Affordance in a design setting, is the key indicator as to whether something is actionable or not. If this is unknown or at the very least undiscoverable, then your interface will be useless.

Perceived affordance—we need to focus on whether the user perceives that some action is possible or not possible.

### What

The notion of an 'affordance' was conceived by James J. Gibson (1977; 1979), a prominent perceptual psychologist, who originally used the term to describe "...the actionable properties between the world and an actor [user]"

Affordances are signals that action can be taken.

**General examples**

- Mouse cursor affordance example: [https://codepen.io/chriscoyier/full/uCwfB](https://codepen.io/chriscoyier/full/uCwfB)

- Hyperlinks

- Button shapes

- Action-oriented button copy (Click here)
## Interactive Layouts

Don't forget that layouts on digital interfaces are not static. They're dynamic! You can bend them, pull them, push them, and more.
## Layout Connectors

This is a supplemental lesson on the topic of alignment, grids, and containers. It's one of those things I see missing in a LOT of designs and it's so so important to make everything look nice.
