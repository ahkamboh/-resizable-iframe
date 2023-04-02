# -resizable-iframe
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
## But a few problems occur while resizing the iframe 
so we can remove it by adding flex properties 
```
    .resizer {
        display: flex;
        margin: 0;
        padding: 0;
        resize: both;
        transform: scale(3);
        overflow: auto;
        margin-bottom: auto;
    }

    .resizer>.resized {
        flex-grow: 1;
        margin: 0;
        padding: 0;
        border: 0;

    }

    .border {
        background: rgb(23, 21, 21);
        border: 1px solid rgb(255, 255, 255);
    }

    h1 {
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        color: white;
        text-transform: capitalize;
        position: relative;
        top: 19%;
    }
</style>
<body >
    <h1>iframe resizable</h1>
    <div class="resizer border" >
        <iframe class="resized" src="https://www.youtube.com/embed/AZBtUNzL450"></iframe>
    </div>
    ```
