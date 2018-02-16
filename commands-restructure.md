---
title: "{{ replace .TranslationBaseName "-" " " | Commands Strstructure }}"
date: {{ .Date }}
anchor: "{{ replace .TranslationBaseName "-" " " | Commands Strstructure | urlize }}"
weight: 
---

# Restructuring Identification's Custom Commands
##### (In other words: Changing how commands are named, navigated, and displayed)


Short context: While trying to make an interactive help menu for all the custom commands the server has, I got to the point where I had to decide how to group and list the commands in a way where it'd be intuitive for someone to navigate such a menu. After some thought, I decided it might just be easier and more beneficial to simply  restructure the command list entirely. This not only solves the task of sorting the current commands, but also will make it very straightforward to integrate other commands in the future. 

---
### Here is what I came up with
##### Potential new structure
`?[category] {set | info} <value> (option)`

##### Logical example
`?[mbti] {set} (intj)`

##### Actual usage
`?mbti set intj`

---

### Further broken down & explained
*Brackets are only used as visual label*

`[Category]`
What topic does whatever youre wanting to do fall under?

`{Set | Info}`
Are you trying to set a role to your account, OR (`|`), Are you trying to get information about something?

`<Value>`
 What specific "thing" (`value`) do you want to set or get information about?

`(Option)`
In the case there iss extra pieces to this command (i.e.`1` -`8`), you can optionally specify which one.


##### Note:
- The request type portion `{set | info}` should be read as, `{set OR info}` As in,"This is either setting a role to my name, or is requesting information be shown"
- The `<value>` would be a mandatory input, whilst `(option)` would be optional.

---

### Clarification & Thoughts
It's hard for me to come up with why this would be a *bad* idea, but I am sure it could be a *better* one. Either way, here's some thoughts on it.

##### Pros: 
- Provides predictable structure, enabling more intuitive navigation
- Helps avoid confusing new users who have limited familiarity with typology
- New command sets can be added and organized with ease without convuluting help menu 

##### Cons:
- Longer command format may be harder to remember`*`
- Less familiarity for accustumed members who memorised current commands 
- Potentially less specific, since it adheres to "structure first, command name second"
 

*`*`debatable*
##### Final notes
I would thinking have a shorthand alternative to these would be ideal, though the above would represent main longform structure regardless. 
The current command list (`?cmd`) would **not** need to be disabled, though it would help in quickening the potentially confusing transition process imo.

---
