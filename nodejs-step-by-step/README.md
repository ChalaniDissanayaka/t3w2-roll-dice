# NodeJS Project Step By Step

## NodeJS Project Step-by-step

Carry out the following steps on your own computer. There are no tests for this challenge - make sure you can achieve each step listed below!

There is no code template for this challenge and we do NOT recommend attempting this challenge on Ed. Instead, this challenge is provided on Ed to show a solution if you choose to look through that.

Please work through this challenge on your own computer.

- Create a new directory named `nodejs-step-by-step` and open that in your code editor.

- Run the commands explained throughout this lesson's previous pages to initialize an NPM project (creating a `package.json` file!). Accepting default values for any prompts that appear will be fine.

- Create a file named `app.js` and place it in the root of your project.

- Add this code to your `app.js` file:

```
const dice = require("./dice");

console.log(`The dice will roll ${process.env.ROLL_COUNT} times!`);

for (let index = 0; index < process.env.ROLL_COUNT; index++) {
    console.log(dice.rollDice(20));

}
```

- Create a file named `dice.js` and place it in the root of your project.
- Add this code to your `dice.js` file:

```
function rollDice(maxNumber){
    return Math.ceil(Math.random() * maxNumber);
}

module.exports = {
    rollDice
}
```

- `Confirm` that your project works so far by running this command in your terminal: `ROLL_COUNT=2 node app.js`

- Create a new script command in your project's `package.json` file named `roll-twice` and give it the command value used in the previous step.

- Confirm that the new command works by running `npm run roll-twice` - once that works, this challenge is done!

//------------------- EX Code -----------------------------------
create directory named `nodejs-step-by-step`

inside that directory create -

1. `dice.js - file`

```
function rollDice(maxNumber){
    return Math.ceil(Math.random() * maxNumber);
}

module.exports = {
    rollDice
}
```

2. `app.js - file`

```
const dice = require("./dice");

console.log(`The dice will roll ${process.env.ROLL_COUNT} times!`);

for (let index = 0; index < process.env.ROLL_COUNT; index++) {
    console.log(dice.rollDice(20));

}
```

3. create `package.json` file

```
{
  "name": "nodejs-step-by-step",
  "version": "1.0.0",
  "description": "",
  "main": "app.js",
  "scripts": {
    "roll-twice": "ROLL_COUNT=2 node app.js"
  },
  "author": "Chalani",
  "license": "ISC"
}
```

4. create `package-lock.json` file

```
{
  "name": "nodejs-step-by-step",
  "version": "1.0.0",
  "lockfileVersion": 3,
  "requires": true,
  "packages": {
    "": {
      "name": "nodejs-step-by-step",
      "version": "1.0.0",
      "license": "ISC"
    }
  }
}
```

//------------------- EX Code end -----------------------------------

5. To RUN this app :-

1. command : `npm install` then created `package-lock.json`
1. command : `npm run roll-twice`
