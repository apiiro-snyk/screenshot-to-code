# screenshot-to-code

This is a simple app that converts a screenshot to HTML/Tailwind CSS. It uses GPT-4 Vision to generate the code, and DALL-E 3 to generate similar looking images.

https://github.com/abi/screenshot-to-code/assets/23818/6cebadae-2fe3-4986-ac6a-8fb9db030045

See Examples section below for more demos.

## Updates

* Nov 16 - Toggle between desktop & mobile preview
* Nov 16 - View code directly within the app
* Nov 15 - 🔥 You can now instruct the AI to update the code as you wish. Useful if the AI messed up some styles or missed a section.


## Getting Started

The app has a React/Vite frontend and a FastAPI backend. You will need an OpenAI API key with access to the GPT-4 Vision API.

Run the backend (I use Poetry for package management - `pip install poetry` if you don't have it):

```bash
cd backend
echo "OPENAI_API_KEY=sk-your-key" > .env
poetry install
poetry shell
poetry run uvicorn main:app --reload --port 7000
```

Run the frontend:

```bash
cd frontend
yarn
yarn dev
```

Open http://localhost:5173 to use the app.

If you prefer to run the backend on a different port, update VITE_WS_BACKEND_URL in `frontend/.env.local`

## FAQs

* **I'm running into an error when setting up the backend. How can I fix it?** [Try this](https://github.com/abi/screenshot-to-code/issues/3#issuecomment-1814777959). If that still doesn't work, open an issue.
* **How do I get an OpenAI API key that has the GPT4 Vision model available?** Create an OpenAI account. And then, you need to buy at least $1 worth of credit on the [Billing dashboard](https://platform.openai.com/account/billing/overview).
* **How can I provide feedback?** For feedback, feature requests and bug reports, open an issue or ping me on [Twitter](https://twitter.com/_abi_). 

## Examples

**Hacker News** but it gets the colors wrong at first so we nudge it

https://github.com/abi/screenshot-to-code/assets/23818/3fec0f77-44e8-4fb3-a769-ac7410315e5d

**NYTimes**

<img width="300" alt="Screenshot 2023-11-16 at 12 06 09 PM" src="https://github.com/abi/screenshot-to-code/assets/23818/01b062c2-f39a-46dd-84ca-bec6c986463a">
<img width="300" alt="Screenshot 2023-11-16 at 12 07 25 PM" src="https://github.com/abi/screenshot-to-code/assets/23818/e1f662b6-68f7-4578-a64d-ea4be52e31f5">



## Hosted Version

Hosted version coming soon on [Pico](https://picoapps.xyz?ref=github).