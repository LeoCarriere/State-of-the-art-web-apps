# React

React is there to simplify the development of interactive and efficient user interfaces by providing a component-based architecture and a virtual DOM for optimal rendering performance.  
<br/>

## Files extension

- ```.js ``` standard JavaScript files.
- ```.jsx ``` files that contain both JavaScript and JSX code (UI components).
- ```.ts ``` TypeScript files (with static typing, classes, etc.).
- ```.tsx ``` TypeScript files with the features of JSX (UI components).  

<br/>

> Note that sometimes any of these could be interpreted by React or other tool as JSX.
> This is why sometimes, you can see UI components wrote into a JS file. 
> However this is a bad practice as certain tools won't expect a JS file there

<br/>


## Start a new React project

> You can use React without a framework, however we’ve found that most apps and sites eventually build solutions to common problems such as code-splitting, routing, data fetching, and generating HTML. These problems are common to all UI libraries, not just React.  

<br/>

## React Concepts :
 - **Components** <br/> 
   Briques réutilisables à l'infini pour structurer l'application<br/> <br/> 

 - **JSX** <br/> 
   Optionnel en théorie, mais permet d'avoir des erreurs plutôt que l'app entiere plante <br/> <br/> 

 - **Dynamic JavaScript**<br/>
   ```{variable}```<br/> <br/> 

 - **Fragments** <br/> 
   Tous les components doivent retourner un seul element, mais si on ne veut pas wrap dans un div, on peut utiliser un fragment ```<>...</>```<br/> <br/> 

 - **Props** <br/> 
   Propriétés CamelCase qui servent à passer des données à un component <br/> <br/> 

 - **Children** <br/> 
   ```function Parent(props){return <div>{props.children}</div>}``` → ```<Parent><Child /></Parent>```<br/> <br/> 

 - **Keys** <br/> 
   Permet d'identifier uniquement un component (souvent utilisé pour les listes, peut etre un int ou un string) <br/> <br/> 

 - **Rendering** <br/> 
   VDOM etc.<br/> <br/> 

 - **Event Handling** <br/> 
   Un peu comme les commandes en MVVM. <br/> 
   Examples fréquent →```<button onClick={handleClick}/>``` ```<input onChange={handleChange}/>``` ```<form 
   onSubmit=
   {handleSubmit}
   />```<br/> <br/> 

 - **State** <br/> 
   ```const [likes,setLikes] = useState(0)``` *0* est la valeur initiale par défaut. *setLikes* est la fonction qui gere la valeur de *likes*.<br/> <br/> 

 - **Controlled Components** 
```jsx
function controlledInput(){ 
    const [value,setValue] = useState('')
    return( <input value={value} 
                   onChange={(e)=>(e.target.value)}
             />
           )
    }
```

- **Hooks** <br/> 
  TODO... <br/> <br/> 
- **Purity** <br/> 
  Chaque component auquel on donne une meme input doit toujours ressortir la même output. Autrement dit il doit retourner uniquement du JSX sans modifier des valeur 
  externes. 
  <br/> <br/> 

- **Strict Mode** <br/> 
  TODO... <br/> <br/> 

- **Effect** <br/> 
  Code qui doit acceder à des ressources externes à React. Exemple :
```jsx
useEffect(() => {
   fetchData().then( data => {
       // use data
   })
}, []);
```

- **Refs** <br/> 
  TODO... <br/> <br/> 

- **Context**<br/> 
  Permet de partager des valeurs sans qu'elles passent par tous les components.<br/> <br/> 

```jsx
const AppContext = createContext()
```
```jsx
<AppContext.Provider>
    <App/>
</AppContext.Provider>
```
... TODO

- **Portal** <br/> 
  Envoie le contenu dans un parent, souvent utilisé pour les fenêtres modales / dropdowns / tooltips <br/> <br/> 

- **Suspense** <br/> 
  
```jsx
<Suspenser fallback={<Loading />}>
    <Component />
</Suspenser>
```


- **Error Boundaries** <br/> 
  TODO... <br/> <br/> 

***
