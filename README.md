# Welcome to Stackedit+ theme!

I have modified Typora default theme  `github.css`,  so that it looks like StackEdit!

> This theme is a pure `css` file and does **NOT** contain any font files, all fonts are source from your **local** machine. Make sure these fonts are installed:
>
> - **Lato** font family
> - **Fira Code** font family

## How to Install

**Step 1.** Copy `stackedit+.css` into your Typora theme folder.

**Step 2.** Restart Typora, select 'Stackedit+' and enjoy.

> Can't find Typora them folder?
>
> Try: `Open menu -> Preferences... -> Appearance -> Open Theme Folder`


## Theme Implementation Trick
Use `@font-face` rule in CSS to overwrite font (of certain family/style/weight) into whatever you specify in the `src` property.

```css
/* overwrite Lato with Lato Black in bold weight, font style is retrieved from local file, make sure you have Lato fonts installed. */
@font-face {
    font-family: Lato;
    font-style: normal;
    font-weight: bold;
    src: local('Lato Black'), local('Lato-Black')
}

@font-face {
    font-family: Lato;
    font-style: italic;
    font-weight: bold;
    src: local('Lato Black Italic'), local('Lato-BlackItalic')
}
```

## References

- [CSS Fonts Module Level 3 (w3.org): Font Matching Algorithm](https://www.w3.org/TR/css-fonts-3/#font-matching-algorithm)
- [CSS Fonts Module Level 3 (w3.org): The `@font-face` Rule](https://www.w3.org/TR/css-fonts-3/#font-face-rule)
