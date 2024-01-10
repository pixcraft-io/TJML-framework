# ampier email framework
It is an email framework that enables quick and convenient creation of cross-platform AMP and HTML emails with the help of TJML — an xml-like markup language.

### Email Coding Optimization with Ampier
* automated HTML and AMP email creation from TJML code,
* 50% faster HTML coding, as compared to regular email HTML coding,
* looser skill requirements for frontend developers and HTML coders,
* emails that respond correctly and immediately to screen size change, **including the cases when media queries are not used**,
* emails that are displayed properly in Microsoft Outlook (2003-2020), as well as in outdated email clients, such as Lotus mail.
 
### Additional Tools Available in the Ampier Email Interface
* dark mode check,
* code compression,
* responsive design preview,
* pixelPerfect tool,
* rendered HTML file size calculation,
* single-click screenshot of the designed email.

### TJML
TJML was build using Vue framework; each tag in it is a Vue component. To create an email, you need to add our JavaScript to your HTML file. Before sending, you should export the rendered HTML or AMP version of the email you created. As you export, each component will be transformed into regular email HTML.

### Autocomplete
| IDE | Description |
|-----| ----------- |
| JetBrains IDEs (WebStorm, PhpStorm) | You can use <a href="https://ampier.io/tjml/web-types.json">web-types</a> for autocomplete TJML tags and attributes. Or use <a href="https://ampier.io/tjml/startpack.zip">start pack</a> for fast dive. |
| Visual Studio Code | [Install plugin from Marketplace](https://marketplace.visualstudio.com/items?itemName=Ampier.vscode-ampier) or [github](https://github.com/ampier-io/vscode-ampier) |

## Enabling Ampier Framework
Insert the following JavaScript code immediately after the `<body>` tag:
```
<script type="text/javascript">
var s=document.createElement("script"),l=document.createElement("link"),d=new Date;s.setAttribute("src","https://ampier.io/tjml/app.js?ver="+d.getTime()),l.setAttribute("type","text/css"),l.setAttribute("rel","stylesheet"),l.setAttribute("href","https://ampier.io/tjml/app.css?ver="+d.getTime()),document.head.appendChild(l),document.body.appendChild(s); 
</script>
```

### Email Structure
You need to stick to the following structure of the document:
You can insert any TJML or email HTML code between the `<m-body>` and  `</m-body>`  tags. 
Please note that regular email HTML code will not allow for the creation of an AMP version of the email.
```
<div id="app">
<tj-ui>
    <m-body>
        <!-- some TJML code -->
    </m-body>
</tj-ui>
</div>
```
## Tags and Attributes
You can find detailed information about all the available tags (components) and attributes in the <a href="https://docs.ampier.io/framework/">Ampier docs</a> and <a href="https://github.com/ampier-io/ampier-framework/wiki">wiki</a>. 
