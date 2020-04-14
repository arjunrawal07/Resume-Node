# Arjun-Resume-npm

## How To Install 

To Install:
1. Fork and Clone this repository.
2. Change into the new directory.
3. In your terminal, run the following command:

    ```npm i arjunrawal-resume```

4. Change into the directory titled Resume Node. The info.json file contains the resume information. 

5. In your terminal, run the following from your command line:
    ```node index.js```
    
6. Voila! You now have my resume printed in your terminal.

## What is this?

Hi! I'm Arjun Rawal, and I wrote a version of my resume that you can install onto your own computer via the command line interface!

### How did I do this?

Step 1. Initialize the npm package to create a package.json file.

Step 2. Create three files (index.js, readme.md, and info.json) in the new directory.

Step 3. Add the following code to the first line of index.js :

`#! /usr/bin/env node`

This allows us to run the code globally as well as from the command line.

Step 4. This part is key. It allows you to access the file system (`fs`), which is a pre-defined pacakge within the npm node. `fs` has many pre-defined functions that come with it. We will use the `fs.readFile()` function to "read" the info.json that contains the resume information.

```
const fs = require('fs')

fs.readFile(__dirname + '/info.json', 'utf8', function(err, data) {
    if (err) {
        console.log(err)
    } else {
        console.log(data)
        return data
    }
})
```

Step 5. Then add the following to your package.json file:

```"bin": {
    "your-command-here": "./index.js"
  },

```

Step 6. Write the resume in the info.json file!
