# Svelte

One of the essential feature of Svelte is the ```.svelte``` extension encapsulating a one component by file. 

```.svelte``` component are usually divided in 3 parts :
- ```<script>``` for import dynamic back-end variables etc.
- some ```HTML``` ```jsx``` content
- and ```<style>``` for the component  

<br/>

Here is a basic example from the [Svelte documentation](https://learn.svelte.dev/tutorial/nested-components) :
```jsx
<script>
	import Nested from './Nested.svelte';
</script>

<p>This is a paragraph.</p>
<Nested />

<style>
	p {
		color: goldenrod;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>
```
## Compiler
An important point is that Svelte compiler :

> "Svelte is a compiler that generates minimal and highly optimized JavaScript code from our sources; you'll need a terminal with node + npm installed to compile and build your app."
>
> Source : [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Svelte_getting_started)

To my understanding, as you code in JavaScript + HTML + CSS when building the application, this is converted into JavaScript only. So it is bundling only what is necessary for your application, doing most of the performance optimizations for you.


## Documentation
The interactive doc is one of the best way to learn Svelte and is very well made. Here is the [link](https://learn.svelte.dev/), this one does not require to setup a local environement and really involve you in the learning process.

There is also a more [traditional documentation](https://svelte.dev/docs/) once you already get the grasp of the Framework.


## Svelte != SvelteKit
>Whereas Svelte is a component framework while SvelteKit is an app framework (or 'metaframework', depending on who you ask) that solves the tricky problems of building something production-ready :
>   - Routing
>   - Server-side rendering
>   - Data fetching
>   - Service workers
>   - TypeScript integration
>   - Prerendering
>   - Single-page apps
>   - Library packaging
>   - Optimised production builds
>   - Deploying to different hosting providers
>   - ...and so on
>
> Source : [learn.svelte.dev](https://learn.svelte.dev/tutorial/introducing-sveltekit)

I guess Svelte vs SvelteKit could be seen as React vs Next.js or React vs Remix.


## Personal Thought / Conclusion
Svelte seems to be rising in popularity and praised by many while it is still early to say if can on day surpass user count that fully fledge Framework with already years of production-ready adoptions like React. Some of the reason for it's popularity being as to this day Svelte is a standalone independent project while being less off a headache to understand than React with his steep learning curve.
I think it is a very promising Framework on which we should stay updated.