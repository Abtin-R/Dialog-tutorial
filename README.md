# Dialog tag   

The ```<dialog>``` tag is an HTML element used to easily create popup dialogs or modals.

## Dialog HTML
You will want to use a ```<dialog>```in the ```<body>``` with a class called dialog inside you can include the dialog has a built in close feature with the "esc" key.
```html
       <dialog class="dialog">
                <h2>Dialog</h2>  
        </dialog>
 
```

## Dialog CSS

We will add basic styling to ```<dialog>``` we can use the ```dialog[open]```to added transitions when the dialog opens otherwise you would style it like a normal div.
```css

.dialog {

    margin: auto;
    width: 337px;
    height: 150px;
    border-radius: 6px;
    text-align: center;
    box-shadow: 2px 2px 4px rgb(0 0 0 / .1);
}

.dialog::backdrop {
    background-color: rgb(0 0 0 / .45);
}

dialog[open] {
    animation:  appear 2s ease-in-out;
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(-20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
   
    }
}

dialog h2 {
    line-height: 150px;
    font-size: 26px;
    font-weight: 700;
}

```

## Dialog Javascript
all you need to do is to select your dialog and use ```.showModal()``` for it to appear and then your done.

```javascript
"use strict"

const dialog = document.querySelector(".dialog")

window.onload = () => {
    dialog.showModal();
}
```

### Resources
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [W3schools](https://www.w3schools.com/tags/tag_dialog.asp)
- [CSS-Tricks](https://css-tricks.com/some-hands-on-with-the-html-dialog-element/s)