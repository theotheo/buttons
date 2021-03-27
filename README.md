# Obsidian Buttons

Run commands and open links by clicking on ✨ Buttons ✨

## Manual Install

Grab the [laest release](https://github.com/shabegom/buttons/releases) and add it to: <vault>/.obsidian/plugins/

## Usage

Buttons have 4 arguments: name, type, action, color

| argument | description                                | options                                      | example    |
-----------|--------------------------------------------|----------------------------------------------|------------|
| name        | the name of the button                                          | any string                                  | My Button  |
| type        | run a command or open a url                                     | command, link                               | command    |
| action      | the command to run or link to open                              | any command from the command palette or url | Toggle Pin |
| color       | optional: arg to change color of the button                     | blue, green, red, purple. yellow            | blue       |
| customClass | optional: add a class to the button for more customized styling | a string representing your custom class     | myClass    |
| customId    | optional: add a custom id to the button for styling             | a string representing your custom id        | myId       |


You create a button using a `button` codeblock

## Examples

### Command Button

Command buttons can run commands you would find in the Command Paletter. `type` will be _command_ and `action` is the exact wording of the command found in the palette.

\`\`\`button  
name My Awesome Button  
type command  
action Toggle Pin  
color blue  
\`\`\`

### Link Button

A Link Button will open the specified link in your web browser. `type` will be _link_ and `action` is the link you want to open (https:// is required)

\`\`\`button  
name My Link Button  
type link  
action https://booked.email  
\`\`\`

### Custom Class & ID

You can add an optional `customClass` argument to target the button with any css styling tweaks you'd want to add

\`\`\`button  
name My Round Link Button  
type link  
action https://booked.email  
customClass roundButton
customId myId
\`\`\`

then in your css tweaks:

```
.roundButton {
 border-radius: 100% !important;
}

#myId {
 color: rebeccapurple;
}
```

use `!important` to override any existing styling from `.default-button`
