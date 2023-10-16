# My Checklists & Icons

[![Video](https://vimeo.com/874879882?share=copy)]

Current version 00.50

My Checklists & Icons is an [Obsidian](https://obsidian.md/) snippet. It will allow you to load a themed set of icons for your Checklist and stand-alone icons. It will allow you to change the icons to fit your workflow best.

## A Note About This Approach
This is a CSS-only approach to managing your Checklist and stand-alone icons. It makes it incredibly easy to load and swap themes. However, adding and changing icons is a little more difficult than simply uploading a file.

Obsidian users tend to be a little more sophisticated and adept at managing files. I don't think this will be an issue for you. The payoff is we get a high level of compatibility and more control over our icons.


## Loading the Snippets
You will need to provide two CSS snippets. The base `My Checklist & Icons.css` snippet and a theme snippet of your choosing. A current list of themed snippets can be found here.

To add your two CSS snippets, follow these steps:
	1. Open **Settings**.
	2. Under **Appearance → CSS snippets**, select **Open snippets folder** (folder icon).
	3. copy the `My Checklist & Icons.css` and your theme snippet into the snippets folder.
	4. In Obsidian, under **Appearance → CSS snippets**, select **Reload snippets** (refresh icon) to see the snippet in the list.

## Using the Snippet
### Using a Checklist Icon

This is as simple as filling your Markdown checkbox with a character. You are probably familiar with this already.
```
- [ ] Is a themed empty checkbox
- [x] Is a themed checked box
- [n] Is a themed icon for a newspaper if a default theme is used.
- [P] Is a themed icon for a picture if a default theme is used.
- [@] Is a themed icon for a person or user if a default them is used.
```

You have 80+ themed icons available. Others can provide you with a theme, or you can create your own.
A complete list of icons can be found here. I suggest you take this markdown file and save it in your vault. It's a great reference to all your available icons.

Some things to note:
1. These are case-sensitive. An "a" will create a different icon than an "A".
2. You are **NOT** limited to just letters. There are many punctuation characters available as well. 

### Insert an icon with your text
You can add the following HTML to add an icon within your text.
```
<i class="mi mi-lessthan mi-animation mi-size"></i>
          ┃  ┃           ┃            ┃
          ┃  ┃           ┃            ┗━ Optional
          ┃  ┃           ┃               mi-xl, mi-2x, mi-3x, etc, etc, etc
          ┃  ┃           ┃
          ┃  ┃           ┗━ Optional
          ┃  ┃              mi-flip, mi-bounce, mi-etc, mi-etc, mi-etc 
          ┃  ┃
          ┃  ┗━ Required
          ┃     Title of any available icon.      
          ┃
          ┗━ Required
```

#### **About Icon Names***
You can easily refer to any icon via the single letter inside the checklist. For example, I can refer to the same icon referenced with `- [I]` with the HTML of `<i class="mi mi-I"></i>`

Punctuation is slightly different since it can interfere with CSS & HTML. So, we refer to `- [/]` with `<i class="mi mi-slash"></i>`.

You can also create a stand-alone icon that isn't associated directly with a Checklist. See below. For example `<i class="mi mi-sample">`

Because this is a CSS-only solution, HTML must be used. I kept the syntax as short as possible to avoid interrupting the readability of a raw markdown file. `<i class="mi mi-q"></i>` shouldn't impact readability a great deal. More importantly, this should translate over to Obsidian Publish without an issue. (Testing and documenting this still)

If you have used Font Awesome, you will be very familiar with the syntax of the HTML since I've adapted their sizing and animation for our purposes.

#### **Sizing**
You can apply the icon size by using any of the following classes. `mi-1x, mi-2x, mi-3x, mi-4x, mi-5x, mi-6x, mi-7x, mi-8x, mi-9x, mi-10x` or `mi-2xs, mi-xs, mi-sm, mi-lg, mi-xl, mi-2xl`

#### **Animation**
You can apply animation to an icon by using the following classes. `mi-beat, mi-bounce, mi-fade, mi-flip, mi-shake, mi-spin, mi-pulse`

You can set the iterations or number of times the animation repeats in Style Settings.

#### **Flipping or Rotating**
You can apply the following classes to flip or rotate your icon. ` mi-rotate-90, mi-rotate-180, mi-rotate-270, mi-flip-horizontal, mi-flip-vertical`

#### **Adding a Border**
You can apply a border to your icon and give it a button feel with the following class. `mi-border`. Width, color and border style can all be set in Style Settings.

## Style Settings
This snippet uses the [Style Settings](https://minimal.guide/plugins/style-settings) plugin to allow you to easily set your default colors, border options, and animation settings. Find the "My Checklist & Icons" section and set it accordingly.

## Change a Checklist Icon
This is the fun part. Checklists can and should be personal to your workflow. 

The icons are nothing more than an SVG file loaded into a CSS file. Let's start with an existing theme and change the icons for your purpose. A blank them file is also provided.

### Step 1 - Find your icon
You can find icons from many sites, such as [Font Awesome](https://fontawesome.com), [Lucide](https://lucide.dev), # [Linearicons](https://linearicons.com), [Heroicons](https://heroicons.com), and [Teenyicons](https://teenyicons.com). Most offer free icons, and you can pay for extended or full versions.

### Step 2 - Convert your SVG
The SVG file must be encoded as a Data URI to be used inside a CSS file. There are many online tools to do this for you, but I like this one from [SVG Backgrounds](https://www.svgbackgrounds.com/tools/svg-to-css/).  Here is a sample of an encoded SVG image.
```
url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-ban"><circle cx="12" cy="12" r="10"/><path d="m4.9 4.9 14.2 14.2"/></svg>')
```

### Step 3 - Add your SVG
Open your themed CSS file and overwrite the SVG for your Checklist icon.

```
	--cl-icon-slash: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-ban"><circle cx="12" cy="12" r="10"/><path d="m4.9 4.9 14.2 14.2"/></svg>');
```

### Step 4 - Use it
You should immediately see your new icon is available for use.


## Adding a Stand-Alone Icon

### Step 1 - Find your icon
You can find icons from many sites, such as [Font Awesome](https://fontawesome.com), [Lucide](https://lucide.dev), # [Linearicons](https://linearicons.com), [Heroicons](https://heroicons.com), and [Teenyicons](https://teenyicons.com). Most offer free icons, and you can pay for extended or full versions.

### Step 2 - Convert your SVG
The SVG file must be encoded as a Data URI to be used inside a CSS file. There are many online tools to do this for you, but I like this one from [SVG Backgrounds](https://www.svgbackgrounds.com/tools/svg-to-css/).  Here is a sample of an encoded SVG image.
```
url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-ban"><circle cx="12" cy="12" r="10"/><path d="m4.9 4.9 14.2 14.2"/></svg>')
```

### Step 3 - Add your SVG
Open your themed CSS file and add a CSS variable to represent your icon within the body element. If it is a stand-alone icon, I suggest you prefix the icon with `--mi`. Followed with `icon` + `name`. In our example, it is `--mi-icon-ban`.
```
body {}
	... Other icons are sure to be listed here already...

	--mi-icon-ban: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-ban"><circle cx="12" cy="12" r="10"/><path d="m4.9 4.9 14.2 14.2"/></svg>');

}
```

### Step 4 - Give Your Icon a Name
We want to add a CSS element to represent your icon.  This is a stand-alone element, so make sure to not have it inside the body element with your SVG.
- The name of the icon should include `.mi.mi-title:after`. This is how you will refer to your icon in your file. `<i class="mi mi-ban"></i>`.
- You also need to ensure it refers to the SVG. This is the `var` portion and should refer back to the SVG in Step 3. Notice that this includes "icon".
```
	.mi.mi-ban:after { 
		-webkit-mask-image: var(--mi-icon-ban); 
	}
```

### Step 5 - Use it
You should immediately be able to use your new icon in your file. You can refer to our example by simply adding the following HTML. `<i class="mi mi-ban"></i>`


## Thanks and please provide feedback
I'm not new to CSS, so I appreciate any and all feedback.