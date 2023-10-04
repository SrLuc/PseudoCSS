# PseudoCSS

### This repository contains examples of how to use CSS to add functionality and style to your websites and applications.

#### The repository contains the following examples:

**Pseudo classes:** Examples of how to use pseudo classes to select elements based on their state or behavior.

**Transitions:** Examples of how to use animations and transitions to make web elements move or change over time.
Form customization: Examples of how to use CSS to customize HTML forms.

**Preprocessors**: Examples of how to use CSS preprocessors to write CSS in a more concise and organized way.
How to use

## To use the examples, simply copy and paste the CSS code into your own project.

### Pseudo Classes

Pseudo Classes are subclasses that can change an HTML element based on its state

- hover : Selects an element when the mouse is over it

```css
button:hover {
  background-color: #f44336;
  color: white;
  border: none;
}
```

- focus : Selects an element when it has keyboard focus.

```css
input:focus {
  background-color: #f44336;
  color: white;
  border: none;
}
```

- active : Selects an element when it is being clicked

```css
p:active {
  background-color: #f44336;
  color: white;
  border: none;
}
```

### Transitions

CSS transitions are used to create smoother visual effects. They can be used to make web elements change size, color or position over time.

- transition

```css
button:hover {
  transition: all 0.2s ease-in-out;
  background-color: green;
  color: white;
}
```

### Preprocessors

CSS preprocessors are tools that allow you to write CSS in a more concise and organized way.
They often provide additional features such as mixins, variables and nesting.

To use SASS which is a CSS Preprocessor, follow these steps:

- Download the Extension Name: Live Sass Compiler
- Create a folder called 'css' in the root of your project
- Create a file called _index.scss_
- Click the **Watch SaSS** icon at the bottom of your Visual Studio Code information bar

After following these 4 Steps, Visual Studio Code will create two files with the _.css_ extension.

The name of the files will be the same as the name of the file you created later, in this case, the file is called index, so the generated files will also be called index.

- index.css
- index.map.css

Now, just call this CSS file within your HTML project, and that way you will be authorized to use the SASS libraries.

Within SCSS I can create:

- Pre-Processed Styles without parameters

```scss
@mixin styledText {
  color: gray;
  font-size: 20px;
  font-weight: bold;
}

.myP {
  @include styledText();
}
```

- Pre-Processed Styles with parameters

```scss
@mixin quadrado($tamanho, $cor) {
  width: $tamanho;
  height: $tamanho;
  background-color: $cor;
}

.myDiv {
  @include quadrado(100px, blue);
}
```

- Style Chaining

```scss
ul {
  border: 1px solid red;

  li {
    border: 3px solid teal;

    a {
      background-color: blueviolet;
    }
  }
}
```

- Erance of Styles

```scss
.p1 {
  color: red;
  font-size: 20px;
}

.p2 {
  @extend .p1;
}
```

- Create Variables

```scss
$corPrimaria: #fe534c;
$corSecundaria: #f5f5f5;
$corTerciaria: #000000;

.p1 {
  color: $corPrimaria;
}
```
