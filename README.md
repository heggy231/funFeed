# funFeed

JSX: Must return single <div>

- https://docs.google.com/presentation/d/144DViot4VJSOx-jmXDLIExE06Wky6pFS4QKkHZxtl1o/edit#slide=id.g1ea4206e08_2_82

- JSX
const MyComponent = () => {
  return (
    <div className="MyComponent">
      <h1>Hello, world! I am a Component!</h1>
      <img src="http://vectorlogo.zone/logos/reactjs/reactjs-card.png" />
    </div>
  )
}
  // output: Hello, world! I am a Component!



JSX = HTML(ish) + JS

-
  Logic can be contained within {}
  ‣ this can be any valid JS expression (i.e. one-liner)

const MyComponent = () => {
  const myLanguages = ['JSX', 'HTML']
  return (
    <div className="MyComponent">
      <h1>Hello, world! I am a Component!</h1>
      <p>{`I’m made up of ${myLanguages.join(' & ')}!`}</p>
    </div>
  )
}

// I’m made up of JSX & HTML!

***** refactor
const MyComponent = () => {
  const myLanguages = ['JSX', 'HTML']
  return (
    <div className="MyComponent">
      <h1>Hello, world! I am a Component!</h1>
      <p>{`I’m made up of ${myLanguages.join(' & ')}!`}</p>
    </div>
  )
}

Ex 3- React hello world
https://jsfiddle.net/hyendler/t167qrap/1/


- Props with Functional Components 
const Welcome = () =>
  <div className="Welcome">
    <img src="https://tinyurl.com/GDISFbanner"/>
    <Greeting 
      course={{ name: "React.js", location: "Eventbrite" }}
      name="Hanah" />
  </div>

/* what JS sees

const props = {
  name: 'Hanah',
  course: {
    name: 'React.js',
    location: 'Eventbrite'
  }
}
*/


Props are how we pass data from a parent component to a child component!
They contain information the component can use in its logic and/or rendering.  
In Functional Components, they are passed as a single argument: an object.
[In Class Components they are attributes - more on Class Components later.]
Props are variables, so to access them within JSX, use {}


**PROPS ARE IMMUTABLE** so don’t try to change them!

  - https://jsfiddle.net/heggycastaneda/7ut0Ljsp/16/