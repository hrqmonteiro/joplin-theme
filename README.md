<p align="center">
  <img width="15%" src="https://raw.githubusercontent.com/laurent22/joplin/master/Assets/LinuxIcons/256x256.png" />
</p>

<p align="center">
<b>My personal <i>userchrome.css</i> and <i>userstyles.css</i> for <a href="https://joplinapp.org" target="blank">Joplin</a>.</b>
  
Built upon <a href="https://github.com/amandamcg/joplin-theme" target="blank">Amanda's</a> theme (thanks for help on the forum!) and highly inspired by the <a href="https://culturedcode.com/things/" target="blank">Things 3 app</a> for Mac/iOS as well as some details i liked myself, and specially built to support my daily GTD (Getting Things Done) workflow. Some details about my setup below.
</p>

![screenshot1.png](/assets/screenshot1.png)

## Details: 

This is the resources i added to my theme. The [setup](#setup) section will guide you on how to install it.

* Dark theme: based on the default Joplin dark theme and, as stated before, on Amanda's theme.
* Colorscheme: i call it **Neptune**, i use it on many things on my setup (Linux rice, Vim colors, and other applications).
* Custom CSS for the app interface and markdown editor (*userchrome.css*) and for the rendered notes (*userstyles.css*)
* Support for icons ([FontAwesome](https://fontawesome.com) and [Material Design Icons](https://materialdesignicons.com/).
* Other stuff i modified/added: 
   * Colored icons on sidebar (based on the *Things 3* app); 
   * Capitalized tags (also support for icons in tags);
   * Colored tables, glyphs and text on rendered notes;
   * Custom symbol for checklists.
   
## Setup:

Following are the instructions if you want to replicate my theme, and the things you need to make it work.

1. You need two fonts with the FontAwesome and Material Icons glyphs, one *sans-serif* and one *monospaced*. The sans i use in all the titles and pretty much the rest of the theme, and the monospaced is used, obviously, on the markdown editor. You can get fonts patched with both glyphs (and more) using *any* of the [https://github.com/ryanoasis/nerd-fonts/](Nerd Fonts) or you can patch your own. I patched mine (I use Google Sans as sans and Roboto Mono as monospaced).

2. Download the files. Open *userchrome.css* and *userstyles.css* and edit the fonts, replacing for the font family of the ones you are going to use.

3. Copy *userchrome.css* and *userstyles.css* to your `joplin-desktop`folder (on Linux, it is located in `~/.config/joplin-desktop`), on Windows you can check the location clicking on `Tools > Options > General` and reading it on the first line.

4. Don't forget to make sure you are using the Dark theme for Joplin. In case you are not, set it clicking on `Tools > Options > Appearance` and select Dark in the *Theme* dropdown menu.

5. Done! The theme is set up.

## Usage:

### Icons:

* The colored icons on sidebar: This is a very (kinda messy) workaround that works for *me*, on my *setup*, and i was able to "implement" this setting some classes using the parameters `:after` and `before` on the *userchrome.css*, so when you open your Joplin, it will have these icons floating on your sidebar. 
Yu can find it on the following section:

```
/* Colored icons on the sidebar */  
.list-item div:before {  
    font-family: var(--font-sans) !important;  
    font-size: 16px !important;  
    content: '';  
    position: absolute;  
    left: 33px; top: 129px;  
    width: 20px;  
    color: var(--yellow);  
}   
[ ...]  
/* Colored icons ENDS HERE */
```  
So if you are not going to use it, you can remove or comment out the entire section. If you are going to use it, adjust the glyps, colors and position for every one of them (i know, it is a lot of work, but i found it worth it to set to have this setup 🙂)

* FontAwesome and/or Material Icons on sidebar, notebook titles, note titles, notes body, tags, and so on:

You need to get your icons from the cheatsheet, you can find it on Nerd font's website [here](https://www.nerdfonts.com/cheat-sheet). Just search some icon you would want to use it (or navigate through it), copy it and paste it on Joplin. Tip: i keep some of which i most use on a note inside my Joplin, for future use, it is easier.

## Screenshots:

### Notebooks section
![screenshot2.png](/assets/screenshot2.png)

### Notes section
![screenshot3.png](/assets/screenshot3.png)

### Rendered markdown
![screenshot4.png](/assets/screenshot4.png)

### Custom checkboxes
![screenshot5.png](/assets/screenshot5.png)
![screenshot6.png](/assets/screenshot6.png)  
![screenshot7.png](/assets/screenshot7.png)
![screenshot8.png](/assets/screenshot8.png)

You can set it on *userchrome.css*, just replace the glyphs for anyone you like it from FontAwesome or Material Icons.
