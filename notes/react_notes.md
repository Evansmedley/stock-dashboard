# Creating UI

## First Component

- A react component is a JS function that you can sprinkle with markup

```
export default function ComponentName() {
    return (
        <img
            src="https://i.imgur.com/MK3eW3Am.jpg"
            alt="Katherine Johnson"
        />
    )
}
```

- 'export default' prefix is standard JS syntax to mark the main function in a file
- Other than that its just a definition of a function that returns markup
- Can reuse snippets
- Capital letter indicates use of a component, lowercase is HTML tag
- Never nest component definitions
- When a child component needs data from a parent, pass by props instead of nesting definitions
- React app has a root component that is automatically created upon starting a new project
- Most react-based frameworks generate HTML automatically from React components (JS doesn't need to load before app shows content!)
- REACT COMPONENTS ALWAYS BEGIN WITH A CAPITAL LETTER!

```
function Profile() {
  return (
    <img
      src="https://i.imgur.com/MK3eW3As.jpg"
      alt="Katherine Johnson"
    />
  );
}

export default function Gallery() {
  return (
    <section>
      <h1>Amazing scientists</h1>
      <Profile />
      <Profile />
      <Profile />
    </section>
  );
}
```

## Importing and Exporting Components

- A root component file (sometimes App.js) iswhere rendering begins
- Using Next.js (like in this project) means that the root component will be different for every page
- Using `import ComponentName from './componentfile.js';` allows for better modularity
- the .js is mpt required
- To export multiple components from one file there can only be one default, so just leave out the default and use curly braces when importing the component

## Writing Markup with JSX

- JSX is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file
- JSX is a syntax extension, React is a JS library, they can be used independently but are most often used together
- Even though JSX looks like HTML, under the hood it is transformed into plain JS objects, can't return two objects without wrapping them into an array
- Rules of JSX
  - Return a single root element (can just be <> and </> instead, called a fragment)
  - Close all of the tags (even self-closing tags like <img>)
  - camelCase should be used (attributes written in JSX become keys of JS objects)

## JavaScript in JSX with Curly Braces

- To pass a string attribute to JSX, use single or double quotes
- To dynamically specify alt text for example, use a value from JS by replacing " and " with { and }
- Can also embed JavaScript inside of JSX too like the following h1 component
- Only two places to use curly braces
  - As text directly inside of a JSX tag
  - As attributes immediately following the '=' sign
- Can also pass objects in JSX (use double curly braces), this is useful for inline CSS styles

```
export default function Avatar() {
    const description = 'Test Description';
    const exampleObject = {name: 'name', info: 'info'}
    return (
        <>
        <img
            className="test"
            alt={description}
        />
        <h1>{name}'s To Do List</h1>
        <h1>{exampleObject.name}: {exampleObject.info}</h1>
        </>
    );
}
```

## Passing Props to a Component
