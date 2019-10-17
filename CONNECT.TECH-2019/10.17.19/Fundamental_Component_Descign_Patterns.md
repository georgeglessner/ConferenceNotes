# Fundamental Component Design Patterns
> Ben Hong


Full slide deck - @bencodezen Twitter

The hardest decision is deciding what to make a component and what not to. 

Why componenets? 
- build faster
- no more repetitive code
- less bugs, means you can relax

Technique - props
- should be object format
- define type, required, default, etc

Better alternative to props -> slots

Use slots for:
- content distribution
- creating larger components by combining smaller componenets
- Default content in multi-page apps
- provide a wrapper
- applying custom formatting/template to fragments of a component

Slots > Props

Composition > Configuration


Composition API -> bit.ly/compositionapi