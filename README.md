# hexo-reading-time
[Hexo](https://hexo.io/) plugin that displays reading time for the article.

## Installation

```
npm install --save hexo-reading-time
```

## Usage
### Basic Usage

To display reading time, add the function into `post.ejs`.

Ejs:
```
<%- readingTime(page.content) %>
```
Swig:
```
{{ readingTime(page.content) }}
```
Jade:
```
span= readingTime(page.content)
```

It will display `X min. read`.

### Customization

You can cutomize the output by passing additional arguments.

Ejs:
```
<%- readingTime(page.content, 'min.', wordsperminute) %>
```
Swig:
```
{{ readingTime(page.content, 'min.', wordsperminute) }}
```
Jade:
```
span= readingTime(page.content, 'min.', wordsperminute)
```

where:  
 `'min.'` - second argument - any string that represents suffx. Default is 'min. read'  
 `wpm` - number  - words per minute. Default is 150.  
 Both arguments are optional.  

## License
MIT
