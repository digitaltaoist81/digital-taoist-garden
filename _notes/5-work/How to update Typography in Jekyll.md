---
up:
  - "[[The Tao of Programming]]"
tags:
  - idea
  - area/career/programming
  - project/digital-taoist
  - public
title: How to update Typography in Jekyll
feynman:
---

> [!abstract] Tutorial \
> This is a tutorial on how \
> to update the typography \
> for your Digital Garden. 

In case you are \
also using Jekyll \
for publishing your \
Digital Garden, \
please follow these steps \
for updating the typography \
of your site. 

> Typography is not just about \
> letters and numbers; \
> it embodies the essence of a brand. 

> They create a direct link between \
> the audience and the message being conveyed.

## Steps 

1. **Select Typography**: Be mindful over which Typography to use. It will convey your brand and message. 
2. **Check License**: Not all typographies are open and free to use. Be sure to check the license and how you can use it. 
3. **Download Font Files**: Time to download the font files into your computer. 

> [!tip] Opt for WOFF
> Most font downloads come in formats such as TTF, OTF, or WOFF. It’s generally advisable to opt for the WOFF format specifically designed for web use, as it offers better compression and faster loading times. According to industry studies, typography can affect reading speed by up to 10%, emphasizing the need for optimized files.

4. **Prepare folder in repo**: Create a folder for hosting the fonts. Commonly under `assets/fonts`. 
5. **Create `_fonts.scss` file**: For adding the font-faces reference, I suggest using this cool website: [google webfonts helper](https://gwfh.mranftl.com/fonts) You can even download the `woff2` files from there so the links match already. You should end up with something like: 

```css
@font-face {
  font-display: swap; /* Check https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display for other options. */
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 400;
  src: url('../fonts/montserrat/montserrat-v26-latin-regular.woff2') format('woff2'); /* Chrome 36+, Opera 23+, Firefox 39+, Safari 12+, iOS 10+ */
}
```

6. **Update config.yaml**: You can now already call them from the configuration file like: 

```yaml
# _config.yml

  use_google_fonts: false
  google_fonts_url: ""
  use_self_hosted_fonts: true 
  heading: "Montserrat"
  base: "Open Sans"
  monospace: "Fira Mono"
  logo: "Montserrat"
```

7. **Call them from your styles.scss**: At this phase, you have multiple options for using them. We can just already call them or refer to the config variable. The important point is that after this they will always be available for your site as a self-hosted option. 

> [!important] Re-build
> Remember you need to `$jekyll build` or `$jekyll serve` your site in terminal after changing any of the config files. 

### 🔬 Sources

- [Step-by-Step Guide: How to Add Custom Fonts to Your Jekyll Theme | MoldStud](https://moldstud.com/articles/p-comprehensive-step-by-step-instructions-for-integrating-custom-fonts-into-your-jekyll-theme) :: Great article on the importance of typography in your blog and how to install fonts in jekyll. 
- [23 Best Fonts for Blogging to Make Your Blog Look Amazing • The SEO Kitchen](https://www.theseokitchen.com/best-fonts-for-blogging) :: List of best fonts for blogging. 
- [Theme Colors and Fonts](https://www.zerostatic.io/docs/jekyll-advance/config/theme-color-font/) Great tutorial for actually loading self-hosted fonts. 
