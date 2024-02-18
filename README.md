# Projects related to DOM

## project link
[Click here](https://stackblitz.com/edit/dom-project-chaiaurcode?file=index.html)

# Solution code

## project 1 Color Changer

```javascript
File: index.js
01: const buttons = document.querySelectorAll('.button');
02: const body = document.querySelector('body');
03: 
04: buttons.forEach(function(button) {
05:     console.log(button);
06:     button.addEventListener('click', function(e){
07:         console.log(e);
08:         console.log(e.target);
09:         if(e.target.id === 'grey'){
10:             body.style.backgroundColor = e.target.id
11:         } 
12:         if(e.target.id === 'white'){
13:             body.style.backgroundColor = e.target.id
14:         } 
15:         if(e.target.id === 'blue'){
16:             body.style.backgroundColor = e.target.id
17:         } 
18:         if(e.target.id === 'yellow'){
19:             body.style.backgroundColor = e.target.id
20:         } 
21: 
22:     })
23: });
```

## project 2 - BMI Calculator
```javascript
const form = document.querySelector("form");

form.addEventListener("submit", function (e) {
  e.preventDefault();
  const height = parseInt(document.querySelector("#height").value);
  const weight = parseInt(document.querySelector("#weight").value);
  const results = document.querySelector("#results");

  if (height === "" || height < 0 || isNaN(height)) {
    results.innerHTML = `Please give a valid height: ${height}`;
  } else if (weight === "" || weight < 0 || isNaN(weight)) {
    results.innerHTML = `Please give a valid weight: ${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    //show the result
    results.innerHTML = `<span>${bmi}</span>`;
  }
});
```



