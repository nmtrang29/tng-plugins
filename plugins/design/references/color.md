# Color

Color theory is fun and all, but this section will take a *very* practical look at color usage as well as do's and don'ts. You won't be mystified by color any longer!

---

## Color Picking Methods

### Why

When you move beyond sketches, wireframes, and default styles in the world of interface design, you're going to start using color.

Color can be overwhelming to choose so I'm going to first breakdown the methods of choosing colors and show you the pros and cons of each method as well as share my methods for color selection.

In this guide we'll lay the foundation for all of our color selecting needs for the future.

### What

1. You will spend a large amount of time with you color picker open and clicking around and adjust things. This will help demystify some of the terms and give you tips on navigating them as quickly as possible

1. HSB is my favorite. There are subtle differences between software color pickers.

1. Get the most comfortable with HSB and HEX. Any of these can be converted into any other formats. So don't fret about final color format.

- RGB (*RGBa)*

- HEX

- HSL

- HSB (*HSV*)

**RGB**

This stands for Red, Green, and Blue. These are the three lights that create color on digital displays. The *a *you will sometimes see associated with RGB (eg. RGBa) refers to the alpha channel of the color. Alpha refers to the *opacity.*

Either three of these colors (RGB) can range from 0 – 255.

**Black**

An RGB value of (0, 0, 0) equals pure black.

**White**

An RGB value of (255, 255, 255) equals pure white.

Remembering and using RGB codes is not very intuitive, so you will often find heavier usage of HSB or HSL in design tools. Look at this image below. Would you ever remember and be able to easily recall and manipulate these three colors? Me neither, that's why I don't use RGB when I'm designing.

