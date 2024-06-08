---
toc: false
---
## The Code is Not the Text: Generator
```js echo
const unless = "unless", is = "is",
reallyIsNot = "it is not", flipForIt = (oneOr, theOther) =>
((Math.random() * 2) | 0) == 0 ? oneOr : theOther
let lastCriticalStatement =
"the code is not the text unless it is the text",
newCriticalStatement = "",
myCriticalCodeStudy = [lastCriticalStatement]
while (myCriticalCodeStudy.length < 101) {
let theCode = flipForIt("the code", "the text"),
isNot = "is not",
theText = flipForIt("the text", "the code"),
itIs = "it is"
if (theCode == theText) {
isNot = flipForIt(isNot, is)
itIs = isNot == is ? reallyIsNot : itIs }
newCriticalStatement =
`${theCode} ${isNot} ${theText} ${unless} ${itIs} ${theText}`
if (newCriticalStatement != lastCriticalStatement) {
myCriticalCodeStudy.push(newCriticalStatement)
lastCriticalStatement = newCriticalStatement } }
```
The code above generates an `array` of statements in `myCriticalCodeStudy`. The statements are displayed below, joined by ‘ and ’. Refreshing the page regenerates the study.
<p>${myCriticalCodeStudy.join(" and ")}</p>