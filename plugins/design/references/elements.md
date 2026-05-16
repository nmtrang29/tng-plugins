# Elements

Ok, now we're really getting practical. In this section we isolate individual components and commonly found objects in our interfaces and go deep on the details that create them.

---

## Introduction to Elements

**Two quick points for this section**

1. This section is a culmination of everything that's been covered in all of the previous modules, so if you've skipped ahead to this point you've missed out on a ton of good content that build a foundation for these elements.

1. It's extremely important to remember the user experience aspect of design and keep those things in mind while you're designing these elements.
## Navigation

### **Why**

You don't want you user to get lost. Give them clear directions that can't be mistaken. It's more important that they end up where they want to go vs. experiencing a beautiful layout. Let's give them both!

Become painfully aware of the UX vs. UI concept mentioned in the first module. What is someone's baseline (Point A) and what is their destination (Point B)

It's also important to note that there can be multiple user scenarios that all have unique Point A's and Point B's

When you need a navigation vs. when you don't. If someone is in some type of form, it's important that it's designed in a way that eliminates distraction, but still gives them control.

Consider whether someone is exploring vs. *hunting.*

Exploring would be browsing casually on an ecommerce site with no real itent to purchase something yet—just checking things out.

Hunting would be someone who has made a decision to perform a certain action like signing up or checking out, and general navigation becomes less important if it doesn't pertain to that exact goal.

### **What**

Native App vs. Mobile Web

- Mobile Tab Bar  (5 or less)

- Menu Button (hamburger) – Side Navigation
  - Twitter

  - Instagram

**General Principles**

- Pay Attention to Naming Conventions
  - Nouns vs. Verbs

  - Word count (one vs. two)

- Rule of 5~
  - If there are more items to include, consider the importance and either put them in a "More..." tab on a mobile app, or in the footer of a website.

**Examples**

