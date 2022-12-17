# Term Land (WIP)

A community-driven dictionary app. It has a bunch of languages, each with a bunch of terms. The terms have pronunciations, audio recordings, definitions, and transcriptions into different writing systems. There are user accounts, and users can add/edit terms and their properties. That is pretty much it.

This is used to help give a project to work on, first to illustrate by example how you can write Link Text for an app, and second to help give something to work on to develop the main framework for Link Text, Crow. Crow will have framework stuff like UIComponents and rendering, request handling, querying, etc.. So in the end ideally you should be declaring a bunch of stuff for your app, write a few business logic functions here and there, but otherwise can stay out of the weeds of writing complex framework logic.

## Organization

Term Land's folder/file structure will probably evolve a lot as things go and new things are discovered and refined. But for now, here is a rough idea of how things are organized.

- `base`: Shared code across backend and frontend.
  - `case`: Shared configuration.
  - `find`: Shared GraphQL-like queries.
  - `form`: Shared class definitions.
  - `task`: Shared functions.
- `hide`: The backend folder, none of this code will ever be exposed on the frontend.
  - `find`: Backend SQL-like queries.
  - `save`: Backend SQL-like mutations.
- `hold`: Shared assets.
- `home`: A temporary folder for doing arbitrarys stuff.
- `hook`: The request handling code.
  - `call`: The public API handler.
  - `site`: The main app with its app URLs.
    - `base`: Shared routes for frontend/backend.
    - `host`: Other routes not used on the frontend.
- `read`: The readme docs for this project.
- `show`: The frontend folder, all of this will be bundled into a frontend build.
  - `case`: Frontend configuration.
  - `zone`: Frontend tree components. These are UIComponents, but also higher-level components.
- `task`: Dev-ops scripts and other project tasks.
- `test`: End-2-end tests.
- `text`: Documents used in the app, like legal docs.

The `base/form` directory is where the database schemas will essentially live. Need to define a place for migrations as well.

See for example:

- `show/zone/land/language/link` for an example component, and others in the `zone/land` folder for now.
- `hook/site/base` for site url handlers for rendering SSR pages.

That's pretty much it for now. Need to figure out more DSL structure for more advanced animation cases and such in the rendering. Then need to figure out how querying a SQL database might work for Crow. And then need to compile this code in this repo (and dependent repos) into JavaScript. Maybe make a smart auto-import / lookup definition sort of language server for Link.

## License

Copyright 2022 <a href='https://drum.work'>TreeSurf</a>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## TreeSurf

This is being developed by the folks at [TreeSurf](https://drum.work), a California-based project for helping humanity master information and computation. TreeSurf started off in the winter of 2008 as a spark of an idea, to forming a company 10 years later in the winter of 2018, to a seed of a project just beginning its development phases. It is entirely bootstrapped by working full time and running [Etsy](https://etsy.com/shop/teamtreesurf) and [Amazon](https://www.amazon.com/s?rh=p_27%3AMount+Build) shops. Also find us on [Facebook](https://www.facebook.com/teamtreesurf), [Twitter](https://twitter.com/teamtreesurf), and [LinkedIn](https://www.linkedin.com/company/teamtreesurf). Check out our other GitHub projects as well!
