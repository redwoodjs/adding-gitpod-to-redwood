;tk - Add GitPod + Redwood logo to the top

RedwoodJS is a full-stack JavaScript framework that combines React, GraphQL, Prisma, Jest, and Storybook to build modern web applications. With this starter, setting up a RedwoodJS development environment in GitPod becomes a straightforward process. It provides a preconfigured development environment with all the necessary tools and dependencies, allowing you to focus on building your RedwoodJS application without worrying about the setup. Get started quickly and efficiently by launching RedwoodJS inside GitPod!

_NOTE:_ If you're starting a brand new Redwood project, we recommend using our [Gitpod Starter repo]() as a starting point. Otherwise, this repo contains the files that wil need to be **added to** your existing repository.

## Adding an "Open in Gitpod" button to your repo:

```md
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/from-referrer/)
```

OR

```md
;tk
```

# Add these files to your repo:
## gitpod.yml

This contains the bulk of the GitPod setup. We're using the `gitpod/workspace-postgres` image.

Then, we're running a couple of tasks to initialize the workspace.

Then, we're running the script inside `gitpod-setup.js`.

We've specified several ports:

- `5432` for Postgres
- `8910` for the frontend
- `8911` for the backend

Lastly, we've listed 8 recommended VS Code extensions to install:
  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
  - [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  - [VS Code Language - Babel](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel)
  - [VS Code Version Lens](https://marketplace.visualstudio.com/items?itemName=pflannery.vscode-versionlens)
  - [Editor Config](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
  - [Prisma](https://marketplace.visualstudio.com/items?itemName=Prisma.prisma)
  - [VS Code GraphQL](https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql)

If you want to add change these, you can modify lines 34 - 41 of the .gitpod.yml file


## .gitpod.env

This file lists initializes the environment variables for the workspace.

This file contains 3 environmental variables, specifically for working with Gitpod. These are _not secrets_ and should be included in your repo.

```text
DATABASE_URL=postgres://gitpod@localhost:5432/dev
TEST_DATABASE_URL=postgres://gitpod@localhost:5432/test
PRISMA_HIDE_UPDATE_MESSAGE=true
```