facebook navigation history (grid of icons, hamburger menu, iOS tab bar

- [https://mashable.com/2013/08/01/facebook-mobile-evolution/](https://mashable.com/2013/08/01/facebook-mobile-evolution/)

- [https://www.facebook.com/notes/facebook/introducing-facebook-for-ipad/10150311269432131](https://www.facebook.com/notes/facebook/introducing-facebook-for-ipad/10150311269432131)

**Navigation States**

1. Default state
  - You can click or tap me.

1. Hover
  - I'm reacting to proximity, giving you even more affordance to let you know I can be clicked. Can be styled as an active state, but only shows temporarily while the mouse is hovering.

1. Pressed
  - You just clicked or tapped me and now I'm reacting to that action.

1. Active state
  - I'm currently active.

### How

**Visual Considerations**

- Type Size
  - 10px size is common on iOS tab bars (don't use a light weight)

  - 17px is the most common size for list views on iOS

  - 12-16px is a great size for top navigation on standard websites, depending on style and typography, etc.

  - You can go larger with type size for stylistic reasons, as long as it makes sense visually. (Fibrestream example)

- Location

- Color

- Style

**Invisible Controls (swiping between sections)**

- iOS control center

- Snapchat

- Instagram

**Keep actions and navigation as separate items. **Navigation items GO somewhere. Actions DO something. There are rare exceptions like the "post" icon on Instagram's app

Look at the BIG tech companies that are spending millions of dollars on design. They experiment and test all types of design patterns and there is absolutely no shame in using those patterns in your own designs.

*Key takeaway — use motion or a very light guided tour to show to use it

(Mario example: press B to jump)

**Resources**

- [Apple iOS HIG – Tab Bars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/tab-bars/)

- [Apple iOS HIG – Navigation](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/navigation/)

- [Luke Wroblewski – Obvious Always Wins](https://www.lukew.com/ff/entry.asp?1945)

- [https://usabilitygeek.com/ui-patterns-for-navigation-good-ux/](https://usabilitygeek.com/ui-patterns-for-navigation-good-ux/)
## User Input

> [!NOTE]
> It's important to note, that this is not a fully, 100% complete and exhaustive list of input field components. There may be other combinations like "autocomplete search fields coupled with selectable dropdowns, etc."

#### **Resources**

- [https://adamsilver.io/articles/where-to-put-buttons-in-forms/](https://adamsilver.io/articles/where-to-put-buttons-in-forms/)

- [http://www.effortmark.co.uk/seven-basic-best-practices-buttons/](http://www.effortmark.co.uk/seven-basic-best-practices-buttons/)

- [https://uxplanet.org/the-anatomy-of-input-field-c3ef863e01d7](https://uxplanet.org/the-anatomy-of-input-field-c3ef863e01d7)

- [https://uxdesign.cc/ui-cheat-sheet-text-fields-2152112615f8](https://uxdesign.cc/ui-cheat-sheet-text-fields-2152112615f8)

- [https://www.lukew.com/ff/entry.asp?504](https://www.lukew.com/ff/entry.asp?504)

Alternate "full screen" input field designs can work well for mobile inputs.

#### Homework

Congratulations! You've been tasked to come up with the design of an input field for a new design system. It's just an input field, simple right!? Hold on just a sec... we're gonna need LOTS of variations of these input components. 😅

Let's start off with the following font sizes:

- 16px for labels and input text.

- 12-14px for any additional helper, error, and success text

**Note on input font size: **Once you've got all variations designed, feel free to adjust the size as you see fit. For example, sometimes it's OK for labels to be slightly smaller than the input text, but not the other way around. Helper text should rarely be larger than the labels or input sizes.
## Forms

Any place online, whether it's in an app or a website where you post information or content, is a type of form. Whether you're posting an Instagram story, a tweet, signing up for a new piece of software, or buying a new pair of shoes, you're are using some type of form.

For our purposes in the lessons, we're going to focus primarily on the standard text-based form so we can lock in on the fundamental.

Case studies reviewed in the video:

1. FibreStream Responsive Web  `(1:08)`

1. Smartline iOS app – Sign up for free trial `(21:34)`

**Form Design Considerations**

1. Try to setup the user for success with clear messaging instead of relying on only error messages that slap them in the face.

1. Default to helpful messages vs strong errors

1. No deadends, helpful alternatives (domain names, gmail addresses, etc.)

1. Only what's required up front—as little friction as possible

1. Creating an account. Consider what is absolutely required vs. helpful to know before a user gains access to the app. `Smartline example in video`

1. Input fields and Calls to Action can be similar in size

1. Consider CTA placement for mobile. Remember the keyboard will be showing.

**Possible 3rd party log in buttons**

In addition to username, email, and or password.

1. Twitter

1. Facebook

1. Dribbble

1. Gmail

1. Amazon

1. Apple
## Profile

Think about social media sites like Facebook, Twitter, Instagram, Pinterest, etc. Your profile serves as a public version of yourself in a way and is often deeply personal.

But then on the other hand profiles for other services like your Netflix or Hulu account or less publicly visible and more for your own usage.

Again it's incredibly important to understand what value the "profile" page is going to provide a user.

There's really no incentive to upload a profile photo or add a phone number to an app, when the majority of the usage is going to be personal.

From a general standpoint, a "Profile" is typically thought of as public-facing, whereas "Settings" is reserved for private information that isn't shared with others online.

**Case studies featured in video**

- Rivalry `(1:28)`

- 12Stone `(4:16)`

- Smartline `(10:14)`
## Settings

Settings in general are typically reserved for app specific items (account information, notifications, display preferences)

So from a general point of view, personal public facing details would be considered profile-type information, whereas personal private information would be considered a setting.

There are some instances where some of this information may bleed into the other, but overall a good way to think about settings, is that it is personal and private.

As a designer, try your best to protect the user from Settings overload. They need control, but they also need opinionated design decisions made on their behalf.

Settings case studies

- ZPPR `(1:36)`

- MyMonero `(6:08)`

- Analog `(9:31)`
## Lists & Cards

### Why use lists or cards?

For a majority of apps, cards and lists make up the majority of content that is "consumed" by users.

**Cards** are often used for grouping multiple pieces of content together like an avatar, username, timestamp, photo or video, and text caption. All of these together can be more easily seen as a group if it's contained in a card. Think of any social media app and it's highly likely they are using some card-based layout for their user-generated content.

**Lists** are most often used as a utility, where scan-ability is a bigger factor in the overall experience.

### What's the difference?

The biggest differentiator is the presence of a background module—traditionally in the shape of a card—that is stylistically delineated by color or border, or both.

**Lists**

---

- Don't *always* signify interactivity

- Emphasize hierarchy

- More scannable in groups

- Take up less space

- Groups small amounts of content

**Cards**

---

- Can signify interactivity

- De-emphasize hierarchy

- Less scannable in groups

- Take up more space

- Groups large amounts of content

**List to Card Layout Progression**

---

1. List using only negative space as a divider

1. List using a partial border as a divider (iOS style)

1. List using a full width border with small margins on each side

1. List/card hybrid using larger full width borders that could also be interpreted as the background. This figure could have a black background with grey dividers or it could be seen as a grey background with black cards.

1. Full card usage where the content is undoubtedly in individual regions based on card shapes.

Below is* the same progression with real world examples...*

1. Spotify is using negative space only to segment the playlists.

1. iOS Mail is using a partial border to signify separation of email previews.

1. Calcbot is using a full-width border to separate previous calculations

1. Facebook is using the hybrid approach with the full-width card that could be perceived as large borders or as segmented white cards with no rounded corners.

1. iOS App store using large cards with substantial padding and drop shadows

One layout is not necessarily "better" than the other from a fundamental standpoint, but rather each serves different needs depending on the context of the design as well as the overall style.

#### Cards

Examples below referenced from [NN/g](https://www.nngroup.com/articles/cards-component/).

[**Law of Proximity**](https://lawsofux.com/law-of-proximity/)

The law of proximity creates a strong sense of visual grouping among shapes  2 & 3  and  4 & 5 , because they are placed close to one another, and further apart from their neighbors 1 & 6. It’s required to use negative space to convey grouping.

[**Law of Common Region**](https://lawsofux.com/law-of-common-region/)** **

The law of common regions trumps the law of proximity through the use of a distinct background. Now the same set of shapes in the same position are now grouped differently. The shapes  1 & 2  ,  3 & 4 , and  5 & 6  are now grouped, even though the layout is identical as the figure above.

**Combinations**

---

Also worth noting, cards can contain lists and vice versa. 😅🤯

### How

**General considerations**

1. Design for different types of activities. Lists for example work better for comparisons, whereas cards work better for exploring.

1. Consider margin, type size, background/foreground color, and media size. More condensed than you think.

1. Design them individually, but always test within the context of a full group.

1. Settings list, vs iTunes app store cards. Facebook vs. Twitter, vs. Instagram, ZPPR feed.

1. Which images will you use?

1. Activity. Create variety with which pieces you test.

1. Text only. Text + Icon. Divider lines vs. divider space. Focus heavily on padding and margin. Small pixel increments matter.

> **The more information needed in your list or card, the more dense it should be and the tighter the margins.**

**Pay extreme attention to the following:**

1. The amount of padding you are using for top, right, bottom, and left margins. When in doubt make them all the same. Experiment with several options using 4px increments.

1. Try different pixel measurements, but don't get too locked into your decision up front. Wait and see how the constraints apply to other screens, then go back and decide if you'll have two rules on padding/margin for different screen types.

1. Use just the right amount of color change between the background and foreground.

1. Use shadows and strokes very subtly. Just enough to show contrast, but not too much to become and object of attention on their own

I would encourage you to try different approaches and see which best fits your project's design style.

> [!NOTE]
> **Key takeaway
> **Cards make use of the law of common region, which will always trump the law of proximity. That doesn't mean that you must use cards at all costs, it just means that information inside of a card will always be the easiest way to group information.
## List → Detail

Whether you're designing for desktop or mobile, you're going to have some type of lists or cards that will link to a detailed view.

- Tweets in the Twitter timeline link to a detailed view that show likes, retweets, and replies.

- Facebook cards link to a detailed view of the post, along with reactions and comments.

- Email previews link to a detailed full view of the entire email.

- Cover art for TV shows or Movies most often link to a detail view of that specific content, which in turn reveals more actions.

If there is more than one item in a feed, it's often necessary to show a truncated version as a preview with scannable bits of information that signifies more detailed information exists.

It's also not very common where a user needs to have access to every possible action for every single item all at once. There may be the occasional exception, but most of the time, additional information and additional actions are tucked into a detailed view.

One key thing to remember about this concept, is that you can use this to you advantage when you're struggling to layout a group of items, whether it's read-only content or interactive content.

Sometimes the answer lies within hiding all of these items behind a singular entryway, and treating those items as their own mini-detail view.

### List → Detail Examples

#### **List → Detail transition types**

Regardless of what you're designing, keep in mind what type of transition might occur in your project and how that might affect the overall feel of the app. This will also be a question for the developers if you are unaware of technical constraints, so start those conversations early!  Options 1-3 are fairly standard and wouldn't require any special development implementation, whereas an option like number 4 could very easily cause conflict between designer and developer.

1. Item links directly to detail view via URL refresh—no transition (Eg. Any standard hyperlink)

1. Item triggers a "detail preview" modal on top of existing content (Eg. Pinterest)

1. Item triggers a slide animation from one view to the next (Eg. Mobile apps)

1. Item triggers and animation to either partially or completely take over the list view with a detail view (Eg. iOS App store

**Case Studies reviewed in Video**

1. InVision Run Concept (*Can't provide source files for this one, sorry*)

1. Streamline Conversation Thread (*Can't provide source files for this one, sorry*)

### Practical Tips

Most of the time, detail screens are going to have larger fonts for the titles. Depending on the content type, you may need to give the impression that the user has "zoomed in" to a level of content that is deeper and more close up, than the list they were viewing before.

Think about video thumbnails vs. clicking on one and being fully immersed in a much larger view of the video. This is another example of zooming in on a detail screen.

The main content sitting on top of the text-based information can have full-width properties that the rest of the UI may not adhere to. It's OK to break format a little to accentuate detailed content.

This is a great place to introduce additional font sizes, colors, or layout possibilities, but keep in mind that it needs to feel related to the previous screen. There should be *some* visual consistency so that it feels like a cohesive experience.

There is additional information introduced on the detail screens, but it has a consistent look and feel as the screen that precedes it.

Below is an embedded prototype. You click and drag the dark card to "scroll" or click it to activate the detail transition.
## Sorting & Filtering

There are two key differences between sorting and filtering.

1. **Sorting** rearranges existing content.

1. **Filtering** removes content.

Take a look at sorting and filtering happen in two different ways below in the Amazon and Nike apps.

**Amazon for iOS**

---

- Exposes multiple options of filters inline as well as keeps Sort by: as a separate item.

**Nike**

---

- Hides all filters behind a single icon in the header. Puts "sort" as a child of filter.

It's more and more common for "sort" to be included as an extensions of "filter" rather that the other way around.

#### **What Should I Do?**

The placement of filter/sort is often a UX question and even a business discussion depending on the analytics and opinions involved from the team you're working with. If you can make yourself a part of those conversations and discussions, you'll be better equipped to make stylistic decisions.

Also keep in mind that your designs can also influence decisions like this. Sometimes it may be better to show filters listed out. Sometimes it may be better to tuck them all into a single button and create a separate modal or detail screen specifically for those things.

#### **Simple Filter Design**

Note in the example above the simple "All ↓" serves as the title *and* the filter together. It has a subtle interactivity associated with it because of the down arrow icon.

Tapping the "All" indicator reveals the dark dropdown, where a user can select (All, Calls, Texts, or Voicemails) to filter the messages in the feed.

Also, the search icon acts as a sort of filter as well. It's filtering the messages based on the matching text strings.

You can see in the 5th screen that "*asd;lfkajsdf*" produces *No results.*

#### Shiplify Filter System

Note, the selected filters showing up on top of the content. The mobile filter view is expanded into the left column for larger screens.

#### Responsive Filter from Babycents project

Mobile view becomes the left column of the desktop view. Note the card and list view options for the grid as well.
## Modals

Modals (also know as dialog boxes) create a *mode* that disables the main window but keeps it visible. Users *must* interact with the modal window before they can return to the parent application. This avoids interrupting the workflow on the main window.

Modals *interrupt* users and demand an action. They are appropriate when user’s attention needs to be directed toward important information.

Modals provide a different "mode" of user interface that is related to the main content, but needs more space to provide a clearer set of actions that might not otherwise be possible within the primary flow.

There is an important distinction here to remember to that there can be "Modal" views that absolutely required action before continuing and also "Non-modal" views that do not require action and can simple be dismissed.

### Modal Anatomy

Modals can be thought of as a quick "dialog" or conversation between the software and the user. It's a small contained conversation that requires immediate attention before proceeding.

In this case the software requires the attention of the user, so that it can know how to proceed. The software and the user are engaging in dialog, hence the term "dialog box."

1. A card-shaped module that contrasts the background content and demands attention.

1. A direct and clear title informing the user of exactly what will happen if they are to proceed. In this example, the user is deleting a video.

1. A close icon in the top right that gives the user a way to escape the modal without taking action. On websites, this close action should be further reinforced by allowing the user to press the "ESC" key on the keyboard, or click anywhere on the overlay background (Fig. 7)

1. A direct and clear body of text to provide more context on the action.

1. Primary CTA with button copy that clearly answers the question posed in the title of the modal.

1. Secondary CTA that allows the user a clear way to cancel the action.

1. A transparent overlay that keeps the main content visible, but inaccessible during the modal state.

#### Alert Modals

Alerts convey important information related to the state of your app or the device, and often request feedback.

- Permission requests—apps requesting the ability to access Photos, Camera, Microphone, Location, Contacts, etc.

- Confirmation of a high-stake action—deleting content, deactivating an account, etc. Any action that would have negative impact if it were done by mistake by the user.

It's important to note that on iOS apps, you are only allowed to request permission access once per app install, so many apps will design a faux permission request.

#### Action Sheet Modals

 From the [iOS HIG](https://developer.apple.com/design/human-interface-guidelines/ios/views/action-sheets/):

> An action sheet is a specific style of alert that appears in response to a control or action, and presents a set of two or more choices related to the current context. Use an action sheet to let people initiate tasks, or to request confirmation before performing a potentially destructive operation. On smaller screens, an action sheet slides up from the bottom of the screen. On larger screens, an action sheet appears all at once as a popover.

#### Popovers

From the Apple HIG: "A popover is a transient view that appears above other content onscreen when you tap a control or in an area. Typically, a popover includes an arrow pointing to the location from which it emerged. Popovers can be non-modal or modal."

In it's own way, the mobile keyboard is type of modal and is further accentuated. A cancel or close button provides confidence that the user can successfully exit the modal, even if it's not a required alert.

#### **Interstitials**

Interstitial screens are in the same family as modals, because they do begin dialog with the user, but are more commonly found in-between screens.

Like a "congratulations, you've earned the X badge" etc.

Or this example to the right taken from Slack on iOS after you've signed up.

Interstitials convey a little more information at the end of some type of sequence. Think of them as an officially designed and integrated alert that is less critical than a true alert, but equally as important from a design standpoint.
## Tables

First of all, designing tables can be quite challenging.

It's not always clear what the user is supposed to do with the information inside of the tables in the first place. This makes the design even more difficult.

Well designed tables allow you to do one or more of the items from the list below, but it's IMPERATIVE that you know what problem you're trying to solve before you begin designing the table in the first place.

- Scan

- Analyze

- Compare

- Filter

- Sort

- Manipulate Data (sometimes)

- Gain Insights

- Act confidently

Here are some simple examples that are used quite often, pricing panels side by side to compare options. They may not be the picture of the "standard" table, but rather they've taken visual liberties to bring attention to certain areas. It works.

### How should I design for them?

Are the tables read-only or is their some sort of functionality associated with them?

Their can be lots of individual components associated with more complex tables...

- Sorting and Filtering

- Resizable Columns

- Column Reordering

- Pagination

- Collapsed/Expanded Views

- Edit Mode

- Actions

- Customization

- Truncation

- Icons/Images

- Designing for small screens

- Density settings

Sometimes it can be easier to style tables with CSS instead of using a design tool. This allows for everything to be affected at once, much more quickly, but does come with the limitation of feeling somewhat comfortable modifying CSS.

**Table design checklist**

- [ ] Are the borders and dividers too dark?

- [ ] Do I really *need* vertical dividers?

- [ ] Is the padding too tight?

- [ ] Is all of my text nice and aligned?

- [ ] Am I leaving enough room for notifications, checkboxes, icons, etc. without disrupting the scannablity of the text?

- [ ] Am I using tabular numbers to increase scannabilty?

- [ ] Are any elements repeating too many times that could be condensed into one action somewhere else?

- [ ] Does this table work really well on small screens?

- [ ] Should my text vertically aligned to the top of each cell?

- [ ] Is most of my text aligned to the left?

- [ ] Are most of my numbers aligned to the right?

- [ ] Are there any special fields that should be horizontally aligned to the center?

- [ ] Am I using too many font sizes and or weights?

- [ ] Does it feel cluttered in any way?

- [ ] Am I intentionally wrapping text in cells or truncating it?

Great example from Steve Schoger, where a table doesn't necessarily need to be a table.

**Resources**

- [Design Better Data Tables](https://medium.com/nextux/design-better-data-tables-4ecc99d23356)* by Andrew Coyle*

- [How to Design Complex Web Tables](https://medium.muz.li/complex-tables-356826d11861) *by Slava Shestopalov*
## Design Systems

A design system only works if:

- everyone feels confident about the system

- everyone agrees what the system is

- agrees to use the system

- it's easy to use

- it allows for confident decision-making

- it makes sense for everyone

- it provides options

- it's scalable

#### **Use Cases and Naming Conventions**

Naming things and categorizing things is often one of the most challenging aspects of creating a design system.

Naming conventions will most likely follow suit with the hierarchy of information, but what if there is no hierarchy of information? What if no one has decided whether something should be sorted by color or size first? This is what makes it hard.

There are lots of contributing factors that go into why something is named the way it is.

Imagine you were putting a label on a box that would include various, small, office supplies.

In the box you were going to place staples, paperclips, pens, sticky notes, and scissors. What would be the best label to put on the box, assuming you couldn't see the contents before you pulled the box off of the shelf?

You might consider the name "small office supplies." But is your coworker going to confidently pull the "small office supplies" box down when looking for sticky notes? What about scissors?

There's no clear answer to that question without more context.

If you're a small company and have had conversations with the 3 other people using the small office supplies, and everyone agrees on the simplicity and naming convention, then this would work perfectly fine.

But, if a new employee comes along how will they know where to get the scissors? That's were documentation comes in handy.

But then again, do you want a new employee consulting documentation every single time they're looking for scissors or sticky notes.

This is where making the design system more accessible and more intuitive starts to shine. What if new employees instinctively knew where to look for sticky notes, because there were several shelves with several boxes, with more descriptive labels for each box. This way new employees could come into the supply room and quickly and easily grab what they're looking for.

But this all comes down to what works best for this particular organization and the employee preferences, etc. There is a point when something becomes over categorized, but it's going to be different for every team and every project.

The best way to start is to get "organized enough" and expand from there.

In our example with only 3 employees, having one small box labeled "small office supplies" might work wonderfully. In fact, they may not even need a box! They might be content with having the office supplies scattered around the office.

As they grow, they'll likely need to get more organized.

Video examples:

- Lego

- Flowkit

- Contrast

- Cinesampler

- [Exxon](https://bigmedium.com/projects/unity-design-system-exxonmobil.html)

#### **Possible steps for designing UI THEN creating a system.**

1. Design for a specific use case first, then abstract into a component

1. Only abstract into a component when it feels right to you. Sometimes when it might make the most sense to abstract:
  - When you find yourself duplicating an element more than once or twice

  - When you know that you will have 5 or more of one components, like a list item, navigation bar, input field, etc.

1. Always valuable to use icons as an abstracted component. This keeps the icons closer to production ready and separates the assets from the interface.

1. Separation of assets and interface. Photos, icons, videos.

1. Pay attention to naming convention.
  - Instead of saying "Blue" specifically for a button as the primary button, call it primary... that way it will continue to be applicable if you decide later to change the primary action color.

  - This double abstraction will allow you to change the color later without ruining your naming convention.

1. Combining abstracted components for quick interface building. `Contrast example` `Cinesampler example`

1. If you're feeling stuck and not creative, DON'T start making a bunch of components. Components can always be created later as you are tidying things up. It is 100% not necessary to begin with them. It will take some time to get used to creating and using components as a regular part of your design process, so don't let this make you feel overwhelmed.

1. Frame or artboard size is critical when you want to be able to swap components or symbols. (icon example of 24x24, list item example, navigation example)

#### What about all this talk about "Tokens" ?

"Tokens" are the formalized and centralized version of "Variables" that can become intentional and understandable decisions integrated into the system.

In short, "tokens" are variables that make sense. They can be easily understood, everyone is aware of the naming method, and it's quite intuitive to make decisions with them.

Tokens are the mortar that bridge your decision decisions with the code that implements them. This is why being incredibly intentional with your decisions on type size, margins, padding, colors, etc. is ever-so-important.

Your decisions become **the code** that runs the entire website or app.

If your decisions are haphazard and messy, so will the implementation. If your decisions are smart and communicated clearly, that will translate into the system as well.

![](https://miro.medium.com/max/2000/1*kanvPTzOa4gii9TU1YLBJg.png)

**Example of Abstraction in CSS**

```CSS
.pill {
	background-color: $background-color-light;
	border: $border-hairline;
	border-radius: $border-radius;
	display: inline-block;
	font-size: $font-size-metadata;
	margin: $space-inline-left-xs;
	padding: $space-inset-xs;
}

.pill--reverse {
	background-color: $background-color-dark;
	border-color: $background-color-dark;
	color: $text-color-light;
}

.pill--ghost {
	background-color: transparent;
	color: $text-color-light;
}
```

**Second Layer of Abstraction in CSS**

```CSS
$background-color-dark = $color-neutral-20;
$background-color-light = $color-neutral-90;
$font-size-paragraph = $font-size-m;
$font-size-microcopy = $font-size-s;
$space-inset-default = 16px 16px 16px 16px;
$space-stack-l = 0 0 32px 0;
```

By the end of this guide I want you to have a fundamental understanding of...

- a design file is not a design system, it's a picture of one

- what a design system actually is and why it's used
  - phases of a design system
    - exploration

    - communication

    - decisions

    - revisions

    - documentation

    - implementation

- general principle of abstraction

- reusing and extending components
  - sizing

  - margin/padding

  - naming and categorizing

  - modifying

**Further Reading:**

- [Atomic Design](https://atomicdesign.bradfrost.com/) by Brad Frost

- [Tokens in Design Systems](https://medium.com/eightshapes-llc/tokens-in-design-systems-25dd82d58421) by Nathan Curtis

- [Design Systems Class](https://skl.sh/3dNBm05) by Dan Mall
