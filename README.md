# MegaBolD
Only the mega-bold objects can catch the people's attention.

[![GitHub license](https://img.shields.io/badge/license-GNU%20public-blue.svg)](https://github.com/sclass53/hexo-theme-megabold/blob/master/LICENSE)

MegaBolD is a powerful magazine theme for your [Hexo] site.

[**☞ Live Preview**](https://megabold.sclass53.jnrcs.org/)

![](https://sclass53.github.io/resources/megabold-shot.png)

<!--more-->

## Installation

 1. Get it from GitHub

 ```shell
 $ git clone https://github.com/sclass53/hexo-theme-megabold.git themes/megabold
 ```
 2. Enable

 Modify `theme` setting in `_config.yml` to `megabold`.
 ```
 ## Themes: http://hexo.io/themes/
 theme: megabold
 ```
 3. Update

 ```shell
 $ cd themes/megabold
 $ git pull
 ```


## Features: normal

### Logo: Image or Text

You can set a image as your logo instead of original text title. 
just enable `avatar` field in megabold/_config.yml.

```yml
# Put your avatar.jpg into `hexo-site/themes/megabold/source/` directory.
# url is target link (E.g. `url: https://hexo.io/logo.svg` or `url: css/images/mylogo.jpg`)
avatar: 
  enable: true
  width: 124
  height: 124
  bottom: 10
  url: https://hexo.io/logo.svg
```


### Code Highlight

MegaBolD use [Tomorrow Theme](https://github.com/chriskempson/tomorrow-theme) for your code block. We have six options in total: `default`, `normal`, `night`, `night blue`, `night bright`, `night eighties`

![code `default` theme Preview](https://raw.githubusercontent.com/sclass53/hexo-theme-megabold/master/source/preview/code-default-preview.png)

Above preview picture is default theme. the image below show other five Highlight themes.

![code themes](https://github.com/sclass53/hexo-theme-megabold/blob/master/source/preview/code-theme.jpg?raw=true)

Modify `highlight_theme` in megabold/_config.yml.

```yml
# Code Highlight theme
# Available value:
#    default | normal | night | night eighties | night blue | night bright
# https://github.com/chriskempson/tomorrow-theme
highlight_theme: default
```

### Background
MegaBolD supports configuring background images.
*Set image to **NEST** to use the geometric background.*

```yml
# Homepage bg
#-# Set image to "NEST" if you want to use the geometrical nest background
background:
  enable: True
  image: NEST
```

### Sidebar

You can put your sidebar in left side, right side or bottom of your site by editing `sidebar` setting.
MegaBolD provides 7 built-in widgets:

- search
- social
- recent_posts
- category
- tag
- tagcloud
- archive
- ads  (*please configure in the Beta widgets*)

Most of them are enabled by default. You can edit them in `widget` setting.


### Search

MegaBolD use `Insight Search` to help you search anything inside your site without any third-party plugin.

```yml
# Search
search:
    insight: true # you need to install `hexo-generator-json-content` before using Insight Search
    swiftype: # enter swiftype install key here
    baidu: false # you need to disable other search engines to use Baidu search, options: true, false
```

> Attention: You need to install `hexo-generator-json-content` before using Insight Search.

```bash
$ npm install -S hexo-generator-json-content
```


### Fancybox

MegaBolD uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)

{% fancybox img_url [img_thumbnail] [img_caption] %}
```



### Donate Button

Support **QR Code** for donation, Modify the following snippets to MegaBol `MegaBold/_config.yml`:


```yml
# donation button
donate:
    enable: true
    message: '如果觉得我的文章对您有用，请随意打赏。您的支持将鼓励我继续创作!'
    wechatImage: https://your_WECHAT_PAY_ImageUrl
    alipayImage: https://your_ALIPAY_ImageUrl
```

### Comment support

MegaBolD has support for DuoShuo,Disqus,Valine,etc. comment systems. Modify the following snippets to MegaBolD `,megabold/_config.yml`:

EX:
```yml
# comment ShortName, you can choose only ONE to display.
duoshuo_shortname: sclass53
disqus_shortname: 
```

## Features: Beta
>NOTE
 All Beta features are in test!!!
including:

### Bottom link table
config the `children:` in the _config.yml to setup the table
```yml
# BOTTOM MENU
# * display menu at the bottom of index pages (pagination == 2)
## *  only supports double layer
menu_bottom_width: 200px
menu_bottom_enable: true
menu_bottom:
  - Links:
    _title: Links 
    children:
      - Home: 
        _: Home
        lnk:

      - About: 
        _: About
        lnk: /about/

  - Commerce:
    _title: Commercial
    children:
      - Shop: 
        _: Online Shop
        lnk: /shop/

      - Blog: 
        _: Blog
        lnk: /blog/

```

### Google Adsense
```yml
# Google Adsense
## header
adsense:
  enable: True
  id: ca-pub-7436530442292220
```

## Contributing

All kinds of contributions (enhancements, new features, documentation & code improvements, issues & bugs reporting) are welcome.

Looking forward to your pull request.


## License

MegaBolD is under the GNU general public license (3.0). See the [LICENSE](https://github.com/sclass53/hexo-theme-megabold/blob/master/LICENSE) file for details.


[Hexo]: https://hexo.io/
[Fancybox]: http://fancyapps.com/fancybox/
[Font Awesome]: http://fontawesome.io/
