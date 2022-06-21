## microfrontend aplication POC
This example demos a basic host application loading remote component.

host is the host application (cra-based).
remote standalone application (cra-based) which exposes Button component.

### Running Demo
Run yarn start. This will build and serve both host and remote on ports 9000 and 8080 respectively.

localhost:9000 (CONTAINER)
localhost:8080 (EXAMPLE APP)

### Folder structure for a scalable app
Using clean architecture to keep de business logic, templates and UI isolated.

```
/
└── src
     ├── bounded-context                
     │      ├── presentation            React Native UI logic, containers, screens, components.
     │      │       ├── i18n     
     │      │       ├── components      
     │      │       └── stylesheets     
     │      ├── application             Application business logic (Use cases).
     │      │       └── custom-hooks 
     │      ├── domain                  Enterprise business logic.
     │      │       ├── entity          
     │      │       ├── failures        
     │      │       └── value-object    
     │      └── infrastructure          Interface to communicate with other contexts. (Local and remote resources)
     │          ├── state-management
     │          ├── services
     │          └── redux
     └── shared  
```

#### TO DO:
[ ] Research about CI and CD in microfrontends.
[ ] Build a example with more logic.
[ ] Share a component from hermes.
[ ] Share a state ?
[ ] Add a UI library to share basic components thought the all organization.

Also we can try use another approach like, Nx, build-time sharing the bundle-js with webpack federation or npm... 

