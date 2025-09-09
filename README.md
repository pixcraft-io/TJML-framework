# TJML email framework
It is an email framework that enables quick and convenient creation of cross-platform AMP and HTML emails with the help of TJML — an xml-like markup language.

[Documentation](https://docs.pixcraft.io/en/tjml/)

## Why TJML framework?
* HTML and AMP versions of the email are automatically generated from TJML code
* Layout development is, on average, twice as fast compared to traditional manual methods;
* Lowers the entry barrier to email development: no need to learn all the quirks of coding for Outlook, mobile email clients, etc. The framework ensures proper rendering in most email clients—both legacy and modern
* Emails adapt correctly to mobile devices, even those without media query support
* Emails render properly in both modern email clients and outdated ones like Microsoft Outlook (2003–2020) and Lotus Mail.
 
### Additional Tools Available in the TJML framework Interface
* Dark mode display check
* Code minification
* Mobile view preview
* Pixel Perfect tool
* HTML file size calculation and warnings if it exceeds recommended limits
* One-click email screenshot generation

### TJML
TJML was build using Vue framework; each tag in it is a Vue component. To create an email, you need to add our JavaScript to your HTML file. Before sending, you should export the rendered HTML or AMP version of the email you created. As you export, each component will be transformed into regular email HTML.

### Autocomplete
| IDE | Description                                                                                                                                                                                                          |
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| JetBrains IDEs (WebStorm, PhpStorm) | You can use <a href="https://app.pixcraft.io/tjml/web-types.json">web-types</a> for autocomplete TJML tags and attributes. Or use <a href="https://app.pixcraft.io/tjml/startpack.zip">start pack</a> for fast dive. |
| Visual Studio Code | [Install plugin from Marketplace](https://marketplace.visualstudio.com/items?itemName=Pixcraft.vscode-tjml) or [github](https://github.com/pixcraft-io/vscode-tjml)                                                  |

## Getting started
Insert the following JavaScript code immediately after the `<body>` tag:
```
<script type="text/javascript">
var s=document.createElement("script"),l=document.createElement("link"),d=new Date;s.setAttribute("src","https://app.pixcraft.io/tjml/app.js?ver="+d.getTime()),l.setAttribute("type","text/css"),l.setAttribute("rel","stylesheet"),l.setAttribute("href","https://app.pixcraft.io/tjml/app.css?ver="+d.getTime()),document.head.appendChild(l),document.body.appendChild(s); 
</script>
```

### Email Structure
You need to stick to the following structure of the document:
You can insert any TJML or email HTML code between the `<m-body>` and  `</m-body>`  tags. 
Please note that regular email HTML code will not allow for the creation of an AMP version of the email.
```
<tjml>
    <m-body>
        <!-- some TJML code -->
    </m-body>
</tjml>
```
## Tags and Attributes
You can find detailed information about all the available tags (components) and attributes in the <a href="https://docs.pixcraft.io/framework/">TJML docs</a> and <a href="https://github.com/pixcraft-io/TJML-framework/wiki">wiki</a>. 
