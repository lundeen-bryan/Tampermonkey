## Move Buttons To Right

In version 41.2020.4.16 go to line 405 and change the function called csleft from:
```html
csLeft = function(ii,a){a = -127 + 37 * (ii-1 - (ii >2 && !mainPg)); return design1612 || layout1811 ?{right: -a+33+'px'}:{left: a+'px'}}
```
To a the following
```html
  csLeft = function (ii, a) {
    a = -127 + 37 * (ii - 1 - (ii > 2 && !mainPg));
    return design1612 || layout1811
      ? { right: -a - 200 + "px" }
      : { left: a + "px" };
  },
```
Using prettier it will format the file to display better and this line becomes #642

## Moving it down a little to match search bar

Then look for the function isWHShown2 and change
```html
  cs: $x(
    {
      position: "absolute",
      top: startPg ? "40px" : "15px",
      wordSpacing: "-1px",
      visibility:
        ii < S.hiddenEdgeLeft || (startPg && ii == 2)
          ? "hidden"
          : "visible",
    },
```
