# commonjs html prettyprinter

A commonjs port of beautify-html.js by Nochum Sossonko which is based on jsbeautifier by Einar Lielmanis

## Installation

### from npm (node package manager)
``` bash
  npm install html
```

## Usage (command line)

```
  echo "<h2><strong><a href="http://awesome.com">AwesomeCom</a></strong><span>is awesome</span></h2>" | html
```

returns:
  
``` html  
  <h2>
      <strong>
          <a href=http://awesome.com>AwesomeCom</a>
      </strong>
      <span>
          is awesome
      </span>
  </h2>
````

## Advanced usage

I find myself constantly using the 'Copy as HTML' feature of the Chrome Inspector:

![Copy as HTML](https://github.com/maxogden/commonjs-html-prettyprinter/raw/master/img/copyashtml.png)

The downside is that that usually the HTML that gets copied is pretty ugly:

![Before pretty printing](https://github.com/maxogden/commonjs-html-prettyprinter/raw/master/img/before.png)

On OS X you can use `pbpaste` and `pbcopy` to stream your clipboard in and out of unix pipes. With the ugly HTML still in your clipboard run this command:

`pbpaste | html | pbcopy`

Now when you paste your clipboard into an editor you will get nice, pretty printed HTML:

![After pretty printing](https://github.com/maxogden/commonjs-html-prettyprinter/raw/master/img/after.png)
