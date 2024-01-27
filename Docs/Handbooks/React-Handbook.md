# My React CheatSheet

## Good Tips

### setting state tips for arrays and objects
When working with useState and the variable is a vector, or an object, never change the vector/object directly on setState().
Make a copy of it inside the function, them do the logic and return the new vector. Otherwise your changes will not be rendered properly. If its being rendered, its because another function is triggering the render method of your component at the same time.
Example:

```
const [choices, setChoices] = useState(["a", "c", "e", "b"])

function switchChoice(index, choice){
  setChoices((oldChoices) => {
    let newChoices = [...oldChoices]
    newChoices[index] = choice
    return newChoices
  })
}
```
---

### Add a gitignore for node
```
npx gitignore node
```
---



[⬅️ BACK TO INDEX](../../#my-open-studies)
