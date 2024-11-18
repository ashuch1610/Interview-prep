# Interview-prep
**Pass an Object as props to a component in React.js**

1.function Person({name, age, country}) {
  return (
    <div>
      <h2>{name}</h2>
      <h2>{age}</h2>
      <h2>{country}</h2>
    </div>
  );
}

export default function App() {
  const obj = {name: 'Alice', age: 29, country: 'Austria'};

  return (
    <div>
      <Person {...obj} />
    </div>
  );
}

2.function Person({data}) {
  return (
    <div>
      <h2>{data.name}</h2>
      <h2>{data.age}</h2>
      <h2>{data.country}</h2>
    </div>
  );
}

export default function App() {
  const obj = {name: 'Alice', age: 29, country: 'Austria'};

  return (
    <div>
      <Person data={obj} />
    </div>
  );
}


3.// ComponentA.jsx
const ComponentA = ({ message }) => {
  return <div>{message}</div>;
};

// ComponentB.jsx
const ComponentB = ({ CustomComponent }) => {
  return (
    <div>
      <h2>Component B</h2>
      {/* Pass additional props to CustomComponent */}
      <CustomComponent message="Hello from ComponentA with props!" />
    </div>
  );
};

