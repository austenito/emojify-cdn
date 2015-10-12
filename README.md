# emojify-cdn.js

A Javascript module to convert emoji keywords to images via a CDN. The emoji keywords are as described by [emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com). This library has no dependencies to work with whatever javascript framework you use (jquery, prototype, etc).

The majority of this project's code is taken from [emojify.js](http://hassankhan.github.com/emojify.js).

## Usage
Add the required lines to the ``<head>`` part of your HTML code:

```
  <script src="emojify-cdn.js"></script>
```

Now type in an emoji keyword in your HTML, for example ``:smile:``
Now run emojify using ``emojify.run()``.
To exclude tags from being emojified, add ``no-emojify`` to their ``class`` attributes.

You can optionally pass an object to ``emojify.run()`` to restrict the **emojification** to that object only: ``emojify.run(document.getElementById('my-element'))``

### Configuration
To set configuration options, use `emojify.setConfig()` and a JSON object as a parameter with the following attributes:
* ``emojify_tag_type``: Set to `<img>` by default. Sets the element the emojify.js uses to replace emoji keywords


### Code Example

    emojify.setConfig({
      emojify_tag_type: 'img',
      cdn_host: "http://tortue.me/emoji',
      emoji_image_extension: 'png',
      emoticons_enabled: true,
      people_enabled: true,
      nature_enabled: true,
      objects_enabled: true,
      places_enabled: true,
      symbols_enabled: true
    });
    emojify.run();
    
*Note*: All emoji are enabled by default.

## Default CDN

Emoji can be used by this library or hotlinked from [http://tortue.me](http://tortue.me). The CDN is provided for free by [Cloudflare](http://www.cloudflare.com).

For example: If you want to see a :turtle: , visit http://tortue.me/emoji/turtle.png

## License

Copyright 2013 Austen Ito

Licensed under the MIT License
