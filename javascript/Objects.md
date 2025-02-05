Objects possuem por padrão prototypes então há o perigo de na hora que formos criar uma chave a mesma conflitar devido a isso, mas há um método que pode ser utilizado para ignorar isso que é a `.create`:
```
const person = {
  isHuman: false,
  printIntroduction: function () {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  },
};

const me = Object.create(person);

me.name = 'Matthew'; // "name" é uma propriedade de "me" mas não de "person"
me.isHuman = true; // propriedades herdadas podem ser sobrescritas
```