# Accessibility Checklist

#### 📐 Layout

- [ ] Have you used standardized controls and components in a very intentional way?
- [ ] If you haven't used standardized controls, do you have a very good reason? And have you talked to your developer about implementing it in an accessible way? *(Example, auto-suggest lists have a specific way of being implemented to be screen-reader friendly)*
- [ ] Can a user visually navigate a page in a logical way?
- [ ] Is there a clear page title that states the purpose of the page?
- [ ] Do the headers accurately convey the structure of information?
- [ ] Does the visual order match the reading order? (Left to right, top to bottom)
- [ ] Do the interface elements have appropriate labels? *(Inputs, checkboxes, radio buttons, etc.)*
- [ ] Do the clickable actions have clear action-oriented labels? *(Download, Sign Up, Log Out, etc.)*
- [ ] `Developer` Don't put status text or other non-interactive elements into the tab order
- [ ] `Developer` Are you using the `<a>` and `<button>` tags appropriately? *(They can both be triggered by Enter, whereas the `<button>` element can additionally be triggered with the Spacebar)*
- [ ] `Developer` Can a screen reader scan your project's interface? *(A screen reader will announce headers, specific areas, links, buttons, and controls along the way)*
- [ ] `Developer` Do keyboard controls provide a logical and predictable order for navigation?
- [ ] `Developer` Have you defined [Roles](https://www.w3.org/TR/wai-aria/#document_structure_roles), [States, and Properties](https://www.w3.org/TR/wai-aria/#global_states)?

#### 🅰️ Typography

- [ ] Is the text at a readable size? *(Primary body copy no smaller than 16px)*
- [ ] Do the titles and body copy have optimal line height?
- [ ] Do the paragraphs fall within the optimal character width of 45 – 75 characters? [https://readable.now.sh](https://readable.now.sh)
- [ ] Have you considered how your design will *read* if you closed your eyes and had someone describe what they see in a logical order?
- [ ] Have you considered the responsive nature of text-based content and created rules around truncation and or change of layout based on viewport?
- [ ] `Developer` Are you using `<strong>` and `<em>` appropriately with semantic markup?
- [ ] `Developer` Have you considered creating a "large font size mode"? *Sometimes this can be done with creative development by using the mobile styles on larger viewports.*

#### 🎨 Color and Contrast

- [ ] Is information conveyed by means other than color alone? *(Underlined links, status indicators, etc.)*
- [ ] Does text meet the minimum contrast ratio requirements? (3.0 for large text and informational graphics, 4.5 or higher for all other text) [https://usecontrast.com/guide](https://usecontrast.com/guide)
- [ ] `Developer` Have you considered creating alternate color themes or a high-contrast version? (AAA–7.0 or higher for all text) [https://whitehouse.gov/accessibility](https://whitehouse.gov/accessibility)

#### 🌆 📺 🎶 Media

- [ ] Have you avoided text inside of bitmap graphics whenever possible?
- [ ] Have you made transcripts available for any audio files? *(Helpful for the deaf and for people who aren't in a suitable environment to listen)*
- [ ] Have you provided closed-captions *(and transcriptions)* for any video content? *([Rev](https://rev.com), [Descript](https://descript.com), etc.)*
- [ ] `Developer` Have you checked your icons for a minimum AA Large (3.0) contrast? Have they been properly labeled via the interface design or within the code?
- [ ] `Developer` Does all of your image-based content have alt (alternate text)? *(Also helpful if internet connection is slow)*

#### ⚙️ Functionality

- [ ] Have you provided feedback for user specific user interactions? *Clearly communicate what's happened, what can be done next, etc. Validation and error messages?*
- [ ] Have you made sure that no part of your interface flashes more than three times per second? *(This can cause seizures)*
- [ ] Make sure your site or app doesn't change context or activate functionality automatically. *(Newsletter popups anyone?)*
- [ ] `Developer` Have you provided identification for languages `<html lang="en">`?
- [ ] `Developer` Don't automatically refresh an entire app canvas unless it is really necessary for app functionality. *(Assistive technologies generally must assume that a page refresh is a totally new structure.)*
- [ ] `Developer` Have you used Accessibility tools to verify screen reading experience? ([Accessibility Insights](https://chrome.google.com/webstore/detail/accessibility-insights-fo/pbjjkligggfmakdaogkfomddhfmpjeni/related), [Axe](https://www.deque.com/axe/), etc.)
- [ ] `Developer` If you haven't used only native HTML, have you implemented the correct ARIA (Accessible Rich Internet Applications) roles to bridge the gap? *(Note some HTML5 elements don't have accessibility support, so using both HTML5 elements and ARIA roles can be used to cover those gaps.)*

#### 📚 More Resources

- [Apple.com/accessibility](http://apple.com/accessibility)
- [iOS 14 accessibility overview via Stark](https://www.getstark.co/blog/where-accessibility-shines-in-ios-14)
- [Princeton University A11Y Checklist](https://ux.princeton.edu/accessibility/accessibility-checklist)
- [UX Design CC A11Y Checklist](https://uxdesign.cc/accessibility-checklist-195da7ab64fb)
- [Microsoft Design A11Y Checklist for Designers & Developers](https://medium.com/microsoft-design/an-accessibility-checklist-for-designers-and-developers-a53a7d2d2c97)
- [Inclusive Design from Microsoft](https://www.microsoft.com/design/inclusive/)
- [A11Y Checklist from Wix](https://www.wix.com/playground/post/designing-for-accessibility-a-checklist-for-web-design)

Please know that even the most well-intentioned project is prone to have mistakes. You will very likely never achieve a perfectly universal solution that works for every single person in every situation.

Inclusion is imperfect—just like us humans—and requires humility. It's an opportunity to be curious and approach challenges with a desire to learn.

> [!NOTE]
