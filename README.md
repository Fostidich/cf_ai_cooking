# Cooking

## Features

### Grocery generation

Users can set up a list of all the meals they intend to consume during the week.
This comprehends breakfast, launch, and dinner, and additional snacks.
Moreover, the user can also select a set of week days in which it is available to go and buy groceries.

The AI assistant then takes over, generating a groceries list for each of the selected days, so that what's bought will fulfill the whole preparation of the days-after meals, ingredient-wise.

### Recipe support

Users can select one of their meals included in the weekdays (or prompt for a new one) to ask the AI assistant for a pointed list describing how the recipe should proceed, including quantities, cook times and good practices.
In this way the user receives a simple and comprehensible to-do list for the meal preparation, aware of the groceries previously fetched.

### Suggestions creation

Often times people forget to plan ahead what to eat, and what's home feels either insufficient or unenjoyable.
It is possible for users to prompt the AI assistant telling which ingredients are available in the house, for then receiving a set of possible meal ideas plausible to prepare and eat.

## Usage

The user will be able to use the app via the browser, and therefore it must be connected to the internet to be able to interact with the AI assistant, and to view its data.
A minimal UI will provide easy access to the main sections/pages:

- a page for inserting the week's meals and generating/viewing the groceries list;
- a page for prompting the AI assistant for recipe steps;
- a page for inserting which ingredients the user has available and for then requesting meal ideas.

Moreover, a floating, pop-up helper panel is always available to expand, for interacting with a chatbot aware of the user state in the app.

## Tech stack

- The AI assistant will be implemented via API calls to CloudFlare's Workers AI LLM.
- Stateful, multi-step AI assistant interactions will be achieved via CloudFlare's Workflow.
- To let users message with the AI assistant, a web app UI hosted with CloudFlare's Page will be developed.
- To store user data and past generated content, CloudFlare's Durable Objects will be in use.

The language used will be TypeScript, as Cloudflare Workers support it natively.
Moreover, it integrates seamlessly with the UI framework: React.

