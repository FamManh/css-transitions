## Animation
- Transition property will change from initial state for the final state
- Duration

```css
button{
    padding: 30px 60px;
    background-color: blue;
    border: 0;
    color: white;
    transition-property: background-color;
    transition-duration: 500ms;
}

button:hover{
    background-color: green;
}

```

- transition-timing-function
- transition-delay

## animation
### animation-fill-mode: 
- none: default băt đầu animation từ style
- backwards: bắt đầu animation từ frame đầu tiên, kết thúc animation thì bac về đầu
- forwards: giữ nguyên vị trí khi animation kết thúc
- both: bắt đầu từ frame đầu tiền, kết thúc giữ nguyên vị trí
### animation-iteration-count:
- number: số lần thực hiện animation
- infinite: lặp vô tận
### animation-timing-function:
- ease
- ease-in bắt đầu chập
- ease-out kết thúc chập
- ease-in-out bắt đầu chập, giữa bình thường, kết thúc chậm
- ...

### animation-direction:
- alternate: thực hiện animation lặp lại khi set animation-iteration-count 
- alternate-reverse: 
- reverse

```css
div{
    width: 150px;
    height: 150px;
    background-color: red;
    animation-name: moving;
    animation-duration: 3s;
    animation-fill-mode: both;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate;
}

@keyframes moving {
    0% {
        transform: translateX(250px);
    }
    50%{
        transform: translateX(500px);
        background-color: green;
    }
    100%{
        transform: translateX(500px) translateY(500px);
        background-color: blue;
    }
```