![](https://negliadesign.com/wordpress/assets/RGB-color-swatches-R-700x342.jpg)

**HEX**

HEX is short for hexadecimal. This is a 6-digit shorthand color code of the RGB color spectrum. For example black would be represented in the following format. `#000000`

It's not really any less confusing, but I have found this slightly easier to use over RGB. HEX and RBG can be used interchangeably without any changes. There is a conversion formula, but you don't need to know it because all design tools do it for you.

In HEX format, there is a range of 16 possibilities for each of the 6 positions. Each position can range from 0-9 and A-F. 0-9 are the first 10 possibilities whereas A-F are the next 6 possibilities of color amount.

The lowest digit `0` represents no amount of color, and the highest position, `F`, represents the fullest amount of color.

- Positions 1 and 2 determine amount of Red.`#FF0000`

- Positions 3 and 4 determine amount of Green. `#00FF00`

- Positions 5 and 6 determine amount of Blue. `#0000FF`

The color is not affected by lowercase or uppercase. That's merely a personal preference.

**Black**

#000000

RGB(0, 0, 0)

**White**

#FFFFFF

RGB(255, 255, 255)

**HEX shorthand**

HEX codes can be shortened to three digits. In this case each of the 3 digits represent each *pair *of 6 digits. `#000` is shorthand for `#000000`, for black. `#FFF` is shorthand for `#FFFFFF`, for white.

**HSL**

Similar to HSB, **HSL** stands for **Hue**, **Saturation**, and **Lightness**.

- See this example on Figma's color wheel

- Contrast difference with Sketch's

- Walkthrough examples of each.

- Saturation goes diagonally from lower left to upper right

- Lightness goes diagonally from lower right to upper left (depending on Saturation level)

1. HSB vs. HSL – worth noting the difference

1. Figma is a better example for choosing HSL values over Sketch. Can be helpful when adjusting only the L value to finding other colors based on your base color.

1. I still prefer HSB over HSL, but it's worth noting that HSL can be useful in certain situations.

---

The 'L' in **HSL** can vary, depending on the software used. HSL can hence also mean 'Hue, Saturation and Luminance' or 'Hue, Saturation and Lightness'. The exact definition of these may vary with the software—which is why I find this method a little confusing to use in most scenarios.

**HSB**

HSB is my favorite color method to design with. For me, it's the most intuitive.

**H** stands for **Hue**. Hue spans Red, Green, Blue and everything in between. This number will range between Red at `0` and Red at `360`. Think of it as a loop.

**S** stands for **Saturation**. This is a scale of 0–100. Zero being absolutely no saturation and 100 being fully saturated. You can also think of Saturation on the *white *scale. A 50% saturated color, will appear the same as a 100% saturated color with a white shape with 50% opacity on top of it.

**B** stands for **Brightness**. This is also a scale of 0–100. Zero being no brightness (black) and 100 being fully bright. You can think of Brightness on the *black* scale. A 50% brightness scale on a color, will appear the same as a 100% brightness color with a black shape with 50% opacity on top of it.

So for me, **HSB** is as simple as Color, Whiteness, and Blackness. Much easier to remember and use than RGB or HEX by itself.

- Saturation goes left to right

- Brightness goes top to bottom

**Fun Fact**

**CMYK** stand for Cyan, Magenta, Yellow, and Black. These are the four colors that are used in color printers. These are also the four colors that create the *four color print process*. CMYK colors will always print slightly differently than how they appear on the screen, because on the screen even CMYK colors are created with digital lights in the RGB space. So if you ever need to print something, never rely on the color you see on your screen. Print it out and test it that way.

**Resources**

[Link: Color by Cloudflare Design](https://color.cloudflare.design/)
## Color Contrast & Accessibility

> [!NOTE]
> Note the [WCAG does not require contrast scores for disabled items](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html), but it's definitely something you should still pay special attention to when designing your interfaces. See this article, [Disabled Buttons Suck](https://axesslab.com/disabled-buttons-suck/).

#### —**Globally, at least 2.2 billion people have a vision impairment or blindness, of whom at least 1 billion have a vision impairment that could have been prevented or has yet to be addressed.**

#### —**This 1 billion people includes those with moderate or severe distance vision impairment or blindness due to unaddressed refractive error, as well as near vision impairment. The majority of people with vision impairment are over the age of 50 years.**

Reference: [https://www.who.int/en/news-room/fact-sheets/detail/blindness-and-visual-impairment](https://www.who.int/en/news-room/fact-sheets/detail/blindness-and-visual-impairment)

---

We built the Use Contrast Figma plugin AFTER I recorded this guide’s video. This is my favorite way to check color contrast now. Yes, I’m biased. 😉

---

### 👉 [WCAG 2.0](https://www.w3.org/TR/WCAG21/#contrast-minimum)

20/20 vision 3.0 contrast (AA Large)

20/40 vision have 1.5 contrast sensitivity loss, which is where the 4.5 score comes from (AA)

20/80 vision for 7.0 score (AAA) Not able to be corrected with glasses, etc.

#### Scores

- Fail – 1 to 3.0 [https://usecontra.st/333/000](https://usecontra.st/333/000)

- AA Large – 3.0 to 4.5 [https://usecontra.st/666/000](https://usecontra.st/666/000)

- AA – 4.5 to 7.0 [https://usecontra.st/777/000](https://usecontra.st/777/000)

- AAA – 7.0 and higher [https://usecontra.st/999/000](https://usecontra.st/999/000)

**Ways to check your color contrast**

- Use Contrast for Figma (and macOS) [https://usecontrast.com](https://usecontrast.com)

- Use Contrast web [https://usecontra.st/000/ff0](https://usecontra.st/000/ff0)

- Stark [https://getstark.co](https://getstark.co)

- Colorable [https://colorable.jxnblk.com/](https://colorable.jxnblk.com/)

- Leonardo [https://leonardocolor.io](https://leonardocolor.io/?colorKeys=%236fa7ff&base=ffffff&ratios=3%2C4.5&mode=CAM02)

**Gotcha situations**

`refer to video for example`

- bright brand colors for primary calls to action

- placeholder copy for input fields

- legal copy

- deactivated items

**Contrast Sweet Spot**

AA or 4.5 (or higher) is your sweet spot. If all of you text colors are hitting this score, you're going to be very well positioned. Go lower or higher from here with a very calculated approach.

**Titles and Body**

7.0 (or higher) gives you a nice even contrast for titles and body copy for lots of content without going too heavy in contrast.

Staying in the middle ground provides opportunities to go lighter or darker, for notifications, etc. that may need to be more heavily weighted.

**CTAs, Links, Buttons, etc.**

- AA+ or AA works well for these, though it certainly won't hurt to go with higher contrast.

---

Here's a great [article](https://medium.com/tap-to-dismiss/color-within-constraints-d6f777a3b72d) from *Linzi Berry* on building a scalable color system at Lyft

---

Here's another great article from *Stripe* about their new accessible color system
## Structural vs. Interactive Colors

### Why

Understanding the two types of colors and how they work together can help you break your color selection process into chunks, making it more of a systematic process rather than a total guessing game.

Setting a general color direction as early as you can will help keep you focused during your project and allow you to make additional color decisions more quickly and easily.

Often times this can take a day or two of experimentation and sometimes you'll end up tweaking final final hex codes until you're ready to ship it.

### What

`refer to video examples`

**Structural colors**

By, structural colors I'm referring to primarily the background color of your interface, the background color of any particular container or grouping of containers, as well as borders and dividers.

The majority of interfaces tend to have a white or light grey background (the inverse is true for dark mode enabled apps), however there maybe situations that call for a very colorful background.

In most cases, if your structural colors are primarily restrained in saturation (white, light grey, etc.) then your interactive buttons will be highly saturated. This is not the case for interfaces that use a fully desaturated color scheme for both structural and interactive colors—but in this case more care needs to be given to the position and color amount and reversal for interactive elements.

**Interactive colors**

Interactive colors are colors that you define some type of action. They can often have brand recognition associated with them.

### How

`refer to video examples`

**Let primary button color drive your color scheme**

- pick a quite saturated primary color

- check it's contrast score to make sure it works!

**Greyscale or tinted structural colors**

- white, medium grey, and dark colors for structural

- same but tinted warm, cool, etc. depending on primary action color

- try using a consistent hue for a rich color theme

**Things to consider**

- Determine supporting overall color scheme

- Pure white background with shallow Z-axis?

- Light grey background with white modules and subtle shadow? (iOS, Facebook, App Store)

- Completely desaturated foundational colors or slightly saturated?

- Cool color scheme or Warm color scheme

- Shifting colors?

- Heavy color usage?

- See if strong brand color already exists and use that to determine if primary action should be the same

**Avoid Muddy Colors**

Muddiness occurs when the contrast between two objects is too low. This can typically be found with certain color combinations as well as drop shadows on certain items.

#### Links
## Primary, Secondary, & Tertiary

The primary action needs to stand out more than the others. It should pass the squint test. It should be the focal point and unmistakably "the thing to do to perform the action."

There should only ever be one primary action on screen. If it helps you, make a simple ordered list with the most important action as number one.

**Common primary actions**

- Sign Up (basecamp)

- Sign In (google)

- Save (edit profile)

- Post (pinterest)

- Etc.

**Common secondary actions**

- Cancel

- Edit

- Skip

- Filter

- Sort

- Go Back

- Close

`refer to video for examples`

Just because there might only be one action on the screen, doesn't make it a primary action.

Use high contrast or high saturation color levels for primary actions. Avoid thin and dainty primary actions as they simply don't command enough attention.

#### Links
## Strategic Color Definitions

#### Color definitions to consider:

- This color will always be used for navigating back

- This color will always be used for primary actions

- This color will always be used for selected objects

- This color will always be used for secondary actions when a primary action is present

- This color will always be the background

- This color will always be used for borders and dividers

- This color will always be used for icons presenting a status

- This color will always be used for icons and links that are actions

- This color will always be used for "doing something" (action)

- This color will always be used for "going somewhere" (navigation)

- This color will always be used as a background color behind a primary call-to-action
## Color Amount & Modification

The method in this video will serve as a great foundation for your color choosing challenges. Following this simple process will give you superpowers when it comes to adjusting your colors.

Using completely desaturated blacks, grays, and whites isn't necessarily a bad thing, but you will find there are LOTS of subtle colors at play in rich interfaces. Especially in the colors that seem to be simple white, grey, and black.

Different locations in interfaces that can be treated with modified base colors. (Note: Don't assume a variation of an accessible base color will also be accessible. Make sure you test each one before locking it in.)

Some of your earliest decisions to consider will be how much or how little color to use. There is no right or wrong answer. You are the designer, you choose. It's OK to go down a path 10 screens deep and change your mind and tweak the initial color palette.

Super trippy example of how color/motion can completely alter what you think I you’re seeing...

(The shapes in the gif are not actually changing position or size at all, only the color is changing)
## Gradients

Gradients can be used in a number of ways to enhance your designs, because they can be generated with code, and don't come with the same performance hit on load times as images do.

They can be used for adding **visual interest**—jazzing things up or making them pop.

They can be used for **utility**—fading things out or making smooth transitions.

And They can also be used for **interactivity**—creating depth

`refer to video for examples`

**Pro-tips**

For creating visual interest you have a little more leeway for changing your HSB values,

for utility and interactive gradients try to be **very** subtle with your shifts in color. It's really easy to overdo it.

> When in doubt go extremely subtle and use restraint.

### **Homework**

1. Recreate the Sketch icon with shapes and gradients

1. Recreate the old [stripe.com](http://stripe.com) background (screenshot in the file) using the exact colors then create a new version with completely different hues

1. Add a utility gradient to some body of text on one of your old assignments

1. Create a few different buttons that use an analogous gradient and a monochrome gradient for creating very subtle depth.

**Bonus CSS tip for gradients**

It's not currently possible to animate gradients with CSS, but you can fake it by adding the gradient to a pseudo element and then animating the opacity of that element.

You can also kinda fake it by increasing the size of an element with a gradient and then animating background-position.

This will give the effect of animating a gradient on hover. 👍
## Nifty Shades of Grey

Most interface projects you work on are simply going to need multiple shades of grey. Usually around 4 or 5 different shades.

And it's 100% ok to have a range of grey to use, as long as you are very strategic and intentional about them.

Your developers will thank if you've had the foresight to be very specific and purposeful with your color choices and conventions.

**Common example**

1. Dark color for most text. Usually in the #000 to #444 range

1. Medium grey for AA readable text

1. Medium light grey for AA Large text or icon usage

1. Light grey for divider lines or hover backgrounds for certain elements

1. Super light grey for a background color

### **Homework**

Design a simple calculator with three different color schemes.

1. Neutral grey

1. Warm or Cool grey

1. Fully colorful with lighter and darker variants used as "colorful" greys

You decide the HUE, but used limited saturation and brightness for the grey buttons.

*Mac and iOS calculators for reference...*

---

> Thoughts about "grey" vs. "gray"
## White & Almost White

Make your decisions about white and light grey colors based on:

- **information density**
  - the more information the more varied you may need to get with background grey bg colors, lighter modules, and dividers

  - the less information, the more you can use negative space as the primary mechanism for content separation without the need for too many module backgrounds or dividers

- **design direction**
  - do want to have a "floating tile" look for you interface with drop shadows and does that make sense for what you're working on?

  - do you prefer a flatter interface with no shadows

  - style preference and general direction will play a big role in deciding this

**Biggest takeaways**

- Pay *special* attention with how you use the color white, specifically with structural colors.

- All white backgrounds with light grey modules can be a very clean and modern look, but it's tricky to hit just the right amount of grey without being too dark. You'll need to do lots of tests and variations.

- For more complex interfaces it can be easier to separate the content from the background with white modules on top of a light grey background. Alternatively you can achieve a similar effect with using big drop shadows on your modules.

- With less complicated data and interfaces you can use less borders, background, and module dividers.

**Z-index tips and tricks**

- If you're using light structural colors in your interface, white will pop forward to the foreground (higher on the z-index or z-axis)

- Darker grey colors will appear slightly sunk-in.

**Ways to modify light structural colors**

(*applies to dark UIs too, it's just 2x tricker and more important when going dark*)

- Background color shift

- Border color shift

- Shadow shift

- Combination border/shadow shift
## Secrets of Dark UI

---

Below is the full redesign at 1x speed. Long video, but packed with lots of on the spot decision making process. Talking through every selection and every choice.

---
