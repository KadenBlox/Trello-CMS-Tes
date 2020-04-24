# Hello Trello

A little experiment to pull content from the Trello API and use it to populate content on a simple web site.

- Production: [https://hellotrello.netlify.app](https://hellotrello.netlify.app)
- Staging: [https://stage--hellotrello.netlify.app](https://hellotrello.netlify.app)

The site is populated from a list of cards in a public (but read only) [Trello board](https://trello.com/b/Zzc0USwZ/hellotrello)


## Sections from cards

Each card in Trello populates a section of the page. And since Trello supports markdown, we can also do some simple text formatting with the markdown we get from the cards API.


## Webhooks trigger updates

Whenever we make changes in the Published list, Trello triggers a [Netlify build hook](https://docs.netlify.com/configure-builds/build-hooks/?utm_source=github&utm_medium=hellotrello-pnh&utm_campaign=devex) which initiates a new build and deployment, updating the site.

Trello paid accounts can have buttons which can make HTTP Post requests, which means we cold have a button which initiates a site deployment on Netlify via a build hook.

## Staging / Production

Netlify lets you create an unlimited number of environments [based on git branches](https://docs.netlify.com/site-deploys/overview/#branches-and-deploys?utm_source=github&utm_medium=hellotrello-pnh&utm_campaign=devex). Each gets its own URL. This example maps the labels on the Trello cards to the different branches, so we event get a simple publishing workflow.


## TODO

- Add a simple starting template for others
- List the APIs and services this uses.
- Create automated way to create the webhooks and join them up for a speedy on-ramp.
