
Rolls dice (or lets you roll your own) and returns a stylized move callout
__
```
^move (.*) ([_a-zA-Z]*) (10|[0-9]) (10|[0-9]) ?([_0-9,]*)$
```
__
```js
var moveName = $1;
var statName = $2;
var statValue = Number($3);
var addValue = Number($4);

let d10A = Math.floor(Math.random() * 10) + 1;
let d10B = Math.floor(Math.random() * 10) + 1;
let d6 = Math.floor(Math.random() * 6) + 1;

console.log("am i running?");
console.log(moveName);

if (!$5) {
	console.log("$5 is blank");
} else {
	const myArray = $5.split(",");
	d6 = Number(myArray[0]);
	d10A = Number(myArray[1]);
	d10B = Number(myArray[2]);
} 

console.log("d6: "+d6);
console.log("d10a: "+d10A);
console.log("d10b: "+d10B);
console.log("statvalue: "+statValue);
console.log("addvalue: "+addValue);


var actionRoll = d6+statValue+addValue;
console.log("actionroll (d6+stat+add): "+actionRoll);

if (actionRoll > 10) {actionRoll = 10;}
var result = "";
var image = "";
let calloutType = "> [!fail]+";

if (actionRoll > d10A && actionRoll > d10B) {
	result = "Strong Hit";
    calloutType = "> [!success]-";
    image = "![[outcome-strong-hit.svg|50]]";
    if (d10A == d10B) {
        result = result + " with a MATCH!";
    }
} else if (actionRoll > d10A || actionRoll > d10B) {
    result = "Weak Hit";
    calloutType = "> [!caution]-";
    image = "![[outcome-weak-hit.svg|50]]";
    if (d10A == d10B) {
        result = result + " with a MATCH!";
    }
} else {
    result = "Miss";
    calloutType = "> [!fail]-";
    image = "![[outcome-miss.svg|50]]";
    if (d10A == d10B) {
        result = result + " with a MATCH!";
    }
}
let calloutTitle = calloutType + " " + moveName + ": " + statName + " + " + addValue;
let actionResult = "\n> ![[d6-" + d6 + "-t.svg#invert_W|50]]![[plus-t.svg#invert_W|15]]![[stat-" + statValue + "-t.svg#invert_W|50]]![[plus-t.svg#invert_W|15]]![[add-" + addValue + "-t.svg#invert_W|50]]![[equals-t.svg#invert_W|15]]![[total-" + actionRoll + "-t.svg#invert_W|50]]";
let challengeResult = "\n> ![[vs-t.svg#invert_W|50]]![[d10-" + d10A + "-t.svg#invert_W|50]]![[and-t.svg#invert_W|50]]![[d10-" + d10B + "-t.svg#invert_W|50]]";
let outcome = "\n> ### Result: " + image + " " + result;
let resultCallout = calloutTitle + actionResult + challengeResult + outcome + "\n\n";
return resultCallout;
```
__
move {move name} {stat/asset name} {stat value} {add value} {optional: rollyourown: d6,d10,d10, default: null} - Rolls the selected move and returns a stylized move callout
__
^ptp$
__
```js
// Get the diceroller plugin (or exit if not available)
const diceRollerPlugin = app.plugins.getPlugin("obsidian-dice-roller");
if (!diceRollerPlugin)
{
	return expText("Command not run.  Dice Roller plugin not available.");
}

// Roll the command parameter with the plugin
const diceRoller = await diceRollerPlugin.getRoller("[[ptp#^paytheprice]]");
result = await diceRoller.roll(true);


return (
	"> [!tip] Pay the Price:  *"+result+"*"+"\n\n"
);
```
__
ptp - rolls on the pay the price table