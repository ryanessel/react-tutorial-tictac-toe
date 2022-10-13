
React - is a declarative, effiecient, and flexible JS **library** for building user interfaces. Lets you compoe complex UIs from small isolated code called **componets**

React has serveral **component**
1. React.Component subclasses

=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-
EXAMPLE
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>   <--- THE BIT IN THE {} is the JSX SYNTAX
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}

its like html you use in JS
// Example usage: <ShoppingList name="Mark" />
=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

**ShoppingList** is a **React component class** or **React component type**.

**component** takes in params called **props** (short for *properties*) and returns a hierarchy of views to display -via- the **render** method.

**render** method returns a description of what you want to see on the screen. React takes the description and display the result. Speficially, **render** returns a **React Element** which is a light weight descirption of what to render.
Most React devs use a special syntax called "JSX" which makes these structures easier to write. The <div /> syntax is transformed at build time to "React.createElement('div')"


 The example above is equivalent to the bit below:
 =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-
return React.createElement('div', {className: 'shopping-list'},
  React.createElement('h1', /* ... h1 children ... */),
  React.createElement('ul', /* ... ul children ... */)
);
=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

JSX EXPRESSION EXAMPLE:
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

JSX allows you to use javascript completely and you can use any JS expression within bracces inside JSX. Eact REact elem is a js obj that you can store in a variable or pass around in your program.

The ShopppingList component above only renders built-in DOM cocmponents like <div /> or <li />. 
BUT you can compose and render custom React components too. 
For example we can refert to the whole shopping list like in the "EXAMPLE USAGE" above as in <ShoppingList /> (ITS LIKEIT BECCOMES A TAG (IN REACT ITS A "REACT COMPONENT" i think...))

