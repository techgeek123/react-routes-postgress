# Portfolio using React

## Release 0

Create your Portfolio, which should be single page application, contains following links 

- `Home`: contains a brief about yourself and display a few photos of yours.
- `MyProjects`: contains a list of your projects
- `About Me`: contains your education details, experience, achivements, hobbies etc.

## Release 1

Create a Home component `home.js` which renders the informations about yourself and photos

Create a MyProjects component (`myProjects.js`) which renders the details of your projects

Create a `aboutMe.js` component which renders your education details, experience, achivements, hobbies etc.

## Release 2

Finally, our application needs a way to navigate between pages. If we were to create links using anchor elements, clicking on them would cause the whole page to reload. React Router provides a `<Link>` component to prevent that from happening. When clicking a `<Link>`, the URL will be updated and the rendered content will change without reloading the page.

## Release 3

Right now, your portfolio is completely unstyled.In your src folder, create a file called index.css and add style rules into it