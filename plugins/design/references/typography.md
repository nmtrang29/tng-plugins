# Typography

Typography is the cornerstone of user interface design. This section is an extensive deep dive into the world of exquisite type usage. Simple, thorough and practical.

More resources

    [Details of UI Typography from Apple](https://developer.apple.com/videos/play/wwdc2020/10175/) →

---

## Font Size

### Why

Sloppy and inconsistent usage of font sizes, weights, and colors is a telltale sign of someone who doesn't quite know what they are doing with typography. I'm not talking about the old vintage signage you might find that uses 8 different typefaces and just so happens to look amazing. I'm talking about interface design, where there needs to be a reliable and consistent system for a user to learn and understand.

My *Rule of Four*, as it relates to typography, is a rule not a commandment. And like all design "rules," it can be broken, once you're aware of it's boundaries and why those boundaries exist.

This rule will help you remember some basic ingredients of typography for interface design. It's not exhaustive by any means, but a *good rule of thumb* to start with— not the letter of the law.

### What

> **Limit yourself to a maximum of FOUR type sizes only.**

You might even realize that 1 or 2 type sizes looks best. In fact, that is totally encouraged!

As a general rule, get your 3-4 type sizes down and use those exclusively as your starting point. Adjust these sizes at a global level, not an individual level.

Variations of one font size:

- ALL CAPS

- **Bold Headlines**

- Regular text

- *Emphasized*

Can you break this rule? Yes. Can you use less than four type sizes? Yes.

Starting out can be difficult, so use this as a launch pad.

Take a look at the Instagram app for example. On the home screen, 90% of all interface copy is set at 15pt, whereas only the* lesser important* Story section, showcases smaller copy

Let's look at the examples in this document to get a quick glimpse at this Fantastic Four rule of thumb at work.

Again, this is **by no means** **exhaustive**, but it is a very good starting point.

Look at nearly every interface that you believe to be well designed. It's very likely you'll be able to find some combination of consistent Title, Subtitle, Action, and Metadata type sizes.

#### Common Occurences

1. Titles

1. Subtitles

1. Actions

1. Metadata

These are the four most common areas, in which you will find varying degrees of type sizes.

[https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/typography/](https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/typography/)

For example, as of iOS 13 the type sizes would be as follows:

- Titles & Actions = **17pt**

- Subtitles & Body Copy = **15pt**

- Secondary Actions = **13pt**

- Metadata = **11pt**

On nearly every single Apple-designed interface screen, you can find some combination of these sizes. Within the latest iOS updates, you can find some titles temporarily set to 34pt, doubling the traditional size of 17pt, but only temporarily. Once it scrolls out of position the trusty 17pt titles reveals itself.

This is another important thing to note. Every interface is always based on some moment in time and can therefore change accordingly.

If you find yourself using way more than four sizes and having a hard time making things work, you may want to reconsider your type size choices.

#### Extending the Rule of Four

It's important to note that this Rule of Four can easily be extended by changing other aspects of the type. Each of these changes, can effectively change the meaning of that particular piece of interface.

**Color**

One way to distinguish a Title from a Subtitle could be to make the Title text completely black with #000, vs. a Subtitle of the exact same size and weight, with the color of #767676. Or perhaps to indicate action, text of the exact same size and color uses a blue #0066FF.

**Weight**

Similar to color, varying weights can give different interactive definitions to the text used in the design. In Instagrams example, they are using an incredibly subtle font weight change to indicate actionable **profile names**. Whereas profile @mentions along with #hashtags are treated with color instead of weight, because they are created by user input, as opposed to the Instagram design system.

**Position**

Simply changing the position of text can affect its meaning used in the context of an interface. Take for example, the right aligned text of set value inside of the Settings panel inside of iOS.

**Decoration **

Keeping any number of your four type sizes the same, but adding an underline, or a background color, is an easy way to stay within the Rule of Four sizes ballpark, but perhaps your action items deserve their very own size altogether.

**Case**

Changing between different text cases can impact the look and the perceived functionality of what you're designing.

- Lowercase

- Uppercase

- Title Case

- Sentence case

**Lowercase**

It's almost never a good idea to use **only** lowercase unless you've got a very strong reason to do so, whether it's a branding thing or anything else. But remember we're talking "rules of thumb" here not letter of the law.

**UPPERCASE**

UPPERCASE can be a very nice way to provide an interesting variety in your typography mix. Keep in mind that UPPER CASE LETTERS will appear to be a font size larger than your otherwise, Sentence-cased friends. UPPER CASE** **might be used for smaller titles on lists of things, or maybe even primary action buttons. The choice is yours, but don't forgot about this very handy weapon in your typography toolkit.

**Title Case**

Title Case is great for titles. Make sense, right? So keep that in mind for your titles, but you may also experiment Title Case on your buttons or actions as well. It's a subtle, yet handy differentiator when it comes to handling typography.

**Sentence case**

Just like it says, Sentence case capitalizes the first letter of the first word in your string of text. Sentence case is best use for sentences when a complete thought is expressed. You could make a case for using Sentence case in other areas, but you better have a really good reason for doing so.

#### What About Larger Websites?

I like to view the Rule of 4 as applying to a mobile screen or a main section of a larger website. You can imagine that larger websites naturally have different layouts in different sections. For example:

1. The hero area of a marketing website

1. The left/right sidebar of a desktop app

1. Any other specific section the deals with specific information

These areas could easily break past the "4 font size" guideline, but that's OK as long as you're being really intentional with those choices. Look for areas where different sections can have overlapping font sizes.  For example, if one section on a larger website has 4 different font sizes and another section below it might need a few extra sizes, try to *reuse* 2 or 3 of the sizes from the section above, instead of comning up with 4 completely new font sizes.

Most visual changes needed in font size would typically be at least 2px values so try to avoid 14px here and 13px there, when one or the other will do.

#### Power of Font Size Constraint

Below is an example of a little site I put together [https://thinkethbook.com](https://thinkethbook.com) that shows the power of constraints when it comes to font size.

1. Default Times New Roman

1. Only one font size

1. Relies only on font **weight** and *style* for important information.

1. Uses generous negative space to give title more prominence

1. Paragraphs have very calculated line height and maximum widths.
## Font Weight

### Why

Font weight affects the perceived hierarchy of information, the readability of text, and sometimes the affordance of action.

In most cases, simply changing from a regular weight font to a bold weight font can be just enough of a change to signal a different meaning with that usage.

When designing interfaces, the type usage is the most critical part of the interface, and making subtle changes here and there can be the best way to emphasize parts of the interface while de-emphasizing others.

### **What**

- Font weight (different styles)

- Visual weight (space, color, layout)

`refer to video for more examples`

On the web, you can set any font's weight using a range of 100-900, or normal, bold, bolder, and lighter.

```CSS
h1 {
	font-weight: normal
	/* other options are bold, bolder, lighter */
}

h1 {
	font-weight: 400
	/* other options are 100, 200, 300, etc. */
}
```

But keep in mind that these options for CSS don't always guarantee that you'll end up with the result you're looking for.

**Weights** has everything to do with what comes with the typeface. THEN, these numbers for weights can be programmattically defined. You don't need to worry too much about this right now.

The big takeaway is that the font you're using defines what weights you have available.

If the font you are using does not include a variety of weights baked in, and you try to force it bold, it will try to do so programmatically. **Do not rely on faux bold and faux italics**. This is a computer-generated thickening or slanting of a typeface and the result is not good.

**Standard weights**

*Light* and *Hairline* should be avoided in most cases with the exception of really large headlines. It's just hard to read in most contexts. But is also depends on the typeface.

*Regular*, *Book*, and *Medium* are generally good weights for body copy.

**Creating weight with negative space**

You can use negative space to surround any particular amount of text to give it implied visual weight and significance.

**Creating weight with color**

Large chunks of contrasting color can create heavy visual weight without even changing the font weight. Think of buttons used as large calls to action.
## Hierarchy

**Hierarchy**—a system or organization in which ~~people or groups are~~ interface elements are ranked one above the other according to status or authority.

### Why

When you're designing for a screen, it's important to consider the hierarchy of your layout. And that hierarchy is typically produced first and foremost by your typography size and style. Hierarchy is important because it elevates the significance of one UI element over another in in the context of the full layout.

This doesn't mean that all titles should be necessarily be larger and more important than body copy or that all interactive items should be colorful and more pronounced... It just means that hierarchy is important to consider while creating your design.

### What

Some key things to think about when considering hierarchy on your screen.

- What do you think the user is *planning* to do on a particular screen?

- Are they exploring and browsing or trying to accomplish something very specific?

- What are you *hoping* the user does or can do on a particular screen.

- What is the most important piece of information on the screen? Second-most? Third-most?

Headlines or titles for a general layout are often the most important element on landing pages or more general type pages.

`screen reference in video`

- apple.com

- text messages vs. individual text message

- gosquared dashboard
## Titles & Body

### Why

Titles combined with body copy makes up the majority of most interfaces and could easily be considered the core part of any nearly any interface—whether it's a marketing site, a complex web app, or a simple mobile app.

Yes it's mixed in with titles and subtitles, calls-to-action and more, but once you drill down into any type of app with a detail page, you're going to end up reading.

### What

#### **Pixels vs Points**

They are used interchangeably, but are slightly different. The simplest explanation would be that 10pt would be the same for a 1x screen, 2x screen, or 3x screen in terms of screen resolution, but in pixels it would be 10px, 20px, and 30px. So as long as we're always designing at @1x on digital screens the ratio of pt:px will always be 1:1.

*A longer description on points vs. pixels from *‣

> [!NOTE]
> *To weigh in on pt vs px, it's actually a very deep rabbit hole. Most design software these days uses "reference pixels", meaning when you type 16px into that size input, it's giving you 16px @ 96dpi – because 16 physical pixels on modern displays can be tiny.
>
> ****If pt == 'dpi point', it's equivalent to a reference pixel**** aka 1pt = 1px @ 1x resolution. ← This is what I think  means, and commonly what you'll see in design docs. Material Design, for example, uses the abbreviation 1dp ('device independent pixel') instead to make the distinction clear.
>
> ****But in print typesetting****, pt == "imperial point", it's 1/72nd of an inch no matter what – and converted to reference pixels, usually that means 16px ~== 12pt
> (pixels = points * 1.333) *😭*
>
> EDIT: Short version –
> If the pt values come from print, multiply by 1.333
> If the pt values come from digital design docs, it's likely 1:1*

#### Title Size

These are general approximations not strict laws.

**For (mobile) apps**

Primary: `34–17pt`

Secondary: `17–13pt`

**For the web:**

Primary: `96–24pt`

Secondary: `34–16pt`

#### Title **Weight**

The *weight *for your titles should be at least 2-3 steps darker than your body copy, depending on your selected typeface.

1. **Bold** `Title`

1. *Semi-bold*

1. *Medium*

1. Regular `Body`

The larger you go with your title size, the greater the flexibility you have with your title weight. The titles will naturally seem bolder as you get larger, so you'll have more room to explore here.

→ [*Hoefler & Co. Reference*](https://www.typography.com/fonts/decimal/how-to-use#decimal-emphasizing-text)

#### Title **Line Height**

Your line height on multi-line titles should be less than the line height on you body copy. The larger the type size you use, the large you can see the line height cap take affect.

**Title Case or Sentence case** `100% – 120%`

**UPPERCASE** `80% – 100%`

At a minimum for title case or sentence case, you need to make sure your ascenders and descenders aren't clashing with each other and this will largely depend on the typeface you're using. With UPPERCASE letterforms, they're more blocky and you can get away with tighter line heights because the top and bottom of each letterform is in the same location.

Ascenders like in the lowercase letters `b d f h k l` can often extend higher than their caps counterpart `B D F H K L`.

#### Title **Width**

**For marketing web sites or articles on large screens**

Make sure there is a nice amount of negative space around your title. This can be done by using short titles, layout grids, and also by manually line-breaking longer titles to contain an even amount of characters.

**For apps and small screens**

The width will likely extend to the edges of the screen or up against other interface elements. Make sure that there is appropriate padding around the edges of the screen and the other elements.

For unavoidably long titles, as is often the case with user-generated content, make sure your designs show the variations of short titles, medium length titles, and long titles. Often times this may mean one line, two line, or three line titles.

However long the titles may be, you will also likely need to account for the truncation of the title using an ellipsis (...) which indicates *more.*

---

#### Title Alignment

The majority of the time the term "alignment" is used in conjunction with Typography, it's referring to horizontal alignment—left, right, centered, and the not-so-used-really-at-all justified.

Titles are most often aligned left or center depending on the screen layout and overall direction of the design. The biggest thing to keep in mind is not to carelessly mix centered and left aligned titles and body copy.

For short blocks of copy paired with a title, both strings of text can be center aligned without legibility issues, but the longer the body copy, the more likely it needs to be left aligned.

When you have left aligned body copy, it can be odd to have centered headlines unless you specific layout works it in in a nice way.

- Left or centered (depending on context)

- Make choice based on the visual balance of other elements

#### Body Size

Body size is typically 16px by default, but can go slightly larger or smaller depending on the context of your design. Some typefaces need an extra bump in size to read well, and other use cases like technical information, etc. might be fine using a 13px font.

#### Body Weight

`Book, Regular, or Medium` is a great sweet spot for most body copy. You can of course go bolder if your particular design calls for it, but you should 🚫 **never** use `Thin, Light, or Hairline` for body copy. Those lighter weights do not render well at smaller sizes and become quite hard to read.

Decide your body weight in conjunction with other elements in your layout, including titles.

#### Body Line-height

Optimal line-height for body copy is anywhere from  `125% – 175%`

#### Body Width

The magic character count number for body width falls somewhere between 45–75 characters, including spaces. Refer to [readable.now.sh](http://readable.now.sh) as a good example.

Here's a Chrome plugin to test line width on websites.

[Link: 45to75](https://chrome.google.com/webstore/detail/45to75/efmppndinjbljeellfdkpghgblenbcdd?hl=en)

This isn't often an issue on smaller screens, because body copy spanning the full-width is often nice and legible, but it becomes of utmost importance as screens get larger.

If the body copy stretches too wide it becomes too long and hard to read from the end of one line to the beginning of another.

The best way to handle this on the web is with CSS `max-width: $number` on the paragraph tag or its container:

```CSS
p {
	font-size: 18px
	line-height: 125%
	max-width: 70ch /* 700px, 40rem, etc. */
}
```

It's not that important that you know CSS syntax as an interface designer, but it is extremely important for you to make sure that paragraphs don't extend too wide.

#### Body Alignment

In general, body text should be default aligned to the left. This refers specifically to a block of text, like multiple sentences or a paragraph.

Sometimes body copy might appear as one sentence and in this case there is great flexibility with how it can be positioned.

- Amount of content allowed vs. *Read More*

- Expand/Collapse or new page

- Alignment
  - Left, centered, or right (depending on context)

  - Make choice based on the visual balance of other elements

#### Letter-spacing

In regards to L E T T E R S P A C I N G,

You should only "noticeably" letter-space ALL CAPS. By their very nature ALL CAPS are blocky and can easily be letter spaced and still look pretty nice.

But **NEVER** letter-space out l o w e r c a s e   l i k e   t h i s. The letter forms are too inconsistent and ends up looking very odd.

This is a BIG typographic no-no.

You can track out or in lowercase to give the entire body copy a little more air or a little more condensed, but never so much that it looks spaced way out.

---

**Title Tips**

You may find that using additional elements *WITH* your title will help give it more balance. Look at the example below from a Medium article. Notice how the avatar, username, and date balance the book mark and more icon on the far right—like an invisible horizontal line.

These items below the actual title give the entire header more visual weight, which naturally creates a nice hierarchy.

Consider adding some additional information like this to your Title homework as well. 👍

This is a beautiful site that has great typography combos on the articles

[Link: Homepage | The Atavist Magazine](https://magazine.atavist.com/)
## Callouts

### Why

"Callouts" add visual interest to typography-based layouts and the term is more of a graphic-designed based typography term whereas on the web you might find callouts more often than not taking the form of "block quotes" or "pull quotes"

They can be used to "call out" attention to any specific information you'd like to highlight.

Callouts can be created with other elements like background colors, borders, arrows, and more, but we'll be specifically looking at typographic callouts in interfaces here.

Another way to think about a Callout, is some special attention given to text that grabs attention for a specific reason.

Despite all of this, when you are constantly battling between form and function, you must make sure you aren't overdoing your typography so that functionality is hindered.

These are mostly used in content heavy layouts meant for consumption. Think articles, longer form text, marketing websites, etc.

A typographic callout would technically not refer to any special functionality, though it certainly could if the situation warranted such a treatment.

### What

Let's go over a few examples of typographic callouts in some interfaces...

- Clock iOS app time stamps

- App store first sentence with bold letters

- Eyebrows (small all caps headers above the main header) Games tab in iOS app store

- Testimonials on AIUX (combined with quote, avatar, company logo, etc)

- Testimonials on Basecamp (super bold)

- Testimonials on MyMonero

- Callouts on 12Stone.com's website

`Refer to the video above for examples`

### How

**Change type size and or case**

A good way to start out experimenting with this is by doubling or even tripling the size of your text. Try ALL CAPS, but keep in mind that when you go larger in size, you'll need to reduce your line height.

**Change the color (text or background)**

Try changing the color of you text in addition to or instead of changing the size. Just be HIGHLY aware if you are using an "interactive" color within your design.

For example you wouldn't want to make a big callout the exact same color as your link color. We will cover color usage more in-depth in another lesson, but do be aware that each color you use has an intrinsic meaning based on the functionality you assign to every element

**Combine other elements to create a lockup**

Often times a larger quotation mark or horizontal line can create more visual interest. This is the mystery of design. There is often no right or wrong in these cases, because it's highly dependent on the outcome you are going for.

**Break the format**

Try breaking the boundaries of the existing design. Grid and structure is great for keeping everything organized, but there are ways to break out of the grid to create visual interest. This is something that you will constantly have to experiment with.
## Truncation

Truncation happens often in interface design, because so much of the data we see in apps is user-generated and the length of content is somewhat unpredictable.

Whether it's usernames, video titles, or a list of random things... chances are someone other than the designer of the app, populated that thing with some data.

### **Homework**

- Design 3-5 components of either the Youtube sidebar or the Apple Podcast app.

Go for a pretty pixel by pixel copy of this one to get a feel for the exact sizes and spacing they're using.

**YouTube sidebar**

*You may want to grab your own screenshot and paste into your design tool*

**Apple iOS Podcasts**

#### More inspiration

For typography layouts [https://www.typography.com/blog/type-capsules](https://www.typography.com/blog/type-capsules?utm_source=Email&utm_medium=Email&utm_content=CTA&utm_campaign=NEW_Type_Capsules_2020-02-05)
## Text Style Definitions

### Why

When you read a legal document pertaining to an agreement between two parties, you'll find language like this...

*This Statement of Work #01 (“SOW”) is dated [today's date] (“Effective Date”) by and between Awesome Client, LLC (AC, Client) and Studio Co (“the Service Provider, Service Provider”), and is executed in accordance with and subject to the terms and conditions of the Parties’ [today's date] Master Services Agreement (“MSA, Agreement”).*

At first glance, it might seem like overkill to have the additional descriptions in parentheses, like ("Service Provider"), but this is in fact the clearest way to describe certain words that might be used later in the document so it is clear to everyone reading the document, what exactly MSA means if used in the language somewhere.

The entire purpose of definitions in a legal document or even language for that matter, is for clarity's sake. We have to mutually agree on the definition of a word before we can agree on any concept that that word might be used to describe.

THEREFORE, it is also imperative that we DEFINE our text styles (font choice, size, weight, style, treatment, etc.) with their own definitions. As designers we have the power to assign and define any text style or treatment however we'd like.

One of the worst things we can do for our typography, is to mindlessly throw around styles and treatments without regard for their systematic impact.

### What

`Refer to video for examples`

- Figma's interface. Inter Font. 11px Bold. 11px Regular. #222222 and #B3B3B3

- Apple's iOS structural typographic system

- Skyscanner or other personal typographic systems

- Outline the use of headers, subtext, body copy, action items, links, ctas, helper text, input text, labels, and more.

- navigation text and action item text

### How

`Refer to video for examples`

You don't have to start off designing the system itself, but rather let it evolve from designing individual components, and slowly let those components come together to inform your system of how to work.

- How might titles be treated?

- How might my interactive color be treated?

- How might my links (go somewhere) vs. actions (do something) be differentiated?

- Will certain background colors and treatments affect the meaning of what my text will do?
## Interactive Text

### Why

A user needs to know what is clickable and what is not.

What action, if any, does the style of the text represent?

Is it read-only or is it interactive?

These are things that need to be defined when designing interactive text.

It is imperative for the text on an interface to have clear meaning for the user.

That meaning will vary project by project and each one must have a clear interaction style.

### What

What text on an interface is interactive? And the text that is interactive, is it an action, a destination, a link? A small contextual action or a large primary, page changing action.

A few examples of interactive text include, but are not limited to the following...

- Navigation

- Actions—Primary and Secondary

- Links (note WCAG accessibility with underlines)  (default, hover, hit, active, visited [less often used])

- Destructive Actions

- Interactive Line Items

- Reinforce definitions for user

`Refer to video for examples`

Interactive text may be defined by the following properties:

- position

- size, weight, or style

- text color or background color

- surrounding elements such as borders, backgrounds, and icons (exxon)

- or any combination of the above

### How

`Refer to video for examples`

> As a general rule, the larger the impact of the action, the more drastic the change in color, contrast, weight, etc. should be
## Combining Text and Elements

### Why

Most interfaces are a combination of multiple elements, not just lines of text only. Quite often you'll be combining text with other text as well as other elements.

It's important to have a grasp on the proper way to combine text with other elements so you can create the best designs possible.

> Our primary focus here is creating balance with the text and over other object.

### What

`refer to video for examples`

Your text needs breathing room.

- Make sure to pay special attention to the space around the text in all instances.

- When multiple text fields are together, include variety to distinguish each ones purpose.

### How

`refer to video for examples`

> Pay special attention to negative space when combing text with other objects.

### Key Takeaways

- Pay attention to overall balance at a high-level. (zoom out)

- Create the balance at a low level—size, spacing, color, copy, etc. (zoom in)

- Be **generous** with your negative space surrounding all text elements.

- When aligning text horizontally, align with the baseline.
## Starting with System Fonts

### What

1. **iOS** – [San Francisco](https://developer.apple.com/fonts/)

1. Device Capable Fonts

1. **Android** – [Roboto](https://fonts.google.com/specimen/Roboto)

1. **Windows** – Segoe UI, MS Sans Serif (Not available for purchase, comes with Windows operating systems)

1. **World Wide Web** (slightly less important to keep in mind)
  - Times New Roman

  - Arial

  - Courier New

  - Verdana

  - Georgia

  - Palatino

  - Garamond

  - Bookman

  - Comic Sans

  - Trebuchet

  - Arial Black

  - Impact

### Why

User familiarity is perhaps one of the most important reasons for using a system font, especially if you're designing a native iOS or Android app.

Think about the way you use your phone. It's a utility first and foremost—checking the time or weather, setting alarms, scrolling through any number of social media posts. It serves as a passageway to get you to the content your trying to see, hear, watch, or... as much as I hate to say it, consume.

It's not that common specifically with interface design, when there is a really big opportunity to go super custom with non-system specific fonts.

Interface design for the web is a slightly different story. There are many more ways to ensure   the same font is seen across multiple browsers, etc. However, learning to design with the system font stack, is a great way to tip-toe into the world of typography.

As you get more confident and want to venture out, *then *you can start experimenting. In fact, I encourage you to just that. Using new and unique fonts are amazing ways to stand out from other websites and pieces of software, just make sure you don't over do it.

Using restraint in design is often a foreign concept for new designers. Don't be afraid to consciously "not over-design something" especially when it comes to crazy typography.

#### One less decision to make

When you're designing a new project, there are so many decisions to make. Sometimes a brand already has a font that is "their font" and you need to use that. Other times you're designing specifically for iOS and Android, so it makes sense to start with the system font.

Using constraints, even if self-enforced, is a great way to make great designs. Having an endless possibility of fonts, colors, and pictures is an easy way feel overwhelmed. So make it easy on yourself when you're getting started and consider going with the tried and true system fonts. It doesn't make you any "less" of a designer.

#### Performance

Speed and performance is key. Baking a font set into a downloadable app, isn't *that* big of a deal, in terms of overall app size and performance...

BUT...

When you're using custom fonts on the web, often times there is javascript that must be loaded to call a third party server and the load times can easily get bloated and slow down the speed of the initial load time of a website. Slower load time, means visitors are bouncing. Visitors bouncing, means few conversions. And at the end of the day, we're designing websites, mobile apps, for people to **use**. What's the point of designing something that's hard to use?

Custom fonts are great when used wisely, but there are many considerations to sift through, so again, don't feel bad to start with common system fonts.

#### Cost

Cost is another huge factor. Are you or your client or your team willing to pay annually for a unique font. Are there view limits associated with the font? For example, 100,000 views per month?

I did, one-time, convince a client to spend $999 on the complete [FF Mark font family](https://www.fontshop.com/families/ff-mark/buy). It took some time, and I really did believe this would be a wise way for this particular company to have a very unique font for their project.

There have been plenty of other occasions, where I suggested specialized fonts for web projects, in fact I'm a huge advocate for that, but *starting out*, don't be afraid to keep it simple.

### How

System fonts and their various weights can take you very far. At the end of the day, I want to drill into you that using system fonts is a good thing.

Only venture outside the font box, when you reach a point where it just *feels* like you need something different. That may be on the very first project for you, and that's ok too.

**You are the designer**, so unless there are font requirements for your project, **YOU** should decide when to use a system font and when you feel like going custom.
## Choosing and Using Alternate Fonts

The primary reason you'd opt for a non-system font is to standout. Often times it's a branding decision that requires the usage of a non-traditional typeface.

The same way not every song has the same guitar riff or the same drum beat, every app or website doesn't necessarily need the same typeface.

**Page 96. Elements of Typographic Style**

> ...a (type) face of modest merits should be handled with great discretion, formality, and care. It should be set in modest sizes (better yet, in one size only) with the caps well spaced, the lines well leaded, and the lower case well fitted and modestly kerned. The line length should be optimal and the page impeccably proportioned. In short, the typography should be richly and superbly *ordinary, *so that attention is drawn to the quality of the composition, not to the individual letterforms.

Make sure you aren't just using a random font without a purpose. And absolutely do not use a font in your designs before you know for sure whether or not it is even available as a webfont or has the ability to be used in an app with an app license.

### What

- Serif, Sans, and Mono-spaced. Things to consider

- Why you may choose non-system fonts

- Simple vs. heavily branded

**Possibilities for using alternate fonts **

1. Custom display font for titles only + standard body copy etc.

1. One custom font used for everything

1. Two or more unique fonts used specifically for different things

`Refer to video for examples`

### How

- Do your due diligence BEFORE you design a whole bunch of things. Explorations are totally fine and encouraged.

- how do I pair fonts?

- keep these things in mind when pairing fonts

- show different projects of my own where I chose a different typeface to work with

**First priority is determining usage**

For what purpose are you using a custom font?** **

Display only?

Display and body copy?

**Legibility**

Make sure the font your using is not hard to read. Especially for body copy.

**Does it have a good x-height?**

X-heights that are too low will be harder to read than a slightly higher x-heights. A good rule of thumb for a body copy candidate would be an x-height in the 60-75% tall ballpark. Higher or lower than that will be hard to read.

**How's the whitespace?**

This refers to the spacing between the actual letterforms. If the letter-spacing is too tight, the letterforms will run together and affect legibility. We can control the letter-spacing or tracking programmatically, but this should be a last resort after an optimal typeface is chosen.

**Typeface Feature Checklist**

- Good range of weights—light, book, medium, bold, black

- Italic styles

- Different widths – Does it have condensed and/or extended versions? Not a dealbreaker, but something to consider.

- Small caps (?) – Does the typeface include 'small caps' as a part of the family? Nice to have sometimes, but definitely not a deal breaker.

- Accented characters for language support

- What kind of numerical figures are included—old style and lining figures. Old style varies in height, whereas lining all have the same height and baseline.

#### **Cost**

🆓  **Free**

Limited choices and all the good ones are used heavily in other places. Not easy to differentiate yourself by using the same typeface as everyone else. But type isn't the only way to standout, it's simply one piece of the pie... but it is a large piece. On the plus side, it's free!

📆  **Subscription**

Paying a monthly or annual fee for serving custom typefaces is a great option. You do need to check though based on your usage. App licenses (if they are available) can be more expensive than web licenses. This will vary from service to service.

💰 **Premium**

Buying fonts directly from type designers is a great way to get a very high quality font that stands out amongst a crowd, but the downside is that the price tag is often heftier. I typically have conversations very early on with clients about potential options for fonts and the variety that is available.

Often times these fonts require "self-hosting" the font on your server or within your app. This means that the font files themselves are literally baked inside of the app, or resting gently in your folder of files on your server along-side your .pngs and .html files. It's important to know these things before you start using these fonts in your design. Research before you start!

[Fontshop](https://www.fontshop.com/families/sachsenwald) is one of my absolute favorite websites to browse amazing fonts from many different Type Foundries.

Another great go-to font discovery website is [MyFonts](http://myfonts.com).

Here are a few examples of independent foundries to get great typefaces.

**More resources**

---

- [Choosing a typeface](https://www.smashingmagazine.com/2011/03/how-to-choose-a-typeface/)

- [Upping your type game](http://jessicahische.is/talkingtype)

- [Historically accurate example](http://jessicahische.is/internetting/gatsby/ver2.html)

- Trial font downloads from Grilli Type [https://www.grillitype.com/free_trials](https://www.grillitype.com/free_trials)
## Typography Overview

**Main Points**

---

1. Typography and copy is the majority of design

1. Readability is most important.

1. Letter-spacing. Paragraph width.

1. Focus heavily on good typography. This is a cornerstone for good design.

---

Getting good with typography is one the single-best skills you can build. Knowing which font, size, weight, color, etc. is a universal design skill that should always be at the forefront of your decision-making process.

Within the world of interface typography, there are four main areas that I consider to be the most common and most important. Please remember, that this list, nor any other list  is not completely and fully exhaustive. It is meant to be used as a platform. A springboard. Use this as a baseline and go from there.

#### Utility

A major purpose behind typography is utility. This means presenting the text in a
way that is useful, clear, and legible to its reader. The content of a web page could
be incredible, but if the typography is lackluster, then it’s going to be difficult for
people to read and navigate. They’ll either struggle through it or quit along the way.
Both situations are undesirable. This is why typography as utility is extremely
important to present text in way that’s clear, orderly, and legible for readers and
users of your site.

#### Personality & Mood (Art Direction)

Type can have a personality or mood. It gives off a certain vibe and conveys something to the reader before they've even digested a single word on the page. The flavor of your typography should match the voice of your content. You don’t want something that looks like chocolate ice cream to taste like meatloaf.

#### Elements of a Typeface

- Cap height

- Baseline

- X-height

- Descenders

- Ascenders

- Serif & Sans Serif

- Contrast
  - High contrast – thick vertical, thin horizontal

  - Low contrast - same size vertical and horizontal

- Color (Weight)
  - Light

  - Medium

  - Bold

  - etc.

[Link: Figma - The Basics of Typography | Learn the fundamentals of good typography and invite readers into your content. What you will f...](https://www.figma.com/community/file/930972336020673565)

### Types of Type

#### **Serif**

A serif is the small extra stroke found at the end of the main vertical and horizontal strokes of some letters. Hence the name, Serif Typeface. Letterforms without these serifs are called *sans serifs.*

Here are a few different serif sub-types.

1. **Humanist**
  - Strong calligraphic influence, diagonal stress, relatively small x-heights

  - Eg. Jenson, Kennerley, & Centaur

1. **Old Style**
  - More refined as type, less calligraphic, less diagonal stress

  - Eg. Goudy, Palatino, Perpetua, & Plantin

1. **Transitional**
  - Even more decreasing calligraphic flow, thinner and flatter serifs, exagerated thicks and thins

  - Eg. Baskerville, Bookman, Clearface

1. **Didone**
  - No influence of the pen, thin serifs with no bracketing, extreme contrast, reminiscent of high fashion culture, best for display only

  - Eg. Bodoni, Didot

1. **Slab**
  - Thick serifs and low contrast, heavy headline usage "look at me"

  - Eg. Rockwell, Clarendon, Sentinel

#### Sans Serif

Sans-serifs are the most commonly used typefaces in interface design. However with the advancement of high-pixel density screens, serif typefaces that were once not used because of legibility issues, are now used heavily for long form body copy on sites like Medium, New York Times, etc.

#### Sans Serif – **Grotesque**

- Low contrast, possibly derived from Didot

- Eg. Akzidenz-Grotesk, Franklin Gothic

#### Sans Serif – **Neo-grotesque**

- Desire for simplicity. Not always great for body copy because of legibility, especially at small sizes.

- Eg. Helvetica

#### Sans Serif – **Humanist Sans**

- Great variations in line width, because of the calligraphic roots. Most legible of sans serif bunch at small sizes.

- Eg. Tahoma, Gill Sans, Frutiger

#### Sans Serif – **Geometrics**

- Based on geometric shapes like circles and squares.

- Eg. Futura, Bank Gothic, Gotham

#### Scripts

1. **Formal**
  - Mimics writing-masters from seventeenth and eighteenth century. Contrast between thick and thin the way a quill would be used by hand.

1. **Casual**
  - Light-hearted, easy going. Think of hand-writing fonts.

[https://practicaltypography.com/](https://practicaltypography.com/)

#### Type Tidbits

There are lots of little tidbits when it comes to type that will be of varying importance along your typographic journey. Here are some of those tidbits.

#### Line height

Line height refers to the negative space between each wrapping line of text. A good starting point for body copy 150% of your type size, but this can range from anywhere to 125% to 185% depending on the type face, the content, etc.

#### Letter-spacing (also called *Tracking*)

Letter spacing

Use with restraint and caution on 90% of your text. All fonts have some form of spacing baked into the typeface by design. Adjusting the space between letters is just as important as designing the letterforms when it comes to type design.

Typefaces that are really well done will have paid special attention to letter spacing by default.

#### Paragraph width

- 45-75 character wide is the sweet spot

[http://readable.now.sh](https://readable.now.sh/)

#### Kerning

Kerning is like letter-spacing, but only applies to the space between two individual characters.

This should really only be used for isolated instances, especially in fixed elements such as logotypes, or special titles.

#### Tabular Figures/Numbers

In short, this is monospaced numbers for a non-monospaced typeface. Great for tables, anything financial, etc. when scanning numbers in a fixed-width is helpful.

#### Ligatures & Discretionary Ligatures

- Special characters used when combinations are found. Most popular ligature is "fi"

- Icon fonts are created using ligatures

#### What about Vertical Rhythm?

If you want to do it, go for it. I've never once in my last 15 years of designing used a mathematical equation for vertical rhythm. Could that be a mistake? Maybe in someone's eyes, and I'm OK with that.

I do strive to achieve balance in my typography and overall composition, but I find it much easier to do so with **implicit** grids and relational proportions.

True Vertical Rhythm requires an **explicit** grid for everything to adhere to. I'm much more of a fan of an **implicit** grid.

If you really really want to learn about mathematical vertical rhythm and get super nerdy (which isn't  a bad thing) with math equations, then go for it.
