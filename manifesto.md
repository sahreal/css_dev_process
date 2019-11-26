The CSS itself:
- Assuming you’re not using a preprocessor, and you’re not importing CSS into JS modules: I recommend one big file because:
  - It's the best option for performance - don't have to request multiple files.
  - Don’t have to wrangle a bunch of files, consider which one will take precedence, and worry about linking them all in your HTML
  - Easy to figure out where to write you code - you literally have no decision you need to make
- Split your CSS into subsections ahead of time using comments
  - There should be one “general” section - it would house all your text styles, overrides for default styling for particular tags, etc.
  - Each section of your page should get its own section
  - These subsections are purely for navigation’s sake, but TRUST me - it will make your life easier
- Some people say you should write your CSS for the device type you see the greatest traffic on, and then put styling for the other devices in media queries at the bottom. 
  - While this is the standard (at least in what I’ve seen), I prefer to put anything that should only apply to specific screen dimensions into a particular media query
  - This forces you to be more thoughtful, and makes your CSS more readable to those who didn’t write it.
  - Please also clarify what you’re coding for at the top of your code!
  - Wondering what devices should live in what widths? Use your Google dev tools! Personally, I recommend these ranges: 
    - 0px - 600px
    - 600px - 800px
    - 800px - 1000px
    - 1200px - 1400px
    - 1400px+
    - Please keep in mind that this can completely depend on the actual content on your webpage

Workflow:
- Write anything you know you’re going to need ahead of time (just makes your life easier)
- With the CSS open in a window and ready to go, take a look at your page in Chrome. 
- Try CSS out by writing it in the rules for the appropriate selector. If you like it, put the same rules in element.style for one of the matching elements.
- When you’re done with a batch of that - I recommend no more than 5 separate elements - go down the list of newly-created style tags and write the rules into your actual CSS. Save it and then refresh the page. 
  - If responsive web design is a priority for you, try what you wrote in mobile view. If it has to be with placement/sizing, odds are you’re going to need to write other stuff in other media queries.
  - Put the CSS in the RIGHT PLACE. Future you will thank you 1,000,000 times.
  - Make sure all the edits are actually there before you move on to bigger and better things
- Rinse and repeat!

Pro tips:
- Treat your CSS like JS - “it works” is not sufficient. Scalability when it comes to CSS is all about readability/ease of maintenance once you have a ton of HTML you want to style.
  - For example - position:fixed; may put an element where you want it right now…. But what if you add something to the page that goes under it?
- If you want to do well at FEC styling, you need to be a wizard of flexbox. Do that flex froggy game for an hour, and you will be a wizard.
- You have many types of units at your disposal! In addition to px and % (which refers to the measurement of that element’s immediate parent in the given dimension), you also have vh, vw, em, rem. Google them - especially vh and vw!
- CSS Transform, while slightly taxing for your graphics processing, is the most powerful positional tool you have at your disposal. You owe it to yourself to read up on it. It’s fairly simple.
- Keyframes animations are a fantastic way to make your page come to life. Google them as well.
