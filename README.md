# resizable-iframe Without js
How can I make an iframe/Container resizable? 

### This can be done in pure CSS, like so:
```
iframe {
  height: 300px;
  width: 300px;
  resize: both;
  overflow: auto;
}
```
### Definition of resize property 
The resize property defines if (and how) an element is resizable by the user.
## $\colorbox{RED}{{\color{white}{Imoprtant Note}}}$
The resize property does not apply to inline elements or to block elements where overflow="visible". 
So, make sure that overflow is set to "scroll", "auto", or "hidden".
###   Important point
+ Default value:	none <br>
+ Inherited:	no<br>
+ Animatable:	no. Read about animatable<br>
+ Version:	CSS3<br>
+ JavaScript syntax:object.style.resize="both"

## But a few problems occur while resizing the iframe 
so we can remove it by adding flex properties 

   ```
<style>
    .resizer {
        display: flex;
        margin: 0;
        padding: 0;
        resize: both;
        transform: scale(3);
        overflow: auto;
        margin-bottom: auto;
    }
    .resizer>.resized{flex-grow: 1;}
    </style>
<body >
    <h1>iframe resizable</h1>
    <div class="resizer border" >
        <iframe class="resized" src="https://www.youtube.com/embed/AZBtUNzL450"></iframe>
    </div>
    </body>
   }
```
#  # Thanks for your time here.
